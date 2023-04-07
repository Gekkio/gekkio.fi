+++
title = "Power consumption of Game Boy flash cartridges"
date = 2021-04-17
+++

Flash cartridges (= "carts") are commonly used to run Game Boy ROMs, such as homebrew games or dumped officially released games, on real hardware. Different kinds of flash carts with various features and performance characteristics have been available for a long time, but flash carts have in general the reputation of consuming a lot of power, greatly reducing the battery life of a Game Boy system, and possibly causing other additional problems. System stability might suffer, especially on Game Boy Pocket, and flash carts can also increase audible noise. Many of these problems have become more obvious in the recent years, since Game Boy modding is nowadays very popular and many modern mods, such as IPS screens, consume a lot of extra power. Some people claim that certain mods are simply incompatible with flash carts, and sometimes people say an extra regluator mod is needed in order to safely use flash carts. There is some truth to these claims, but unfortunately the fine details tend to matter and these kind of blanket statements can be misleading!

In order to research the topic, I tested the power consumption of several commonly available flash carts and some of my own designs. In this blog post I intend to show that there is more variation in flash cart power consumption than people might think, and a flash cart can even be more power efficient than a genuine cart!

## Tested cartridges

### Genuine Tetris from 1997

{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/tetris_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/tetris_pcb_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/tetris_pcb_back.jpg", op="fit_height", height=300) }}

This is a genuine Tetris cart from 1997 that uses a glop top mask ROM. Since there are no other chips (e.g. MBC or RAM) on the board and the mask ROM capacity is small, the power consumption is very low. This simplicity means the cartridge presents a tough challenge for more complicated flash carts in power consumption tests.

### Genuine Pokemon Blue from 1998

{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/blue_genuine_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/blue_genuine_pcb_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/blue_genuine_pcb_back.jpg", op="fit_height", height=300) }}

This is a genuine Pokemon Blue cartridge with a very typical ROM+RAM+MBC chip combination. While the exact chips used may vary, this kind of combination is very common in officially released Game Boy games. This is why it provides a more realistic comparison point than Tetris.

### Cheap reproduction Pokemon Blue

{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/blue_repro_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/blue_repro_pcb_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/blue_repro_pcb_back.jpg", op="fit_height", height=300) }}

This is a cheap reproduction cartridge I bought from AliExpress for research purposes. It has clearly been designed with only cost in mind, because the design violates some chip ratings and does not even have PCB edge gold fingers. A poorly designed cartridge that would undoubtedly not survive constant use for very long, but it's still interesting to include it in the comparison.

### Genuine Wario Land II (GBC release) from 1998

{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/wario_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/wario_pcb_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/wario_pcb_back.jpg", op="fit_height", height=300) }}

This is a genuine Wario Land II cartridge. Like Pokemon Blue, it uses a very typical set of chips, but this one uses MBC5 instead of MBC3. Note that Wario Land II had more than one release, and this is the western Game Boy Color -enhanced release that is still compatible with all Game Boy consoles.

### Everdrive GB

{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/edgb_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/edgb_pcb_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/edgb_pcb_back.jpg", op="fit_height", height=300) }}

The original Everdrive used to be a very popular flash cartridge, but has recently been obsoleted by newer products. It uses an SD card, so multiple games can be stored and easily switched with the initial menu program that appears when the system powers up.

The tested cartridge PCB is labeled as "v1.2", "13.03.2014", and was used with firmware v4.

### Everdrive GB X5

{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/edgbx5_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/edgbx5_pcb_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/edgbx5_pcb_back.jpg", op="fit_height", height=300) }}

Everdrive GB X5 is a newer Everdrive model with greatly improved design and performance. Like its predecessor, it uses an SD card. The X-series also includes X3 and X7, but I only tested the X5 model, which omits some features like RTC from the most expensive X7 model. Note that the circuit board says "X7" but several components are missing, so it seems the same board design is used in both X5 and X7.

The tested cartridge PCB is labeled as "Model 17", "Rev B", "26.08.2017", and was used with firmware v1.04.

### EZ-FLASH Junior

{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/ezflash_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/ezflash_pcb_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/ezflash_pcb_back.jpg", op="fit_height", height=300) }}

EZ-FLASH Junior is another flash cart that uses an SD card. Its product page boasts about it having a lot of features, like RTC support, and it costs quite a lot less than an Everdrive GB X5.

The tested cartridge PCB is labeled as "1320", and was used with kernel 1.04e and firmware v4.

### EMS64

{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/ems64_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/ems64_pcb_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/ems64_pcb_back.jpg", op="fit_height", height=300) }}

This one is a fairly old USB-based cartridge. Instead of using an SD card, you simply flash it using a USB Note that there are several EMS64 versions with very different designs, so results for this particular version might be different compared to other versions.

The tested cartridge PCB is labeled as "GB64USB-12".

### GB-CART32K-A

{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/cart32k_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/cart32k_pcb_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/cart32k_pcb_back.jpg", op="fit_height", height=300) }}

This is one of my designs and a simple 32 kB flash cartridge with support for only one 32 kB ROM. It's very limited but a good choice if you only need a cartridge to run a simple game. The design is open source and can be found in my [gb-hardware repository](https://github.com/Gekkio/gb-hardware/tree/master/GB-CART32K-A).

The tested version was GB-CART32K-A v1.0 with an SST39SF020A flash chip.

#### GB-CART256K-A

{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/cart256k_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/cart256k_pcb_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/cart256k_pcb_back.jpg", op="fit_height", height=300) }}

This is one of my designs and a ROM-only flash cartridge with support for 256 kB ROM and either MBC1 or MBC5 emulation using a CPLD. There's no support for save games, but it's a good choice for games that need a larger ROM size than 32 kB. The design is open source and can be found in my [gb-hardware repository](https://github.com/Gekkio/gb-hardware/tree/master/GB-CART256K-A).

Note: the circuit board says GB-CART2M-A, because that's the old name of the project before I renamed it for consistency with my other cartridges.

The tested version was GB-CART256K-A v1.1 with an SST39SF020A flash chip.

#### GB-CART8M-A

{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/cart8m_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/cart8m_pcb_front.jpg", op="fit_height", height=300) }}
{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/cart8m_pcb_back.jpg", op="fit_height", height=300) }}

This is one of my designs and a "maxed-out" design with support for 8 MB ROM and 128 kB save RAM. It only supports MBC5 emulation but can handle the largest ROM/RAM official MBC chips can support so any Game Boy game will fit. There's no support for RTC or other extra features. The design is intended to be open source but hasn't yet been published.

The tested version was GB-CART8M-A v2.1 with an MX29LV640E flash chip and an IS62WV1024E RAM chip.

## Test setup

{{ thumbnail_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/test_setup.jpg", op="fit_height", height=300) }}

An original Game Boy (DMG) was powered with a [Rohde & Schwarz HMC8043](https://www.rohde-schwarz.com/us/products/test-and-measurement/dc-power-supplies/rs-hmc804x-dc-power-supply-series_63493-61542.html) programmable power supply using the DC jack input providing a stable +6V input voltage. The power supply was controlled with SCPI commands via USBTMC by an automated test running on a PC. Testing some cartridges involves going through an initial menu after powering on the system, and in these cases some manual steps were necessary to complete the test.

The used console has the serial number **G38953646**, and uses a B version SoC chip and a type C power board. You can read more details about the test console on its [Game Boy hardware database entry page](https://gbhwdb.gekkio.fi/consoles/dmg/G38953646.html).

Input voltage and current data was collected using the data logging functionality of HMC8043 with a 1ms sampling interval, which according to the device datasheet results in a resolution of 10mV / 1mA. Using a fairly short sampling interval for the raw data allows collecting data about short spikes in current and other fine-grained detail. However, too much detail is not very useful when comparing power consumption from a high-level point of view. For example, with 1ms sampling interval it's possible to see even the vblank times of drawn frames, because the Game Boy PPU (= Pixel Processing Unit) consumes less power at that point of time and there's a dip in the measured input current! It's an interesting research topic, but right now we're interested in the more high level differences between cartridges, so a rolling mean with 50ms window was used in postprocessing to smooth out the unnecessary detail from the data.

The following extra steps were taken to minimize potential inconsistencies in the test setup:

- The screen contrast was turned all the way up, so the screen was completely black. If an SD card cartridge was used, I learned in advance how to navigate the menu and load the test ROM without looking at the screen
- Audio volume was turned all the way up
- The exactly same SD card was used to test all SD flash cartridges. I don't know if the cartridges keep the SD card powered when a game is running, but using the same SD card is in any case a good idea for consistency

### Pseudo-code of the automated test

```rust
hmc.instrument_select(Channel::Ch3)
hmc.voltage(6.0)
hmc.current(3.0)
hmc.fuse(true)
hmc.voltage_protection(true)
hmc.voltage_protection_level(Limit::Max)
hmc.power_protection(true)
hmc.power_protection_level(Limit::Max)
hmc.voltage_ramp(true)
hmc.voltage_ramp_duration(Duration::from_millis(10))
hmc.output_channel(true)

hmc.log_file("test.csv", FileLocation::External)
hmc.log_channel(true)
hmc.log_mode(LogMode::Unlimited)
hmc.log_interval(Duration::from_millis(100))
hmc.log(true)

hmc.output_master(true)

pause_until_manual_stop()

hmc.log(false)
hmc.output_master(false)
```

## Power consumption at startup

In our first test, we'll take a look at the power consumption immediately after the system has powered up before the actual cartridge ROM starts executing. This will give us some idea of static power consumption of the cartridge when the cartridge is not actually being accessed most of the time.

### No cartridge inserted - startup measurement

First, let's take a look at a measurement done without any cartridge inserted in the system.

{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/no_cartridge.svg", height=400) }}

There are three especially interesting highlights in the figure:

  1. There is a large initial inrush current immediately after the system has been powered up. This is perfectly normal, but extremely large inrush currents can blow a fuse in a system. Note that the 50ms rolling mean used in data postprocessing actually hides the real peak in the data and we're seeing a smoothed version of the peak! The actual peak can be very high and sharp, and could be measured using a different technique. However, this time we're not focusing on accurate inrush current testing.
  2. There is another much smaller peak after the initial inrush current has almost settled. I suspect this is caused by the system getting released from reset state, so many things are powering up at the same time.
  3. The third peak is much wider, and is caused by the "cha ding!" sound after the logo has scrolled down. Since we're using the system at max volume, we can sometimes see the audio the console is playing as input power variations in the data!

If we ignore the peaks and look at the more stable time periods, it looks like the system input power normally hovers around ~235 mW. The peaks are also interesting and especially the third peak will be important in later tests, because the "cha ding!" sound will be used to align measurements from different flash carts.

### Genuine cartridges - startup measurement

{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/genuine_startup.svg", height=400) }}
{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/genuine_startup_zoom.svg", height=400) }}

It looks like Tetris consumes almost no extra power compared to having no cartridge inserted, while Pokemon Blue and Wario Land II consume slightly more with the normal input power hovering around ~250 mW. It also seems like Pokemon Blue might be consuming a tiny amount more than Wario Land II, but this difference is very minor.

### Reproduction Pokemon Blue - startup measurement

{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/repro_startup.svg", height=400) }}
{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/repro_startup_zoom.svg", height=400) }}

The reproduction cart is interesting: *it consumes less power than the genuine cart* in the startup measurement.

### Gekkio flash carts - startup measurement

{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/gekkio_startup.svg", height=400) }}
{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/gekkio_startup_zoom.svg", height=400) }}

My flash cart designs consume very little power in this test and are roughly comparable to having no cartridge, although if we zoom in, we can see the flash carts consuming a tiny bit more power. GB-CART8M-A consumes slightly more power than the other two, and it looks like GB-CART256K-A might just barely lose to GB-CART32K-A.

This figure also shows an interesting extra detail: GB-CART8M-A has different behaviour than others and generates different kinds of peaks. Firstly, the smaller peak after the large inrush current event is missing, and we actually see *a wide dip* until the input power goes to the normal state. The "cha ding!" sound peak also happens later but looks otherwise normal. These differences are caused by power supervisor circuitry in GB-CART8M-A, which keeps the system in reset state until the system voltage has been stable for a certain duration of time. This is a safety feature to help keep inrush current at reasonable levels, and to ensure the cartridge has a stable voltage before it starts doing anything important. Genuine carts that support saves also have a supervisor mechanism to help keep your save games safe, but they use different kind of chips which get out of reset state much more quickly, so we don't see the behaviour in the figure in this test scenario.

### EMS64M - startup measurement

{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/ems64m_startup.svg", height=400) }}

Like GB-CART8M-A, EMS64M seems to have some kind of supervisor circuitry on the cartridge, but it results in a narrower dip during startup and the "cha ding!" sound peak has less delay than GB-CART8M-A does. Overall the cartridge consumes more power than the genuine carts, my flash carts, and the reproduction cart. However, the difference isn't huge, so I'd say EMS64M performs pretty well in this measurement.

### Everdrive GB - startup measurement

{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/everdrive_startup.svg", height=400) }}

The original Everdrive cartridge generates a curve shaped very much like the previously tested cartridges. However, there's a *massive* vertical offset so the cartridge consumes a lot more power than the others. The normal stable input power in this measurement was around ~465 mW, which is almost double compared to a genuine Tetris cartridge!

### Everdrive GB X5 - startup measurement

{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/everdrive_x5_startup.svg", height=400) }}

Everdrive X5 performs much better than the original Everdrive, bringing the power consumption closer to the competition. However, it still loses to genuine cartridges, EMS64M, and my designs.

### EZ-FLASH Junior - startup measurement

{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/ezflash_startup.svg", height=400) }}

EZ-FLASH Junior has the worst performance of all in this measurement. Input power during inrush current event goes off the chart, it consumes overall the most input power of all tested cartridges, and the input power does not even seem to fully stabilize during the test time. Not great at all.

## Power consumption of Tetris

In this second test we measure power consumption of various carts when Tetris (v1.1, the more common version) is being played. The measurement data has been aligned to start from the "cha ding!" sound peak to make different cartridges easy to compare. This is necessary, because some carts keep the system in reset state for some time during startup, and the SD card -based flash carts need to go through a menu before they load the correct ROM.

### Genuine cartridge - Tetris

Let's start with the genuine cartridge so we can understand what the power consumption graph looks like by default.

{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/genuine_tetris.svg", height=400) }}
{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/genuine_tetris_zoom.svg", height=400) }}

  1. After the "cha ding!", this is where the boot ROM code embedded in the console ends, and the code on the cartridge starts executing. Power consumption goes up because data gets read from the cartridge very often and this consumes more power than the cartridge being just on standby. The exact behaviour depends on what the cartridge code is doing, but in the case of Tetris, the code makes some preparations, shows the "copyright screen" which has no music, and simply waits for a couple of seconds in a hot loop executing from the cartridge.
  2. This is where the title screen is shown and music starts to play. Audio consumes some extra power, and you can even see many of the individual notes of the title screen melody in the power graph if you look carefully and try to imagine the music in your head!

### Gekkio flash carts - Tetris

{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/gekkio_tetris.svg", height=400) }}
{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/gekkio_tetris_zoom.svg", height=400) }}

My flash carts remain competitive with the genuine cart, but do consume slightly more power. In startup measurements differences between my flash carts were very tiny, but here you can clearly see the flash carts ordered by power consumption: GB-CART32K-A consumes the least, and GB-CART8M-A and consumes the most.

**For simplicity, I'll leave out GB-CART32K-A and GB-CART256K-A from further comparisons and only include the "worst" of my flash carts: GB-CART8M-A.**

### The grand power consumption comparison - Tetris

{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/all_tetris.svg", height=400) }}

Unsurprisingly all flash carts lose to the genuine cart, but there's a large amount of variation between different carts. As an example, if we calculate the mean power consumption in the 2s - 9s time interval and compare the flash carts to genuine Tetris, we get the following relative power consumption values:

- GB-CART8M-A: +6%
- Everdrive GB X5: +30%
- EZ-FLASH Junior: +66%
- EMS64M: +96%
- Everdrive GB: +120%

If we assume the relative power consumption remains roughly similar all the time, using an original Everdrive to play Tetris gives you *less than half* the battery life compared to a genuine cart.

It's also interesting that EMS64M starts with much lower power consumption during the "cha ding!" sound, but then the power consumption increases massively. When the game is actually running, it manages to only beat the original Everdrive. It seems that the cartridge has reasonable static power consumption but very high dynamic power consumption.

## Power consumption of Wario Land II

Now, let's take a look at a more complicated game: Wario Land II.

{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/all_wario.svg", height=400) }}

  1. At this point something strange happens: the genuine cart and GB-CART8M-A show a narrow power consumption peak, while all other flash carts have a wider peak and the rest of the figure is delayed slightly. This suggests the other flash carts end up executing slightly different code for some reason. I don't have a good explanation for this, but I suspect the flash carts may have initialized the save RAM contents with zeroes or some other pattern, and the RAM contains a different kind of pattern than in the other carts. If the code is calculating a checksum of the RAM contents or something like that, the code might take different amount of time to execute depending on the RAM contents.
  2. This is where the intro animation with clouds and music starts. The power consumption of EMS64M drops significantly, which might be caused by the CPU spending more time sleeping in HALT mode instead of reading bytes from the cartridge all the time.
  3. This is where the music changes and an island appears from behind the clouds. Once again, the power consumption of EMS64M drops. I suspect that playing back the different kind of music here requires reading less bytes from the cartridge, so the CPU is spending even more time sleeping in HALT mode.

In most cases the power consumption looks quite similar to Tetris. This makes sense, because a more complicated game with a bigger ROM and/or RAM probably won't greatly affect power consumption of a flash cartridge. However, EMS64M ranks a bit more favourably here than with Tetris, possibly due to the CPU HALT mode reducing dynamic power consumption as suggested earlier. Also, this time GB-CART8M-A beats the genuine cart. The difference is very small, but this proves a flash cart can consume less power than a genuine cart!

## Power consumption of Pokemon Blue

Finally, let's test Pokemon Blue. This time a repro cart is also included.

### Genuine vs repro - Pokemon Blue

{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/genuine_vs_repro_blue.svg", height=400) }}

I honestly didn't expect the repro to beat the genuine cart in power consumption, but it has a slight advantage here. It's also worth noting that the repro figure shape looks a bit different, because it's executing a patched ROM and not the original genuine ROM. This repro cart uses only flash memory and doesn't have battery-backed save RAM on the circuit board, so it needs a patched ROM which uses a portion of the flash memory as "save RAM".

### The grand power consumption comparison - Pokemon Blue

Now that we've looked at the repro, we can drop it from the test and focus on the flash cartridges.

{{ svg_link(path="blog/2021/power-consumption-of-game-boy-flash-cartridges/all_blue.svg", height=400) }}

This flash cart test with Pokemon Blue tells a similar story as Wario Land II, but with one big difference: this time EMS64M is actually competing with Everdrive GB X5 during most of the time in the test! Perhaps Pokemon Blue intro spends even less time reading cartridge bytes than Wario Land II? I don't think this result improves my general opinion of EMS64M, but it confirms its power consumption can vary greatly depending on how often and in what manner the cartridge is accessed.

## Conclusions

All the tested flash carts except EMS64M had fairly stable behaviour so it's possible to rank them from best to worst based on these power consumption tests.

My cartridge designs prove that flash carts can consume less power than genuine cartridges, but they are are not widely available and are mostly interesting to people with the right skills and equipment to assemble them. The best widely available flash cartridge seems to be Everdrive GB X5, which is a massive improvement compared to the original Everdrive GB, which in turn was the worst cartridge. EZ-FLASH Junior was disappointing, and I was personally expecting it to perform much better. EMS64M power consumption varied greatly, so battery life depends on what game you play and how the game has been programmed.

My personal recommendations in case you're looking to buy a flash cartridge:

- Don't buy the original Everdrive GB or any of its clones. I've heard some clones have a "power saving module" (most likely a switching regulator), but I don't think it can make a big enough difference if the design is otherwise the same
- If you want an SD-card based flash cart, buy an Everdrive GB X-series cartridge if you can afford it. If you go with EZ-FLASH Junior, be prepared for a much lower battery life and potential problems if you have modded your console
- Avoid EMS64M

### Raw CSV data files

Here are the raw data files of all measurements. Note that these files have not been postprocessed with the 50ms rolling mean mentioned earlier, so there's more fine detail and fast transients than in the figures shown in this blog post.

- [No cartridge](no_cartridge.csv)
- Genuine cart: [Tetris](genuine_tetris.csv), [Wario Land II](genuine_wario.csv), [Pokemon Blue](genuine_blue.csv)
- Reproduction cart: [Pokemon Blue](repro_blue.csv)
- GB-CART32K-A: [Tetris](gb_cart32k_tetris.csv)
- GB-CART256K-A: [Tetris](gb_cart256k_tetris.csv)
- GB-CART8M-A: [Tetris](gb_cart8m_tetris.csv), [Wario Land II](gb_cart8m_wario.csv), [Pokemon Blue](gb_cart8m_blue.csv)
- EMS64M: [Tetris](ems64m_tetris.csv), [Wario Land II](ems64m_wario.csv), [Pokemon Blue](ems64m_blue.csv)
- Everdrive GB: [Tetris](everdrive_tetris.csv), [Wario Land II](everdrive_wario.csv), [Pokemon Blue](everdrive_blue.csv)
- Everdrive GB X5: [Tetris](everdrive_x5_tetris.csv), [Wario Land II](everdrive_x5_wario.csv), [Pokemon Blue](everdrive_x5_blue.csv)
- EZ-FLASH Junior: [Tetris](ezflash_tetris.csv), [Wario Land II](ezflash_wario.csv), [Pokemon Blue](ezflash_blue.csv)

## TL;DR

* In these tests, Everdrive GB X5 was the best widely available flash cartridge
* GB-CART8M-A proves a flash cartridge can consume *less power* than a genuine cartridge
* A repro cart can also consume less power than a genuine cartridge. Note: this doesn't mean using repro carts is a good idea, unless you treat the cartridges and your save games as disposable goods
* Typical power consumption ranking (ordered from least consuming to most consuming; EMS64M is not ranked; numbers are based on Pokemon Blue):
  1. GB-CART8M-A (around -5% vs genuine)
  2. Genuine cartridge
  3. Everdrive GB X5 (around +25% vs genuine)
  4. EZ-FLASH Junior (around +75% vs genuine)
  5. Everdrive GB (around +120% vs genuine)
* EMS64M power consumption varies greatly depending on what the ROM on the cartridge is doing, but it seems to always lose to Everdrive GB X5 and more power efficient cartridges
