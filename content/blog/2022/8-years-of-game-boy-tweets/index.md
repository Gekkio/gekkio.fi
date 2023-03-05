+++
title = "8 years of Game Boy tweets"
date = 2022-12-26
+++

Thanks to the "great" effort of Elon Musk, Twitter is in flames and I've suddenly realized all my data there is potentially at risk. During the last 8 years, I've occasionally tweeted about my Game Boy research and projects, so here's an archive of my Game Boy tweets with some extra commentary.

Quick links to each year:

- [2015: Research begins](#2015)
- [2016: First custom hardware to support research](#2016)
- [2017: Hardware tests using GB-BENCH-G1, more discoveries, birth of gb-ctr](#2017)
- [2018: Reverse engineering expanded to decap photo tracing, more custom hardware work](#2018)
- [2019: Discovery that GB uses "SM83 CPU core", being busy with too many GB projects](#2019)
- [2020: SM83 CPU decap photo tracing, various GB schematics, work on better decapping microscope](#2020)
- [2021: SM83 CPU work burnout, focus on better microscope and random GB projects](#2021)
- [2022: More schematics, SM83 CPU core fully reverse engineered](#2022)

<style>
  .tweet {
    display: flex;
  }
  .tweet > * {
    flex: 0 1 auto;
    width: 50%;
    overflow-x: scroll;
  }
  @media only screen and (max-width: 600px) {
    .tweet {
      flex-direction: column;
    }
    .tweet > * {
      width: auto;
    }
  }
</style>

## 2015: Research begins {#2015}

### 2015-01-13

<div class="tweet">

[![Screenshot of the original tweet](2015-01-13.png)](https://twitter.com/gekkio/status/555049610872647680)

> Mooneye GB: A Gameboy emulator written in Rust [link](@/blog/2015/mooneye-gb-a-gameboy-emulator-written-in-rust.md)

</div>

This tweet is the one that started it all: In late 2014 I had started my emulator assuming there was plenty of accurate documentation about the Game Boy. After all, it was a 25 year old game console, so why wouldn't we fully understand it at that point? I quickly realized how wrong I was, and started to research the hardware myself without much knowledge about digital electronics. After a couple of months, the first public commit of Mooneye GB appeared on Github.

Looks like I also didn't know the correct spelling/capitalization of Game Boy at this time. 😅

### 2015-02-14

<div class="tweet">

[![Screenshot of the original tweet](2015-02-14.png)](https://twitter.com/gekkio/status/566611487780003840)

> Mooneye GB: Gameboy cartridge types [link](@/blog/2015/mooneye-gb-gameboy-cartridge-types.md)

</div>

### 2015-05-01

<div class="tweet">

[![Screenshot of the original tweet](2015-05-01.png)](https://twitter.com/gekkio/status/571798737988788225)

> Mooneye GB: Cartridge analysis - Tetris (no MBC) [link](@/blog/2015/mooneye-gb-cartridge-analysis-tetris.md)

</div>

### 2015-05-17

<div class="tweet">

[![Screenshot of the original tweet](2015-05-17.png)](https://twitter.com/gekkio/status/599961326539145217)

> Mooneye GB: Cartridge analysis - Wizards & Warriors X: Fortress of Fear (MBC1) [link](@/blog/2015/mooneye-gb-cartridge-analysis-fortress-of-fear.md)

</div>

### 2015-05-18

<div class="tweet">

[![Screenshot of the original tweet](2015-05-18.png)](https://twitter.com/gekkio/status/600382619809878017)

> Mooneye GB: Cartridge analysis - three games with DMG-BEAN-02 boards [link](@/blog/2015/mooneye-gb-cartridge-analysis-dmg-bean-02.md)

</div>

### 2015-09-13

<div class="tweet">

[![Screenshot of the original tweet](2015-09-13.png)](https://twitter.com/gekkio/status/643077561082347520)

> Dumping the Super Game Boy 2 boot ROM [link](@/blog/2015/dumping-the-super-game-boy-2-boot-rom.md)<br>
> [Attached photo](643077561082347520-COyrojhUYAA-Xmq.jpg)

</div>

This boot ROM dump was pretty exciting for me, because it proved I could perform the dump with fairly primitive tools...at this point I didn't know dumping would be even easier on non-SGB devices using a simpler method.

### 2015-09-27

<div class="tweet">

[![Screenshot of the original tweet](2015-09-27.png)](https://twitter.com/gekkio/status/648117181251764224)

> Mooneye GB 0.1.0 released [link](@/blog/2015/mooneye-gb-0-1-0-released.md)

</div>

Initial (and at the time of writing, the only) release of Mooneye GB 😅 . I was of course planning to release more versions, but at this point I didn't realize research would take all my time and my focus would shift away from actual emulator development.

## 2016: First custom hardware to support research {#2016}

### 2016-03-19

<div class="tweet">

[![Screenshot of the original tweet](2016-03-19.png)](https://twitter.com/gekkio/status/711150351190196224)

> Game Boy cartridge PCB photos [link](@/blog/2016/game-boy-cartridge-pcb-photos.md)

</div>

### 2016-08-05

<div class="tweet">

[![Screenshot of the original tweet](2016-08-05.png)](https://twitter.com/gekkio/status/761667041317314560)

> My rapid Game Boy development cartridge works! &lt;1 s save-compile-flash-reboot-observe cycle on real hardware<br>
> [Attached photo 1](761667041317314560-CpH71AOWIAAIvqG.jpg)<br>
> [Attached photo 2](761667041317314560-CpH71AQWAAA7TFj.jpg)

</div>

GB-LIVE32 v1.0 was very exciting for me! The initial design had some issues but the approach of using a small static RAM chip as the "cartridge ROM" worked, and it made it very quick to update the "ROM" contents leading to quick feedback from real hardware.

### 2016-08-06

<div class="tweet">

[![Screenshot of the original tweet](2016-08-06.png)](https://twitter.com/gekkio/status/761927876266582016)

> Here's a (low-quality gif) video of the rapid development cart <https://gfycat.com/EquatorialCavernousFish> No touching of cables or power switches

</div>

### 2016-10-11

<div class="tweet">

[![Screenshot of the original tweet](2016-10-11.png)](https://twitter.com/gekkio/status/785594988323188736)

> Game Boy test ROM do's and don'ts [link](@/blog/2016/game-boy-test-rom-dos-and-donts.md)

</div>

### 2016-10-17

<div class="tweet">

[![Screenshot of the original tweet](2016-10-17.png)](https://twitter.com/gekkio/status/788100518166032384)

> Finally found a Game Boy with the elusive DMG-CPU C. Just one more CGB CPU version and I have all the GB CPUs for research and testing

</div>

*Narrator's voice*: Unfortunately he didn't realize he'd discover even more GB CPU versions later...

### 2016-10-19

<div class="tweet">

[![Screenshot of the original tweet](2016-10-19.png)](https://twitter.com/gekkio/status/788767892745715712)

> Got the CPU CGB A as well, so I now have a full set of 18 Game Boy CPUs (I don't care about OXY so CPU AGB E is not included)

</div>

### 2016-12-06

<div class="tweet">

[![Screenshot of the original tweet](2016-12-06.png)](https://twitter.com/gekkio/status/806218871749414912)

> Current status: finally working Game Boy hw tools: hw breakpoints, clock edge counts, full signal traces. A treasure trove for research!

</div>

This was another research breakthrough...GB-BENCH made it possible to gather full signal traces of almost all the SoC chip pins, and do much lower level hardware testing than what was previously possible.

### 2016-12-08

<div class="tweet">

[![Screenshot of the original tweet](2016-12-08.png)](https://twitter.com/gekkio/status/806980625374806016)

> Signal trace of running Game Boy Tetris for two seconds...16 million samples, 300 MB Value Change Dump. This is the "light" version :)<br>
> [Attached screenshot](806980625374806016-CzL3r5GWEAAvpxS.jpg)

</div>

### 2016-12-09

<div class="tweet">

[![Screenshot of the original tweet](2016-12-09.png)](https://twitter.com/gekkio/status/806989678041825280)

> Let's zoom in until we can see the single byte read from $0040 when the CPU reads the first instruction of the vblank routine<br>
> [Attached video](806989678041825280-CzMAhU_WEAELTc5.mp4)

</div>

## 2017: Hardware tests using GB-BENCH, more discoveries, birth of gb-ctr {#2017}

### 2017-06-10

<div class="tweet">

[![Screenshot of the original tweet](2017-06-10.png)](https://twitter.com/gekkio/status/873554988945076226)

> Current status: my new hardware setup can trace all 73 digital signals of Game Boy CPU chips. Full tracing@30 kHz, run+trigger@3 MHz

</div>

### 2017-06-18

<div class="tweet">

[![Screenshot of the original tweet](2017-06-18.png)](https://twitter.com/gekkio/status/876445350357282816)

> Brace yourselves...more GB test ROMs are coming. VRAM/OAM accessibility timing for read and write can differ! And it makes sense from hw POV

</div>

<div class="tweet">

[![Screenshot of the original tweet](2017-06-18-2.png)](https://twitter.com/gekkio/status/876479425717698561)

> Like taking candy from a baby<br>
> [Attached screenshot](876479425717698561-DCnhDR-WsAARHSj.jpg)

</div>

In retrospect I was sometimes a bit too proud of finding problems with existing emulators...at some point I realized this and stopped announcing these kind of things and instead just released test ROMs, or preferably released documentation first and tests later.

### 2017-06-30

<div class="tweet">

[![Screenshot of the original tweet](2017-06-30.png)](https://twitter.com/gekkio/status/880696333375610881)

> HW is blocking my research progress ATM...Who knew a system with ~200 loose wires and 5 boards could have noise issues? :P ;) Time for KiCad

</div>

### 2017-07-06

<div class="tweet">

[![Screenshot of the original tweet](2017-07-06.png)](https://twitter.com/gekkio/status/883032145249406976)

> Hmm...using a slow slew rate for the GB clock has fixed my HW issues. I hate magic like this but I'll use this as long as things work :P

</div>

### 2017-07-12

<div class="tweet">

[![Screenshot of the original tweet](2017-07-12.png)](https://twitter.com/gekkio/status/884881227261640704)

> Joined the Rigol DS1000Z owner club. Here's the clock signal from my CPLD to the Game Boy CPU (divided to 1MHz because of noise issues)<br>
> [Attached picture](884881227261640704-DEe06diXgAEjphy.jpg)

</div>

### 2017-07-19

<div class="tweet">

[![Screenshot of the original tweet](2017-07-19.png)](https://twitter.com/gekkio/status/887777372124196868)

> Time to start doing preliminary routing of this monster<br>
> [Attached screenshot](887777372124196868-DFIEhHdXcAEpcLJ.jpg)

</div>

This monster would turn out to be GB-BENCH-G1, the first fully integrated GB-BENCH where everything was on a single board. The previous version (not released as open source) consisted of multiple PCBs and a lot of wiring was required. It worked, but was quite unreliable at times.

### 2017-08-21

<div class="tweet">

[![Screenshot of the original tweet](2017-08-21.png)](https://twitter.com/gekkio/status/899567037923696640)

> Very happy with my first 4-layer board :) (manufactured by Elecrow) Soldering took almost 4 hours (hot air + drag soldering)<br>
> [Attached photo](899567037923696640-DHvkubLXoAE5y4c.jpg)

</div>

### 2017-08-28

<div class="tweet">

[![Screenshot of the original tweet](2017-08-28.png)](https://twitter.com/gekkio/status/902262192631939073)

> Added Lisp scripting to my GB testbench :) I don't even like lisps but it works quite nicely here. Dialect is Ketos: <https://github.com/murarth/ketos>

</div>

### 2017-09-03

<div class="tweet">

[![Screenshot of the original tweet](2017-09-03.png)](https://twitter.com/gekkio/status/904428788565594112)

> Published sources for my GB breakout board v3.0. This version was designed with KiCad <https://github.com/Gekkio/gb-hardware><br>
> [Attached photo](904428788565594112-DI0s9klXUAQxNww.jpg)

</div>

### 2017-09-10

<div class="tweet">

[![Screenshot of the original tweet](2017-09-10.png)](https://twitter.com/gekkio/status/906930836804702208)

> Problem? My problem is that I still don't have all the Game Boys I need ;)<br>
> [Attached photo](906930836804702208-DJYQLVZXcAAIqUk.jpg)

</div>

### 2017-09-19

<div class="tweet">

[![Screenshot of the original tweet](2017-09-19.png)](https://twitter.com/gekkio/status/910225035763306502)

> Oh dear, I've done it again...another test that passes on real hardware but fails on emulators 😈<br>
> [Attached screenshot](910225035763306502-DKHEWF7XUAg7IZ9.jpg)

</div>

### 2017-12-03

<div class="tweet">

[![Screenshot of the original tweet](2017-12-03.png)](https://twitter.com/gekkio/status/937260146006339585)

> New GB hardware test: ei_sequence <https://github.com/Gekkio/mooneye-gb/commit/b61f9c6e8b3d809957846cd932760aa0398e0a3b>

</div>

<div class="tweet">

[![Screenshot of the original tweet](2017-12-03_2.png)](https://twitter.com/gekkio/status/937318109052010497)

> Another new GB hardware test: mbc1/bits_ram_en <https://github.com/Gekkio/mooneye-gb/commit/7e34ea3bde5b1192ee2d6d51b2704764785d60dc>

</div>

### 2017-12-04

<div class="tweet">

[![Screenshot of the original tweet](2017-12-04.png)](https://twitter.com/gekkio/status/937652553222782976)

> It's been on Github for quite some time already, but I think it's time to start actively telling people about the existence of my WIP reference documentation of all GB things: <https://github.com/Gekkio/gb-ctr>

</div>

<div class="tweet">

[![Screenshot of the original tweet](2017-12-04_2.png)](https://twitter.com/gekkio/status/937654134613962752)

> Instead of being copy-paste of existing GB docs, my focus is on accurate and deep technical documentation, especially stuff that can't be found elsewhere. For example, *complete* documentation of MBC1 that covers edge cases as well.

</div>

At this point I was naively hoping more people would read gb-ctr...lack of readers and lack of feedback are the main reasons why I ended up updating gb-ctr rarely.

### 2017-12-05

<div class="tweet">

[![Screenshot of the original tweet](2017-12-05.png)](https://twitter.com/gekkio/status/938103486113304576)

> Looks like either A) GB uses simple pipelining or B) my M-cycle boundaries are wrong. An M-cycle is 4 T-cycles, but I have evidence that opcode decoding happens 3.5 T-cycles after PC is put on the address bus. That would leave only one T-clock edge for the actual instruction

</div>

*Narrator's voice*: Option A would later turn out to be true!

### 2017-12-06

<div class="tweet">

[![Screenshot of the original tweet](2017-12-06.png)](https://twitter.com/gekkio/status/938412089554718720)

> Published sources for my 2015 Game Boy bus conflict test ROM called "naughtyemu.gb": <https://github.com/Gekkio/naughtyemu>. Basic explanation is in this forum post: <https://forums.nesdev.org/viewtopic.php?f=20&t=16796&p=209596#p209596>

</div>

### 2017-12-11

<div class="tweet">

[![Screenshot of the original tweet](2017-12-11.png)](https://twitter.com/gekkio/status/940235979117547521)

> Going to talk at @Disobey_fi about Game Boy reverse engineering. The original GB launched in 1989 (almost 30 years ago) and a lot of RE work has been done, but we still keep finding behaviour and edge cases not covered by existing docs or emulators. [disobey.fi/#program](https://disobey.fi)

</div>

This was going to be a big public talk in front of a fairly large audience...very intimidating to an introvert like me, but I couldn't pass the opportunity, even as an inexperienced public speaker!

## 2018: Reverse engineering expanded to decap photo tracing, more custom hardware work {#2018}

### 2018-01-05

<div class="tweet">

[![Screenshot of the original tweet](2018-01-05.png)](https://twitter.com/gekkio/status/949236843933036544)

> Finished tracing all the signal pins in this DMG-CPU B decap photo.
> Yes, there will eventually be an interactive viewer with toggling/coloring of signals ;)
>
> (Decap photo CC BY 4.0 digshadow / <https://siliconpr0n.org>)<br>
> [Attached picture 1](949236843933036544-DSxdKR0WAAAFix5.jpg)<br>
> [Attached picture 2](949236843933036544-DSxdLAUWsAUBcxf.jpg)<br>
> [Attached picture 3](949236843933036544-DSxdMEYW4AAfjNt.jpg)

</div>

*Narrator's voice*: Sadly an interactive viewer was never created...

<div class="tweet">

[![Screenshot of the original tweet](2018-01-05_2.png)](https://twitter.com/gekkio/status/949372419327881219)

> Here's a version of the earlier picture with pin labels added<br>
> [Attached picture](949372419327881219-DSzYoeoX0AAAhGP.jpg)

</div>

### 2018-01-08

<div class="tweet">

[![Screenshot of the original tweet](2018-01-08.png)](https://twitter.com/gekkio/status/950444423242043393)

> Looks like info about "corrupted STOP" on GB is nonsense. The next byte is simply skipped instead of some values being "corrupted". Yes, it still makes sense to put a NOP there, but the justification in current docs for this seems wrong

</div>

<div class="tweet">

[![Screenshot of the original tweet](2018-01-08_2.png)](https://twitter.com/gekkio/status/950478077871652864)

> "A wild STOPHALT bug appeared!"...so it turns out that executing STOP *while already pressing a button* doesn't do STOP but a different version of HALT. And yes, the HALT bugs are also present here but in a weird way

</div>

### 2018-01-30

<div class="tweet">

[![Screenshot of the original tweet](2018-01-30.png)](https://twitter.com/gekkio/status/958397607839260675)

> Ugh... GB bench v1 has 3 separate power rails and it wasn't easy to design the board and route it. In v2 I've got 6 power rails so far in the design from just following datasheet recommendations :O challenge accepted :)

</div>

### 2018-02-04

<div class="tweet">

[![Screenshot of the original tweet](2018-02-04.png)](https://twitter.com/gekkio/status/960103260781727744)

> Here's my GB talk from Disobey :D the fine details section has some errors, but I'll write an errata blog post soon to point out the errors

</div>

<div class="tweet">

[![Screenshot of the original tweet](2018-02-04_2.png)](https://twitter.com/gekkio/status/960235856849227777)

> The full video of my GB talk from Disobey 2018 is now available :) the last 10 minutes were missing in the earlier upload. Remember that the "fine details" part has some errors, so wait for my errata blog post before fixing your emulator ;) https://twitter.com/Disobey_fi/status/960221371619045377

</div>

Despite being nervous at first, the talk went well and I'm very happy about the whole thing!

### 2018-02-06

<div class="tweet">

[![Screenshot of the original tweet](2018-02-06.png)](https://twitter.com/gekkio/status/960635715041275904)

> Errata blog post for my GB talk is now available. The last section (="fine details") had some wrong clock edges, although the main points are still valid and remain the same [link](@/blog/2018/errata-for-reverse-engineering-fine-details-of-game-boy-hardware.md)

</div>

### 2018-02-27

<div class="tweet">

[![Screenshot of the original tweet](2018-02-27.png)](https://twitter.com/gekkio/status/968543728100093952)

> THE TIME FOR HIDE AND SEEK IS OVER, MR CHIP. I FOUND YOU!
>
> Soooo, once again I can say that I've got all the known GB CPU versions :)<br>
> [Attached photo](968543728100093952-DXD0yyTX4AMJ3J-.jpg)

</div>

### 2018-03-15

<div class="tweet">

[![Screenshot of the original tweet](2018-03-15.png)](https://twitter.com/gekkio/status/974183960845672449)

> Discovered a new hw technique yesterday: I can now read/write GB hw registers freely in my test bench, so I can read stuff like PPU registers at *one clock edge accuracy*. This is *huge*!!
>
> Screenshot 1: scanline LY + modes<br>
> Screenshot 2: mode 1 / line 144<br>
> [Attached screenshot 1](974183960845672449-DYT9f6VXUAAK5Lm.jpg)<br>
> [Attached screenshot 2](974183960845672449-DYT9obaXcAAxmbh.jpg)

</div>

### 2018-03-18

<div class="tweet">

[![Screenshot of the original tweet](2018-03-18.png)](https://twitter.com/gekkio/status/975409992688861184)

> New GB test ROM: acceptance/ppu/stat_lyc_onoff
>
> You know the drill...it passes on all real hardware versions and fails in every emulator I tested (including mine) :)<br>
> [Attached screenshot](975409992688861184-DYlS9QGW4AA2qLQ.jpg)

</div>

### 2018-03-24

<div class="tweet">

[![Screenshot of the original tweet](2018-03-24.png)](https://twitter.com/gekkio/status/977530749934063621)

> GB research is on hold for this weekend because I'm looking for secret lost GB hardware documents in the Alps. Haven't found any yet but I'll keep looking! 😜 next week: PPU interrupt and OAM DMA conflict tests + docs in gbctr<br>
> [Attached photo](977530749934063621-DZDjA73WkAAQyMp.jpg)

</div>

### 2018-03-27

<div class="tweet">

[![Screenshot of the original tweet](2018-03-27.png)](https://twitter.com/gekkio/status/978585482786492417)

> I'll be doing an updated version of my recent talk about GB reverse engineering at the next Reaktor Meetup.
>
> There's still a couple of spots left, so enroll now if you are in Helsinki next Tuesday and are interested in three hardware-focused talks:
>
> <https://www.meetup.com/reaktor-events-helsinki/events/248991039>

</div>

### 2018-04-01

<div class="tweet">

[![Screenshot of the original tweet](2018-04-01.png)](https://twitter.com/gekkio/status/980442995110678528)

> Now I'm pretty sure the glop top DMG CPU is the B version.
>
> Left: DMG-CPU B (© Digshadow/siliconpr0n.org)<br>
> Right: glop top decap by me
>
> The die took a lot of damage, but the "L20A" part of "CESL20A" is IMHO clearly visible.<br>
> [Attached photo](980442995110678528-DZs6IUFXUAAKy3C.jpg)

</div>

This was an important discovery: the glop top chips were not inherently unique, but were simply repackaged B and C revisions. The revision is even indicated on the board, which is obvious in hindsight 😄

### 2018-04-26

<div class="tweet">

[![Screenshot of the original tweet](2018-04-26.png)](https://twitter.com/gekkio/status/989590390473977863)

> I'll be speaking about Game Boy reverse engineering at @ReaktorBP on May 24th. My talk includes live hw demos and some newly discovered hw details :D
>
> There's a lot of exciting talks at the event, so check out the program and get your tickets here: [reaktorbreakpoint.com](https://reaktorbreakpoint.com)

</div>

### 2018-05-03

<div class="tweet">

[![Screenshot of the original tweet](2018-05-03.png)](https://twitter.com/gekkio/status/992096966925467648)

> Finally received my shipment of 50 Game Boy link ports. Gonna use several for, uh, a project ;) Now I just need to create a couple of new KiCad symbols+footprints, design a PCB and write some VHDL...

</div>

*Narrator's voice*: Unfortunately these link ports would remain in storage, because he ended up focusing on too many other projects...

### 2018-05-05

<div class="tweet">

[![Screenshot of the original tweet](2018-05-05.png)](https://twitter.com/gekkio/status/992706504800264192)

> Another day, another board :) This is just an update to my old GB-LIVE32 board, but it's an important stepping stone to something bigger...<br>
> [Attached screenshot](992706504800264192-DcbMDJ0X4AEV8qI.jpg)

</div>

### 2018-05-11

<div class="tweet">

[![Screenshot of the original tweet](2018-05-11.png)](https://twitter.com/gekkio/status/994892528049643520)

> Finally found hard evidence that the GB CPU has a 2-stage pipeline (or "prefetch"). An important find for understanding true timing of hardware traces and some behaviours. I'll present some details and consequences in my Reaktor Breakpoint presentation in two weeks :)

</div>

### 2018-05-14

<div class="tweet">

[![Screenshot of the original tweet](2018-05-14.png)](https://twitter.com/gekkio/status/996102947233828864)

> It's going to require a lot of effort to have Game Boy Pocket and Game Boy Color CPU support in my test bench system, but this is how it starts: desoldering CPU chips for upcoming test bench boards. (also in picture: various support chips)<br>
> [Attached photo](996102947233828864-DdLdXBeW0AECQca.jpg)

</div>

### 2018-05-27

<div class="tweet">

[![Screenshot of the original tweet](2018-05-27.png)](https://twitter.com/gekkio/status/1000836098371842049)

> Spent a lot of time today desoldering and measuring all components from this poor corroded Game Boy Pocket board. Loose 0603s are a pain to probe, but I only managed to lose one component. Goodbye C35, you will be missed.
>
> Same unit before desoldering: <https://gbhwdb.gekkio.fi/consoles/mgb/MH12129596.html><br>
> [Attached photo](1000836098371842049-DeOtTuBX0AIK7fE.jpg)

</div>

### 2018-06-06

<div class="tweet">

[![Screenshot of the original tweet](2018-06-06.png)](https://twitter.com/gekkio/status/1004453394508079104)

> 10+ hours of USB debugging has finally paid off: my GB-LIVE32 rapid development cart v2.0 is now much more reliable than its predecessor. This time I've polished things a lot, so everything will be open sourced (KiCad design, PIC18F firmware, Rust lib+CLI app).<br>
> [Attached photo](1004453394508079104-DfCH-9sX0AEVhnR.jpg)

</div>

GB-LIVE32 v2.0 would turn out to be a true workhorse for hardware testing! I even gave some to other people so they could run tests much easier and faster.

### 2018-07-08

<div class="tweet">

[![Screenshot of the original tweet](2018-07-08.png)](https://twitter.com/gekkio/status/1015721966483988481)

> Getting ready to start routing this little guy...if this works out, it means I can create a working MAX 10 FPGA design with some high speed IO included. And that is the road to GB-BENCH v2 with new stuff like audio capture and Game Boy Color CPU support<br>
> [Attached photo](1015721966483988481-DhiEtMhWAAEUB0j.jpg)

</div>

This turned out to be too ambitious...in 2022 GB-BENCH v2 still hasn't been completed, and I've iterated various different designs without actually building anything.

### 2018-07-11

<div class="tweet">

[![Screenshot of the original tweet](2018-07-11.png)](https://twitter.com/gekkio/status/1017149896674234368)

> Here's a (very) rough demo video of my GB-LIVE32 v2.0 rapid development cartridge:
>
> <https://www.youtube.com/watch?v=GCIcgmga9Mo>
>
> Now fully open source!
>
> KiCad/gerbers: <https://github.com/gekkio/gb-hardware><br>
> Firmware/software: <https://github.com/gekkio/gb-live32>

</div>

### 2018-08-27

<div class="tweet">

[![Screenshot of the original tweet](2018-08-27.png)](https://twitter.com/gekkio/status/1034157871372484608)

> I've got two valid excuses for doing slightly less GB things recently:
>
> 1. The parcel with new GB-BENCH control PCBs still hasn't arrived and tracking says it's been stuck at the Helsinki airport for two weeks now 😢<br>
> 2. I started playing Danganronpa and am completely hooked 😇

</div>

### 2018-09-11

<div class="tweet">

[![Screenshot of the original tweet](2018-09-11.png)](https://twitter.com/gekkio/status/1039588344706093057)

> Ok looks like I've managed to confirm my first finding of temperature-dependent behaviour on Game Boy hardware :D now emulators just need to add support for temperature sensors and/or a temperature slider in the UI.......

</div>

### 2018-11-04

<div class="tweet">

[![Screenshot of the original tweet](2018-11-04.png)](https://twitter.com/gekkio/status/1058851052475334656)

> TIL:
> a Game Boy and 2 games in hand luggage is normal.<br>
> 3 Game Boys and 6 games in hand luggage gets you "Sir, you've got a lot of electronics in your bag" and a bag search at the airport security :D
>
> (not complaining...I'm sure it looks a bit unusual :P)

</div>

### 2018-11-13

<div class="tweet">

[![Screenshot of the original tweet](2018-11-13.png)](https://twitter.com/gekkio/status/1062412348349136897)

> Current status: experimenting with different approaches to writing a parser that can identify chips on GB cartridge boards based on the chip labels<br>
> [Attached video](1062412348349136897-Dr5xmWsW4AExhpl.mp4)

</div>

Spoiler: regex won 😄. My GB hardware database site would eventually switch to regexes to parse chip information from labels.

## 2019: Discovery that GB uses "SM83 CPU core", being busy with too many GB projects {#2019}

### 2019-01-06

<div class="tweet">

[![Screenshot of the original tweet](2019-01-06.png)](https://twitter.com/gekkio/status/1081706992882847745)

> I'm entirely convinced that the original GB CPU chip uses a Sharp SM83 CPU core. And there are public datasheets of some chips that use the same core....😍

</div>

This was a huge discovery and perhaps even a historical moment in GB research...I think I was searching some datasheet archive for Sharp, STOP, and HALT, and randomly stumbled upon some SM83xx SoC datasheet. After staring at it for a while, I realized the instruction set looked suspiciously familiar, and started to investigate more. Eventually I realized it was a perfect match for the GB CPU core.

### 2019-01-13

<div class="tweet">

[![Screenshot of the original tweet](2019-01-13.png)](https://twitter.com/gekkio/status/1084391449087655936)

> One more thing about SM83 CPU core: it's possible GB is not exactly SM83 but just *SM83-compatible*...there might be an older ancestor (a bit like 6502 vs 65C02). In 1986 data book there's SM-812/SM-813 with the same reported instruction count as SM8311/SM8320...but no details

</div>

I can't emphasize this enough...SM83 is still the best guess, but personally I still suspect GB SoCs might have the unnamed predecessor.

### 2019-01-14

<div class="tweet">

[![Screenshot of the original tweet](2019-01-14.png)](https://twitter.com/gekkio/status/1084572996868677632)

> Not looking forward to soldering this beast 😓 the schematic isn't even ready yet, so there will be more capacitors<br>
> [Attached screenshot](1084572996868677632-Dw0sZazXQAAePgm.jpg)

</div>

Yet another GB-BENCH v2 attempt that would turn out to be a waste of time...

### 2019-06-01

<div class="tweet">

[![Screenshot of the original tweet](2019-06-01.png)](https://twitter.com/gekkio/status/1134568927210684416)

> Internal primary 8-bit data bus of the Game Boy DMG-CPU B chip visualized<br>
> [Attached screenshot](1134568927210684416-D77L5qqXYAIntX-.jpg)

</div>

### 2019-06-07

<div class="tweet">

[![Screenshot of the original tweet](2019-06-07.png)](https://twitter.com/gekkio/status/1137068368983396353)

> Time to write some VHDL for this monster :D<br>
> [Attached photo](1137068368983396353-D8etpe6WkAEM0tH.jpg)

</div>

I still use GB-CARTPP Pro (known as just GB-CARTPP at the time), because it's crazy fast and reliable. I'm very happy about this little device, even though v1.0 had some design issues that needed some ugly bodges.

### 2019-06-19

<div class="tweet">

[![Screenshot of the original tweet](2019-06-19.png)](https://twitter.com/gekkio/status/1141447103740284930)

> Experimenting with Ghidra and Game Boy ROM reverse engineering...there's no official support for GB but my custom language support files work already surprisingly well<br>
> [Attached screenshot](1141447103740284930-D9c69Y8WwAc3cYf.jpg)

</div>

This would become GhidraBoy a bit later, and would become my primary tool for GB ROM reverse engineering.

### 2019-06-23

<div class="tweet">

[![Screenshot of the original tweet](2019-06-23.png)](https://twitter.com/gekkio/status/1142792866814746624)

> I shall call this "art piece" The Twins
>
> Got some soldering to do during the holidays 😁<br>
> [Attached screenshot](1142792866814746624-D9wC8pDWsAYWyqh.jpg)

</div>

Sadly both twins didn't survive very long...I got the PCBs and soldered everything, but both designs had too many issues and I ended up scrapping them.

### 2019-07-15

<div class="tweet">

[![Screenshot of the original tweet](2019-07-15.png)](https://twitter.com/gekkio/status/1150803080314798080)

> My FPGA-based GB cartridge dumper can now dump a Tetris cart ROM in ~40 ms. It's overkill, but I'm practicing using FT232H USB chip's FT245 sync mode (~40 MB/s half-duplex, but limited here to ~15 MB/s at the moment, because pipelining in my VHDL code isn't yet perfect)

</div>

### 2019-07-17

<div class="tweet">

[![Screenshot of the original tweet](2019-07-17.png)](https://twitter.com/gekkio/status/1151475649359601664)

> Time required to dump Densha De Go 2 ROM (largest Game Boy game, 8MB ROM):
>
> GB01 (a polished-looking cartridge reader you can buy): 5 min 30 s<br>
> GB-CARTPP (my not-so-beautiful device): 10 s
>
> And I still have two performance tricks left that I can do with the FPGA 😊 target is <5 s

</div>

### 2019-07-18

<div class="tweet">

[![Screenshot of the original tweet](2019-07-18.png)](https://twitter.com/gekkio/status/1151883272496013314)

> Improved the hardware timings, so now I can dump Densha De Go 2 in **2.1s**. However, this is with "overdriven" timings so it's not a good idea in normal use. Perfectly compatible timings give 5.1s, which is still a good result<br>
> [Attached screenshot](1151883272496013314-D_xNxBHXsAAhKdN.jpg)

</div>

### 2019-07-26

<div class="tweet">

[![Screenshot of the original tweet](2019-07-26.png)](https://twitter.com/gekkio/status/1154832167836553216)

> Published my Game Boy extension for the Ghidra reverse engineering framework:
>
> <https://github.com/Gekkio/GhidraBoy>
>
> It can be used for both cartridge ROM and boot ROM disassembly / reverse engineering

</div>

### 2019-08-03

<div class="tweet">

[![Screenshot of the original tweet](2019-08-03.png)](https://twitter.com/gekkio/status/1157408978382610438)

> Prebuilt GhidraBoy release zips are now available for both Ghidra 9.0.4 and 9.1-DEV (latest Ghidra git master) <https://github.com/Gekkio/GhidraBoy>

</div>

### 2019-10-21

<div class="tweet">

[![Screenshot of the original tweet](2019-10-21.png)](https://twitter.com/gekkio/status/1186380074280468480)

> I've been working tirelessly to go through and fully understand the recently released amazing Game Boy schematics by @Furrtek. Still got plenty of work, but here's simulation results of some bus accesses that match real hardware. Automatic VHDL generation from KiCad helps 😀<br>
> [Attached screenshot](1186380074280468480-EHbeY3JWkAEEs4G.png)

</div>

Furrtek's release was groundbreaking! I was slightly annoyed about how much time I had personally spent on DMG-CPU B SoC tracing that was now unnecessary, but having full schematics meant a chance to make great progress with improving low-level understanding of the SoC. The only problem was that Furrtek's schematics didn't include the CPU core, and there were quite a lot of mistakes. I couldn't get even the first page to simulate correctly, so I ended up redoing a lot of the work and making my own schematics.

### 2019-11-04

<div class="tweet">

[![Screenshot of the original tweet](2019-11-04.png)](https://twitter.com/gekkio/status/1191416558972817409)

> I've released GhidraBoy 20191104, which has been tested to work with the recently released Ghidra 9.1 release
>
> <https://github.com/Gekkio/GhidraBoy/releases/tag/20191104_ghidra_9.1>

</div>

### 2019-11-21

<div class="tweet">

[![Screenshot of the original tweet](2019-11-21.png)](https://twitter.com/gekkio/status/1197273506423197697)

> It's just Tetris, right?
>
> ...this image was generated by a low-level 11kloc VHDL simulation model consisting of 1200+ DMG-CPU B standard cells almost entirely generated from KiCad schematics.
>
> Simulating ~20ms took ~40s of real time and generated a 250MB signal dump file.<br>
> [Attached screenshot](1197273506423197697-EJ2R5_-W4AAYyqQ.png)

</div>

Just one month later after acknowledging Furrtek's amazing work, I had my own WIP schematics simulating Tetris correctly. Unfortunately my approach was getting more and more complicated and error-prone, and this would end up being the best I could do for a while.

## 2020: SM83 CPU decap photo tracing, various GB schematics, work on better decapping microscope {#2020}

### 2020-02-07

<div class="tweet">

[![Screenshot of the original tweet](2020-02-07.png)](https://twitter.com/gekkio/status/1225901940904808449)

> SM83 CPU core tracing progress...unfortunately currently available decap photos are not good enough for much more. But I'm surprised how much one can learn from just looking at how things are connected. For example, the register file has more buses than one might expect.<br>
> [Attached screenshot](1225901940904808449-EQNC7iNX0AAbkAh.jpg)

</div>

After getting frustrated with the inability to run test ROMs on the DMG-CPU B HDL model, I decided to try to reverse engineer the CPU core.

### 2020-02-19

<div class="tweet">

[![Screenshot of the original tweet](2020-02-19.png)](https://twitter.com/gekkio/status/1230202377229209601)

> GhidraBoy has been updated and the latest release is compatible with Ghidra 9.1.2 🎉
>
> <https://github.com/Gekkio/GhidraBoy/releases/tag/20200219_ghidra_9.1.2>

</div>

### 2020-03-15

<div class="tweet">

[![Screenshot of the original tweet](2020-03-15.png)](https://twitter.com/gekkio/status/1239214486424301570)

> Here's DMG-AMP IR3R40 (manufactured by Sharp), the amplifier chip from the original Game Boy<br>
> [Attached photo](1239214486424301570-ETKSxeBWkAISzFo.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-03-15_2.png)](https://twitter.com/gekkio/status/1239280360124567554)

> Here's DMG-AMP and F411A under higher magnification. I don't have a motorized XY stage so everything was done manually. Luckily Microsoft ICE worked much better than I expected and managed to stitch the photos fairly well.<br>
> [Attached photo](1239280360124567554-ETLLJ_SXkAAYh0h.jpg)
>
> Max resolution photos are here:<br>
> <https://gekkio.fi/files/decapped-chips/AM4515ZT4/>

</div>

### 2020-03-28

<div class="tweet">

[![Screenshot of the original tweet](2020-03-28.png)](https://twitter.com/gekkio/status/1243887873683869696)

> Better tools -> better chip decap photos.<br>
> This is the same magnified part of the DMG-AMP chip die taken with my old tools and new tools for comparison.<br>
> [Attached photo 1](1243887873683869696-EUMsrQhXkAAgXsH.jpg)<br>
> [Attached photo 2](1243887873683869696-EUMsrQoX0AIbXJm.jpg)

</div>

I finally had decent tooling for decapping, although without a motorized stage I was limited to small chips or small areas of large chips...certainly usable for the SM83 CPU core!

### 2020-05-07

<div class="tweet" id="tweet-1258483113023373318">

[![Screenshot of the original tweet](2020-05-07.png)](https://twitter.com/gekkio/status/1258483113023373318)

> This cell is my reverse engineering mystery of today...behaviour suggests it could be AND gate. But note how In2 only goes to a gnd-side NMOS, so the input side looks almost like Pseudo-NMOS NAND with 2x NMOS in series. But In1 also has the complementary PMOS near vdd-side (?!)<br>
> [Attached photo](1258483113023373318-EXcGBd0X0AQ4RIO.png)

</div>

<div class="tweet" id="tweet-1258498108297752581">

[![Screenshot of the original tweet](2020-05-07_2.png)](https://twitter.com/gekkio/status/1258498108297752581)

> Here's how I see it at the moment...black rectangles are the transistors. Seems like an AND gate but In2 PMOS is missing. The yellow signal also has one unexplained via that seems to be connected to diffusion area going up towards gnd, but obscured by the green signal metal<br>
> [Attached photo](1258498108297752581-EXcUeb4WsAAE_oE.png)

</div>

### 2020-05-09

<div class="tweet">

[![Screenshot of the original tweet](2020-05-09.png)](https://twitter.com/gekkio/status/1259135507214327808)

> Abstract art, or fully traced Game Boy SM83 CPU core instruction decoding 1st stage? You decide...
>
> In: 8-bit instruction register + 3-bit seq counter + "in CB mode" flag + "in interrupt dispatch" flag<br>
> Out: 107 control signals, 3 seem to be always low<br>
> Uses dynamic domino logic [Attached photo](1259135507214327808-EXlWaWdXgAInMny.jpg)

</div>

### 2020-05-27

<div class="tweet">

[![Screenshot of the original tweet](2020-05-27.png)](https://twitter.com/gekkio/status/1265706867352797185)

> This is what a fully traced Game Boy Pocket mainboard looks like :D<br>
> ...<br>
> ...<br>
> ...<br>
> And here are the schematics!<br>
> <https://github.com/gekkio/gb-schematics><br>
> [Attached photo](1265706867352797185-EZCw3tNXkAcUUgZ.jpg)

</div>

My first GB schematics release! A lot of work, but I really enjoyed it and ended up reverse engineering much more GB hardware and releasing more schematics.

### 2020-06-14

<div class="tweet">

[![Screenshot of the original tweet](2020-06-14.png)](https://twitter.com/gekkio/status/1272167835876446210)

> GB SM83 CPU core I/O cell reverse engineered. One surprise about the CPU core is how much dynamic logic and precharging it uses. Even the main SoC data bus (EXT_DATA) has precharge circuitry and the CPU core only uses a low-side driver (but SoC peripherals are proper push/pull)<br>
> [Attached screenshot](1272167835876446210-EaejU6wXQAIIC9m.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-06-14_2.png)](https://twitter.com/gekkio/status/1272215638883393538)

> Some more info and the Inkscape SVG is now here: <https://github.com/Gekkio/sm83-research>
>
> I've got a lot more details about SM83 coming soon™, including new info about the register file and the various (and plentiful) 8-bit buses internal to the CPU core.<br>
> Also: simulation-tested HDL code

</div>

Much later in 2022 when finishing my full RE work on the SM83 CPU core, I was very surprised that I got all the important details right at this point! The locations of individual transistors were sometimes guesses and were not perfectly correct, but I didn't miss any transistors or misunderstand the behaviour.

### 2020-06-19

<div class="tweet">

[![Screenshot of the original tweet](2020-06-19.png)](https://twitter.com/gekkio/status/1273971586937360384)

> Ummm...yeah sure, Microsoft Image Composite Editor, that's exactly what the chip die looks like. Good job! Well stitched!<br>
> [Attached screenshot](1273971586937360384-Ea4NdXIXsAIbjio.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-06-19_2.png)](https://twitter.com/gekkio/status/1273972804216664064)

> It managed to stitch this 10x objective photo correctly, but at 40x there seems to be too much repetition and not enough information for it to infer the layout correctly :(<br>
> [Attached screenshot](1273972804216664064-Ea4O94lX0AECQfy.jpg)

</div>

### 2020-06-20

<div class="tweet">

[![Screenshot of the original tweet](2020-06-20.png)](https://twitter.com/gekkio/status/1274427461225402368)

> Here's a "handy" guide to some Game Boy MBC3B memory bank controller chip standard cells<br>
> [Attached screenshot](1274427461225402368-Ea-s3ijWAActLgL.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-06-20_2.png)](https://twitter.com/gekkio/status/1274428892548300804)

> And no, there's no ARM microcontroller on the chip

</div>

Sadly I don't think many people understood this pun... 😭

### 2020-06-29

<div class="tweet">

[![Screenshot of the original tweet](2020-06-29.png)](https://twitter.com/gekkio/status/1277675285069148160)

> What exactly are you implying, FJWC?? 🤨🧐<br>
> ...<br>
> FJWC=(NOT nSHDN) OR (nWR)<br>
> In other words, FJWC=nWR when nSHDN=1, and FJWC=1 when nSHDN=0. Turns out nSHDN isolates pins (like Lattice Power Guard / Xilinx DataGATE), so this extra gating is needed to keep nWR safely deasserted<br>
> [Attached screenshot](1277675285069148160-Ebszbo1WkAMGRnB.jpg)

</div>

### 2020-07-22

<div class="tweet">

[![Screenshot of the original tweet](2020-07-22.png)](https://twitter.com/gekkio/status/1285952815362383873)

> Aaaaand nope, I don't think I'll capture a full set of photos of a decapped CPU CGB B chip die, since stitching is a nightmare as usual and I'll go mad before getting it to work with a chip this large. People with motorized XY(Z) stages don't know how lucky they are<br>
> [Attached screenshot 1](1285952815362383873-EdiekklWsAETEJ4.jpg)<br>
> [Attached screenshot 2](1285952815362383873-EdielU_WsAA15B9.jpg)

</div>

### 2020-08-06

<div class="tweet">

[![Screenshot of the original tweet](2020-08-06.png)](https://twitter.com/gekkio/status/1291426842038153216)

> Decapped an SGB-CPU 01 chip to capture some Game Boy SM83 CPU core photos with 40x magnification + EDF. Can *you* tell the difference between left (from [siliconpr0n.org](https://siliconpr0n.org), 20x I think?) and right (mine, 40x + EDF)? 😎<br>
> [Attached screenshot](1291426842038153216-EewRFf-WoAAeAx-.png)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-08-06_2.png)](https://twitter.com/gekkio/status/1291429988323950597)

> The previous photos were of an IO cell. Here's a piece of the ALU<br>
> [Attached screenshot](1291429988323950597-EewUi5xXoAAs4Nf.png)

</div>

### 2020-08-09

<div class="tweet">

[![Screenshot of the original tweet](2020-08-09.png)](https://twitter.com/gekkio/status/1292206670710480896)

> Finally figured out this mystery cell used in the Game Boy SM83 CPU core [link to tweet](#tweet-1258483113023373318)
>
> It's just an SR latch (with reset signal prioritized) but unusual because S and R have opposite polarities.
>
> Truth table:<br>
> nR  S   Q<br>
> 0    0   0<br>
> 0    1   0<br>
> 1    0   held<br>
> 1    1   1<br>

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-08-09_2.png)](https://twitter.com/gekkio/status/1292211341000876032)

> I almost had it figured out here: [link to tweet](#tweet-1258498108297752581)
>
> Yellow is inverted and output to green, but the previously missing part is another inverter (2 transistors)! Green is also inverted and output to yellow, creating a cross-coupled inverter loop that makes the cell a latch

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-08-09_3.png)](https://twitter.com/gekkio/status/1292212531340214280)

> Here's a higher resolution photo of the damn thing...
>
> "bastard_gate.jpg"<br>
> [Attached photo](1292212531340214280-Ee7b9nIXkAcIxDi.jpg)

</div>

### 2020-08-22

<div class="tweet">

[![Screenshot of the original tweet](2020-08-22.png)](https://twitter.com/gekkio/status/1297197932429619200)

> Here's something I started writing 4 years ago...I wrote it because most reviews of Game Boy mods/parts focus on ease of installation and not on the technical side
>
> "HHL Bivert Module V2 - technical review" a.k.a "how hard can it be to invert two signals"<br>
> [link](@/blog/2020/hhl-bivert-v2-technical-review/index.md)

</div>

### 2020-10-16

<div class="tweet">

[![Screenshot of the original tweet](2020-10-16.png)](https://twitter.com/gekkio/status/1317205752608624641)

> After another evening of lovely reverse engineering work, I proudly present the first publicly available schematics of Game Boy Advance SP console.
>
> (this is for AGS-001 mainboard revision AGS-CPU-11...other versions have some differences)
>
> <https://github.com/Gekkio/gb-schematics#game-boy-advance-sp-ags-001-mainboard-ags-cpu-11><br>
> [Attached screenshot](1317205752608624641-EkencqXXIAEDrM_.jpg)

</div>

### 2020-11-13

<div class="tweet">

[![Screenshot of the original tweet](2020-11-13.png)](https://twitter.com/gekkio/status/1327011528084774912)

> Earlier this year I reverse-engineered stage 1 of the Game Boy SM83 CPU core decoding logic. I think it's time to start working on stage 2 😎<br>
> Not really looking forward to stage 3, which is the largest one.<br>
> [Attached screenshot](1327011528084774912-Emp7CqDXEAI3ust.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-11-13_2.png)](https://twitter.com/gekkio/status/1327012903858434048)

> The goal is to generate a lot of control signals depending on the opcode in the IR register and a couple of system state signals.<br>
> Instead of simple and clean grid-like structure, all stages use pass transistors and surprisingly complicated diffusion layer to do both AND/OR logic.

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-11-13_3.png)](https://twitter.com/gekkio/status/1327014498725748738)

> For example, this blue column is a stage 1 output I call OP_NOP_STOP_S0XX. Purple "taps" are pass transistor gate inputs, horizontal lines are the inputs. If all pass transistors conduct, an electrical path is formed between top and bottom ends of the column (ground and output).<br>
> [Attached screenshot](1327014498725748738-Emp_YkmXcAAk-lA.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-11-13_4.png)](https://twitter.com/gekkio/status/1327015222532517888)

> Dynamic logic is used, so in one clock phase, the ground in the top end is always disconnected and the output is precharged to 1. In the other clock phase, the ground is available and the column may pull its output low.
>
> Here's a VHDL implementation of this column.<br>
> [Attached screenshot](1327015222532517888-EmqAwUyWEAEvVlg.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-11-13_5.png)](https://twitter.com/gekkio/status/1327016906382045187)

> Doesn't look that bad, right? Well, that was a simple case 😏<br>
> The blue "column" can be much more complex, and multiple outputs share some parts.
>
> Here's 3 outputs based on a complicated shared diffusion layer structure with branching:<br>
> OP_LD_X_N<br>
> OP_LD_X_N_SX00<br>
> OP_LD_R_N_SX01<br>
> [Attached screenshot](1327016906382045187-EmqCFxOXcAEY71m.png)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-11-13_6.png)](https://twitter.com/gekkio/status/1327018976937906176)

> Remember, all that matters is creating a path to ground! So the three parallel mini columns basically form a NOR3.<br>
> Here's the VHDL 😅<br>
> Note that this code intentionally matches the original structure, and the same logic could be written in a simpler way without branching/sharing. <br>
> [Attached screenshot](1327018976937906176-EmqDWL0XcAYX4E8.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-11-13_7.png)](https://twitter.com/gekkio/status/1327356800669261824)

> Ghidra 9.2 has finally been released and I've also released a new version of GhidraBoy freshly built for Ghidra 9.2 🎉
>
> <https://github.com/Gekkio/GhidraBoy/releases/tag/20201113_ghidra_9.2>

</div>

### 2020-11-17

<div class="tweet">

[![Screenshot of the original tweet](2020-11-17.png)](https://twitter.com/gekkio/status/1328787565143592966)

> Took me more than 30 minutes to spot one error in the traced blue areas in Game Boy SM83 CPU core stage 1 decoder. Can *you* spot the mistake?😏
>
> One challenge with stage 2 RE is that even small mistakes in stage 1 propagate and lead to great chaos and confusion in stage 2<br>
> [Attached screenshot](1328787565143592966-EnDKXZNUwAATnNe.jpg)

</div>

### 2020-11-19

<div class="tweet">

[![Screenshot of the original tweet](2020-11-19.png)](https://twitter.com/gekkio/status/1329188003483430913)

> All done with Game Boy SM83 CPU core decoder stage 2! Simple simulation gave sensible control signals, although there's definitely some mistakes left here (and in stage 1 too!). More CPU core areas are needed for thorough testing...
>
> Photo shows stage 2 before vs after tracing<br>
> [Attached screenhot](1329188003483430913-EnI4XsbXEAUSR1Q.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-11-19_2.png)](https://twitter.com/gekkio/status/1329195506027929616)

> I've published the Inkscape SVG here:
>
> <https://github.com/Gekkio/sm83-research>
>
> Note that the signal names are still based on "educated guesswork" and might be incorrect and/or misleading.
>
> ...and yes, I know stage 1 is still missing from the repository 😅

</div>

### 2020-12-10

<div class="tweet">

[![Screenshot of the original tweet](2020-12-10.png)](https://twitter.com/gekkio/status/1337118677284622339)

> Game Boy SM83 CPU core RE status: since finishing decoder stage 2 and tracing its outputs, I've noticed how we've got a "everything is connected to everything" -type of situation...<br>
> So now I'm doing the ALU, the register file, and decoder stage 3 at the same time. 😅

</div>

<div class="tweet">

[![Screenshot of the original tweet](2020-12-10_2.png)](https://twitter.com/gekkio/status/1337121255158321153)

> Back when I started this RE work, I imagined a decoder connected like this:<br>
> opcode + CPU state -> stage1 -> stage2 -> stage3 -> various places like ALU and reg file
>
> Reality:<br>
> stage1 -> stage2 -> stage3 -> places<br>
> stage1 -> places<br>
> stage2 -> places<br>
> ALU has extra local decoding logic

</div>

## 2021 SM83 CPU work burnout, focus on better microscope and random GB projects {#2021}

### 2021-03-09

<div class="tweet">

[![Screenshot of the original tweet](2021-03-09.png)](https://twitter.com/gekkio/status/1369342559089266690)

> It's interesting to watch the value of my stock market investments go down, and the value of the 60+ Game Boys I bought 4-7 years ago to go up 😅<br>
> Maybe one day I'll actually sell some on Ebay for profit

</div>

### 2021-04-05

<div class="tweet">

[![Screenshot of the original tweet](2021-04-05.png)](https://twitter.com/gekkio/status/1379158254400471042)

> Writing a blog post about Game Boy flash cartridge power consumption. Pretty interesting measurement results!
>
> It makes me wonder how optimized existing designs are, and what are the practical limitations in designing low power carts...
>
> Blog post will be available soon™<br>
> [Attached screenshot](1379158254400471042-EyO_upCWQAMa88A.jpg)

</div>

### 2021-04-16

<div class="tweet">

[![Screenshot of the original tweet](2021-04-16.png)](https://twitter.com/gekkio/status/1383148933678006272)

> TIL: A 30-year old Game Boy cartridge can still have a battery in a very healthy condition. I just measured 3.257V battery voltage on a cart from 1991.
>
> I initially didn't believe it, but datasheets confirm 10-80 times difference in data retention current specs between RAM chips.

</div>

<div class="tweet">

[![Screenshot of the original tweet](2021-04-16_2.png)](https://twitter.com/gekkio/status/1383150970050338820)

> <https://gbhwdb.gekkio.fi/cartridges/DMG-GWJ-0/gekkio-1.html>
> The cart in question uses Sharp LH5168 with 0.6 uA MAX spec. Carts sometimes use chips which have 10uA or 50 uA MAX specs. Conditions may vary slightly, but even if the difference in reality is something like 1:5, it can mean 50 vs 10 year data retention.

</div>

### 2021-04-17

<div class="tweet">

[![Screenshot of the original tweet](2021-04-17.png)](https://twitter.com/gekkio/status/1383410961759932418)

> New blog post: Power Consumption of Game Boy Flash Cartridges
>
> [link](@/blog/2021/power-consumption-of-game-boy-flash-cartridges/index.md)
>
> Short summary:<br>
> Everdrive GB X5 beats other SD-card flash cartridges. Genuine carts beat Everdrive GB X5. My designs usually beat genuine carts

</div>

### 2021-05-08

<div class="tweet">

[![Screenshot of the original tweet](2021-05-08.png)](https://twitter.com/gekkio/status/1391098901059579905)

> It's been a while since I've done any work on this, but I finally have a rough but working MVP of this "magic" tool useful for chip reverse engineering.
>
> Current focus is Game Boy DMG-CPU B simulation and testing, but I plan to use the same approach on other chips as well.<br>
> [Attached screenshot](1391098901059579905-E04rPrcWUAA97kk.png)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2021-05-08_2.png)](https://twitter.com/gekkio/status/1391101118474764288)

> I already have a tool that generates a flat VHDL model from a KiCad netlist. But this is better, because I can isolate and test any part of the hierarchy separately.
>
> For example, I can write a VHDL testbench just for the "System clocks" module which is defined in clock_gen.vhd

</div>

<div class="tweet">

[![Screenshot of the original tweet](2021-05-08_3.png)](https://twitter.com/gekkio/status/1391102658090520577)

> And it turns out testing is crucial when dealing with a model of a large chip.<br>
> Maybe some cell has been misidentified or signal polarity is wrong in some cell model. A simple mistake can ruin the entire model, so I find testing and building trust piece by piece very important

</div>

### 2021-05-29

<div class="tweet">

[![Screenshot of the original tweet](2021-05-29.png)](https://twitter.com/gekkio/status/1398736569029345283)

> GhidraBoy for Ghidra 9.2.4 has been released 🎉
>
> Developing new GhidraBoy features is not on top of my list at the moment, but I *do* try to keep up with Ghidra releases so you should never find yourself unable to upgrade Ghidra just because GhidraBoy is holding you back.

</div>

### 2021-06-30

<div class="tweet">

[![Screenshot of the original tweet](2021-06-30.png)](https://twitter.com/gekkio/status/1410264175599931396)

> GhidraBoy for Ghidra 10.0 has been released 🎉
>
> As usual, a prebuilt binary package is available on the releases page:
>
> <https://github.com/Gekkio/GhidraBoy/releases/tag/20210630_ghidra_10.0>

</div>

### 2021-07-07

<div class="tweet">

[![Screenshot of the original tweet](2021-07-07.png)](https://twitter.com/gekkio/status/1412814144349347847)

> Fairly quick'n'dirty decap of Nintendo Game Boy Advance SP SoC chip (CPU AGB B) with 4x microscope magnification.
>
> Way too modern for detailed RE work, but some info can be collected from this photo.<br>
> Chip die labeled as "CBUG04". Package is QFP-156, die has 156 pads so no unused<br>
> [Attached photo](1412814144349347847-E5tRVpvWEAMOzQm.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2021-07-07_2.png)](https://twitter.com/gekkio/status/1412814463292542982)

> Max quality stitched photo is available here:
>
> <https://gekkio.fi/files/decapped>

</div>

### 2021-09-01

<div class="tweet">

[![Screenshot of the original tweet](2021-09-01.png)](https://twitter.com/gekkio/status/1433112545280335876)

> I've released the schematic for the original Game Boy LCD board (version DMG-LCD-06)
>
> Not terribly exciting, but these are (hopefully) accurate unlike the older schematics you can find online.
>
> <https://github.com/Gekkio/gb-schematics#original-game-boy-lcd-board-dmg-lcd-06>

</div>

### 2021-10-31

<div class="tweet">

[![Screenshot of the original tweet](2021-10-31.png)](https://twitter.com/gekkio/status/1454910696454598656)

> The test ROMs bundled with Mooneye GB emulator are now known as "Mooneye Test Suite", and are now in a separate repository:
> <https://github.com/Gekkio/mooneye-test-suite/>
>
> I'm still sorting out some practical things and the mooneye-gb repository hasn't been cleaned up yet, but this is a first step.

</div>

### 2021-12-11

<div class="tweet">

[![Screenshot of the original tweet](2021-12-11.png)](https://twitter.com/gekkio/status/1469607573053661189)

> GhidraBoy for Ghidra 10.1 has been released, so you no longer need to fear Java logging library CVEs when doing Game Boy ROM reverse engineering :)
>
> <https://github.com/Gekkio/GhidraBoy/releases/tag/20211211_ghidra_10.1>

</div>

## 2022: More schematics, SM83 CPU core fully reverse engineered {#2022}

### 2022-01-02

<div class="tweet">

[![Screenshot of the original tweet](2022-01-02.png)](https://twitter.com/gekkio/status/1477635068814401540)

> I've just released schematics for the first two Original Game Boy (DMG) power board revisions (unofficially known as type A / B) 🎉
>
> <https://github.com/Gekkio/gb-schematics/blob/main/DC-CONV-DMG-AB/schematic/DC-CONV-DMG-AB.pdf>
>
> Type C and D will be released later after I clean them a bit.
>
> Other schematics in the repo also got some minor updates 🙂

</div>

### 2022-01-12

<div class="tweet">

[![Screenshot of the original tweet](2022-01-12.png)](https://twitter.com/gekkio/status/1481381078631956483)

> As promised earlier, I've released the schematics for the remaining original Game Boy (DMG) power boards (type C / D) 😃
>
> I've also documented known differences and added visual component references since the boards have no component reference designators
>
> <https://github.com/Gekkio/gb-schematics#original-game-boy-dcdc-power-board-dc-conv-dmg--dc-conv2-dmg>

</div>

### 2022-02-19

<div class="tweet">

[![Screenshot of the original tweet](2022-02-19.png)](https://twitter.com/gekkio/status/1494796818298855425)

> 🎶<br>
> Might as well jump<br>
> Go ahead and jump<br>
> Get it in, jump<br>
> Go ahead and jump<br>
> 🎶
>
> For some strange reason I sometimes think about this song whenever I install more than 1 of these things...<br>
> [Attached photo 1](1494796818298855425-FL6T0KFXMAEsbKW.jpg)<br>
> [Attached photo 2](1494796818298855425-FL6T2ilWUAUanmh.jpg)

</div>

This lovely board would eventually make it much easier to capture all cartridge bus signals with a logic analyzer...at the time of writing (2022), it's not open source but perhaps I'll release it at some point.

<div class="tweet">

[![Screenshot of the original tweet](2022-02-19_2.png)](https://twitter.com/gekkio/status/1494799536321179655)

> Here's a sneak peek of my next Game Boy schematics project. I've already desoldered and characterized all components and am now doing tracing. After that it's time for schematics...
>
> This time the trace SVG is also nicer since I have two separate but aligned BG layers<br>
> [Attached screenshot](1494799536321179655-FL6XyVRX0AELY2W.jpg)

</div>

### 2022-03-09

<div class="tweet">

[![Screenshot of the original tweet](2022-03-09.png)](https://twitter.com/gekkio/status/1501611657537241092)

> My current chip decap project: Game Boy MBC1B memory bank controller chip found on many cartridges. This chip is already well understood, but decided to RE it thoroughly anyway.
>
> I've already traced everything and just need to finish the schematics...<br>
> [Attached screenshot 1](1501611657537241092-FNbKMpYWYAI_cqo.jpg)<br>
> [Attached screenshot 2](1501611657537241092-FNbLmVqXMAAPIej.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-03-09_2.png)](https://twitter.com/gekkio/status/1501614894633959426)

> Image quality is pretty bad since I used a low-quality 20x objective 😅 lots of optical aberrations...
>
> It's good enough to identify cells and connections, but I took some extra photos with a good 40x objective to study internal cell structures.
>
> Just look at the difference 😻<br>
> [Attached screenshot](1501614894633959426-FNbN299XsAAwFNp.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-03-09_3.png)](https://twitter.com/gekkio/status/1501616502352580614)

> "I didn't do anything! I'm sure it was like this when I found it!"<br>
> 😐
>
> Turns out I was a bit careless with decapping and the die took some damage. Luckily the connections were obvious and easy to guess...<br>
> [Attached screenshot](1501616502352580614-FNbPCMtXoAcjnWa.jpg)

</div>

### 2022-03-13

<div class="tweet">

[![Screenshot of the original tweet](2022-03-13.png)](https://twitter.com/gekkio/status/1502987288107786240)

> I've just released my Game Boy MBC1B chip research 🎉
>
> <https://github.com/Gekkio/gb-research/tree/main/mbc1b>
>
> - fully traced SVG file based on decapped chip photo<br>
> - KiCad schematics<br>
> - automatically generated VHDL model<br>
> - VHDL testbench, also verified on real HW
>
> Let's take a look at what's in the repo 🧵

</div>

This was an important "practice project", because I was going to use the same techniques for the SM83 CPU core and the full SoC.

<div class="tweet">

[![Screenshot of the original tweet](2022-03-13_2.png)](https://twitter.com/gekkio/status/1502987966892974081)

> Firstly we have the SVG file using a decapped die photo as a background.
>
> All connections are traced and cells are identified. I've even added start/end markers to connections: for example, "FE" OAI21 cell has one output (top left) and three inputs (2x top right, and 1x bottom)<br>
> [Attached screenshot](1502987966892974081-FNuvAtdXoAAi1Du.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-03-13_3.png)](https://twitter.com/gekkio/status/1502988513914068999)

> Then we have the KiCad schematics (top level sheet in the screenshot). I've tried to make them as readable as possible, but this is still a 1:1 cell-level mapping to the SVG so nothing should be missing.<br>
> [Attached screenshot](1502988513914068999-FNuvtPqXsAE5ALj.png)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-03-13_4.png)](https://twitter.com/gekkio/status/1502989656224419843)

> Then we have a VHDL model generated from the schematics using my Kingfish KiCad-to-HDL generator.<br>
> Not very readable since this is a raw mapping from the KiCad netlist, but the main point is to run a VHDL testbench "against the schematics" without error-prone manual work.<br>
> [Attached screenshot](1502989656224419843-FNuwOtYWQAYqR9h.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-03-13_5.png)](https://twitter.com/gekkio/status/1502990663788511239)

> Finally, a VHDL testbench tests and describes the expected behaviour of the generated model. These tests were taken from my old "gpio-bench" hardware system which ran peek/poke -style tests on a real MBC1 chip, so the tests have been previously verified on real hw.<br>
> [Attached screenshot](1502990663788511239-FNuxVLfXsAQEBat.png)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-03-13_6.png)](https://twitter.com/gekkio/status/1502991857965580297)

> Having a way to "test the schematics" has been invaluable...even on a simple chip like this I had one misidentified cell, which was only caught once I started running tests. Staring at schematics and trying to reason about them is way too slow and error-prone for me 😅

</div>

### 2022-03-19

<div class="tweet">

[![Screenshot of the original tweet](2022-03-19.png)](https://twitter.com/gekkio/status/1505214010349785091)

> I proudly present the schematics of Game Boy Light (a.k.a MGL) 🎉
>
> <https://github.com/Gekkio/gb-schematics/blob/main/MGL-CPU-01/schematic/MGL-CPU-01.pdf>
>
> As expected, it's 95% identical to Game Boy Pocket (a.k.a MGB), but that 5% includes some important differences that are now documented.
>
> Only *one* MGL was harmed to make these 😅

</div>

RIP my only Game Boy Light...it was kind of an expensive sacrifice, but I never used it anyway...🥲

### 2022-05-07

<div class="tweet">

[![Screenshot of the original tweet](2022-05-07.png)](https://twitter.com/gekkio/status/1523011738551164929)

> My gb-hardware repo now has a "naughty list" of people who violated the very liberal CC BY 4.0 license of my designs.
>
> License summary: just don't erase my name and claim you made the design 100% yourself. That's all. You can modify and/or sell freely.
>
> <https://github.com/gekkio/gb-hardware#license-violations-aka-naughty-list>

</div>

### 2022-05-30

<div class="tweet">

[![Screenshot of the original tweet](2022-05-30.png)](https://twitter.com/gekkio/status/1531336881429958657)

> Time for another Game Boy -related schematics release: I've RE'd 2 types of Game Boy Pocket DC/DC conversion boards! AFAIK there are no others.
>
> LSEP01088A1 (a.k.a. type A):
>
> <https://github.com/Gekkio/gb-schematics/blob/main/LSEP01088A1/schematic/LSEP01088A1.pdf>
>
> A different one with the text "MGB" (a.k.a. type B):
>
> <https://github.com/Gekkio/gb-schematics/blob/main/MGB-DCDC-B/schematic/MGB-DCDC-B.pdf>

</div>

### 2022-09-12

<div class="tweet">

[![Screenshot of the original tweet](2022-09-12.png)](https://twitter.com/gekkio/status/1569340023992119298)

> When I woke up yesterday, I had no idea I'd end up reverse engineering the Game Boy MBC2A mapper chip 😅
>
> Yesterday was spent on tracing, so now I just need to do schematics and simulation.
>
> Original background microscope photo by Raphael Boichot: <https://github.com/Raphael-Boichot/Game-Boy-chips-decapping-project/><br>
> [Attached screenshot](1569340023992119298-FcdqX8BWYAE3xD4.jpg)

</div>

*Narrator's voice*: "Just schematics and simulation" would end up taking months...

<div class="tweet">

[![Screenshot of the original tweet](2022-09-12_2.png)](https://twitter.com/gekkio/status/1569426101721612288)

> The main motivation was two pins: "VCC_RAM" and "GND_RAM". I realized I never questioned previous research which claimed these to be supply pins for embedded RAM. A quick look at the decap photo made it clear that they are I/O pins! I had to RE the whole chip to understand them

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-09-12_3.png)](https://twitter.com/gekkio/status/1569427215338577932)

> "GND_RAM" seems to be an active-low global output enable pin. On PCBs it's always tied low, so all outputs are enabled.
>
> "VCC_RAM" seems to be an active-low async clear pin, which resets all flip-flops. On PCBs it's always tied high, so it's deasserted.

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-09-12_4.png)](https://twitter.com/gekkio/status/1569427855737487361)

> The chip also has an active-low RESET pin, which is actually used on PCBs and it too resets all flip-flops.
>
> Why two pins for reset? RESET also gates inputs, so it does more than the other pin. Perhaps the CLEAR pin was used for testing, or is just an unused leftover feature.

</div>

### 2022-10-16

<div class="tweet">

[![Screenshot of the original tweet](2022-10-16.png)](https://twitter.com/gekkio/status/1581674682842955776)

> Getting ready to release my Game Boy SM83 CPU core research I started more than 2 years ago. I have a complete HDL model (written in VHDL), understand pretty much all the signals and have assigned good names for them.
>
> Here's a screenshot of the huge manually traced SVG file 😅<br>
> [Attached screenshot](1581674682842955776-FfM6_oQXEAU0EVV.jpg)

</div>

I was way too excited about this project and ended up tweeting this when I still had more work to do before release...perhaps I should've just tweeted the actual release, which happened just a week later.

<div class="tweet">

[![Screenshot of the original tweet](2022-10-16_2.png)](https://twitter.com/gekkio/status/1581676477984124928)

> Here's a zoomed in section of the ALU. The background is a massive stitched photo taken with my microscope using a 40x objective. Some educated guesswork based on my understanding of the chip was needed, because I can't see what's under the top metal layer.<br>
> [Attached screenshot](1581676477984124928-FfM9J6iWQAIzzF-.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-10-16_3.png)](https://twitter.com/gekkio/status/1581686531529457664)

> I originally started this work using a stitched microscope photo from [siliconpr0n.org](https://siliconpr0n.org). Here's one section as an example.
>
> This was sufficient for a lot of things, but some fine structures were a bit too difficult to figure out, so I started building my own microscope.<br>
> [Attached photo](1581686531529457664-FfNHJI8XgAEcXmt.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-10-16_4.png)](https://twitter.com/gekkio/status/1581688258953547778)

> Using a microscope with a 40x objective, I was able to selectively capture some areas with finer details. Without a motorized stage this was a lot of work, and as a result I had several photos and had to switch back-and-forth between them when tracing common signals<br>
> [Attached photo](1581688258953547778-FfNHkZ1XkAEIPfQ.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-10-16_5.png)](https://twitter.com/gekkio/status/1581689411107897344)

> The solution: capture the whole CPU core at 40x and make one big photo. This summer after a lot of work, I finally had a motorized scope and was able to do it. I've moved most of my previous work to this new single photo, fixed mistakes, and worked on the last ~10% I was missing<br>
> [Attached photo](1581689411107897344-FfNJ2zqXkAIMxdx.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-10-16_6.png)](https://twitter.com/gekkio/status/1581691747591077888)

> This turned out to be very useful 😄 As an example, here's one output from decoder stage 1, used by stage 2 and 3 and also the ALU. Previously I had 4 separate SVG files and had to jump between them to understand the whole signal. Now it's enough to look at one trace in one file<br>
> [Attached photo](1581691747591077888-FfNLmj5XkAIPZzz.jpg)

</div>

### 2022-10-23

<div class="tweet">

[![Screenshot of the original tweet](2022-10-23.png)](https://twitter.com/gekkio/status/1584234589442441219)

> After 2+ years of research, it's time to release my Game Boy SM83 CPU core RE work!
>
> <https://github.com/Gekkio/gb-research/tree/main/sm83-cpu-core>
>
> Includes non-synthesizable HDL model and an SVG with almost all important stuff traced.
>
> Passes Blargg's cpu_instrs tests, except "02 interrupts" which needs a full SoC<br>
> [Attached screenshot](1584234589442441219-FfxTpFrWQAA0xkx.jpg)

</div>

This was a massive milestone and the result of a lot of work...I could finally run test ROMs with my DMG-CPU B SoC model and continue that work. Many questions about the SM83 CPU core also got answered.

<div class="tweet">

[![Screenshot of the original tweet](2022-10-23_2.png)](https://twitter.com/gekkio/status/1584236637932126208)

> Let's take a tour! 😄
>
> Here's the register file: you can see all main registers, including the WZ temporary register, which is not directly visible to programmers. 8 "rows" where each row contains everything to handle one bit. 16-bit regs are built as 2x 8-bit adjacent regs<br>
> [Attached screenshot](1584236637932126208-FfxVt4jXEAEn_YH.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-10-23_3.png)](https://twitter.com/gekkio/status/1584237201411305472)

> Next to the reg file we have the Increment/Decrement Unit (IDU) and some interrupt handling logic. The IDU is a separate unit from ALU, and does 16-bit increment/decrement/load operations, and also outputs the 16-bit address to the rest of the SoC.<br>
> [Attached screenshot](1584237201411305472-FfxW5Q5XgAE-s90.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-10-23_4.png)](https://twitter.com/gekkio/status/1584238102335610880)

> The interrupt logic block contains e.g. interrupt priority and address handling and also the IE (Interrupt Enable) register. The IF (Interrupt Flag) register is not in the CPU but elsewhere in the SoC!
>
> The CPU core supports 8 interrupts + NMI, but some are disabled in the GB SoC

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-10-23_5.png)](https://twitter.com/gekkio/status/1584238514769575937)

> Next we have a massive 3-stage instruction decoder using dynamic logic. The decoder takes the current opcode and a bunch of other state as input, and outputs a lot of control signals to various parts of the CPU core.<br>
> [Attached screenshot](1584238514769575937-FfxYQbIXgAAPolR.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-10-23_6.png)](https://twitter.com/gekkio/status/1584239205903142913)

> Next to the decoder we have the control unit, which consists of a lot of logic cells. It contains some CPU state such as the IME register, and control various parts of the system while taking inputs from the decoder and other areas.<br>
> [Attached screenshot](1584239205903142913-FfxYqV_X0AAmZ7l.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-10-23_7.png)](https://twitter.com/gekkio/status/1584240032910839808)

> A very important part of the system is the 8-bit Arithmetic and Logic Unit (ALU), which handles 8-bit calculations (the IDU does some 16-bit stuff instead). I've also included the flag registers here, but it's debatable whether they are truly part of the ALU or not.<br>
> [Attached screenshot](1584240032910839808-FfxZR3hWQAA9JVv.jpg)

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-10-23_8.png)](https://twitter.com/gekkio/status/1584241140391239681)

> What about the HDL?
>
> Non-synthesizable HDL = you can't just put this on an FPGA and expect it to work. Why not? The core uses dynamic logic and other ASIC stuff that FPGAs simply can't do and need to emulate instead.
>
> The main goal here is to support simulation and understanding

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-10-23_9.png)](https://twitter.com/gekkio/status/1584242705923612672)

> What we *can* do is use this HDL as a reference model to build a more FPGA-friendly model. Many things can be simplified and improved, and the result can be compared to the reference.
>
> No plans to do this myself (for now), but I hope the HDL helps other people 😄

</div>

<div class="tweet">

[![Screenshot of the original tweet](2022-10-23_10.png)](https://twitter.com/gekkio/status/1584246690294693889)

> It's also important to understand that this is not a HDL model of a Game Boy...it's just the CPU core, so it can't run any games.
>
> A full and accurate HDL model of the whole Game Boy SoC is a separate thing, and there are multiple projects attempting it (yes I have one too).

</div>

## Final words

What a rollercoaster these 8 years have been! I've never been a huge fan of twitter, but it has been one of the main communication channels where I've announced new info about my various Game Boy projects. In the future, I'll probably focus on Mastodon instead of Twitter, despite having less than 1/10 followers there.
