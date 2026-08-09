<p align="center">
  <img src="brand/ore-slab-live.svg" width="100%"
       alt="OOBE:Fe Lite for Windows and OOBE:Nd N42 for Android, in one ORE chassis">
</p>

# OOBE:Fe

A set of small instruments that share one chassis.

Every one of them does a real job on real files, says what it measured rather than what it guessed, and refuses to pretend. They look like laboratory hardware because they behave like it: stamped metal for the machine, recessed glass for anything that is a number, and four heat tiers that carry every warning in the app so a red edge always means the same thing.

> [!NOTE]
> This repository holds **downloads and nothing else**. There is no source here.

---

## Downloads

| | Platform | Where |
|---|---|---|
| **OOBE:Fe Lite** | Windows 10 or later, 64 bit | [Releases](../../releases) |
| **OOBE:Nd N42** | Android 9 or later | [oobe-fe-mobile-releases](https://github.com/HelyerAnArgh/oobe-fe-mobile-releases/releases) |

> [!TIP]
> **The phone build lives in its own repository now.** Everything mobile is at [oobe-fe-mobile-releases](https://github.com/HelyerAnArgh/oobe-fe-mobile-releases), including its own downloads, notes and updates.

---

## OOBE:Fe Lite

| Module | Does |
|---|---|
| **Nd** | Plays your music, and measures it |
| **Ge** | Shows you where your disk space went |
| **Li** | Reads a plugged in phone, and only ever reads |

### Nd, the music module

**A ten band graphic EQ**, because Windows Media Player 11 had ten and muscle memory is real. Shelves at the ends, bells in the middle, eight presets, and double click a band to zero it.

> [!TIP]
> **Quiet Mode is a real compressor**, not a checkbox that does nothing. Measured at **14.4 dB** of gain reduction on loud material and exactly **0.00 dB** when it is off.

**The seek bar is the real envelope of the track**, 900 buckets measured from the audio and drawn as 182 bars, downsampled by maximum and never by average, because averaging drags every transient towards the mean until the whole thing looks like a sausage.

**It measures your library and tells you the bad news.** One pass gives every track its replay gain, its dynamic range and whether it clips. A real 1,256 track library came back at **mean DR7.9** with **326 tracks** holding samples over full scale, which is a sentence about the loudness war rather than about this app.

**It plays the video hiding inside an mp3.** The container decides, never the extension, so a file named `.mp3` that is secretly MP4 simply works and the readout says `REALLY MP4` about it.

**Twelve smart lists, which are questions rather than folders.** Rate a five star track down to two and it leaves Favourites while you watch, because there is nothing stored to go stale.

**Deep listening statistics**, including a weekday by hour heatmap of 168 cells, because *when* you listen is a two dimensional fact and one line of totals throws half of it away.

### Ge, this machine

Where the disk space actually went, with duplicates found rather than implied.

### Li, a plugged in phone

> [!IMPORTANT]
> **Read only, permanently.** Nothing is written, moved or deleted on a connected handset. Ever.

---

## Updating

Lite asks **one pinned file** in this repository whether a newer build exists, shortly after it starts, and then leaves you alone. Nagging is the thing this design is arranged to avoid.

Old releases keep their page but not their installer. Nothing depends on them: the pinned file always names the current build.

> [!NOTE]
> The phone build updates from [its own repository](https://github.com/HelyerAnArgh/oobe-fe-mobile-releases) rather than this one. Builds of it before 0.1.1 checked here, and will find their way across on their own.

## Before you install

> [!WARNING]
> **SmartScreen will pull a face on first run.** The installer is not signed with a Microsoft code signing certificate. More info, then Run anyway.

Windows 10 or later, 64 bit.

## Scanned

Every build gets put through VirusTotal and the result is kept here, so it can be checked rather than trusted.

| Build | Result | Report |
|---|---|---|
| **OOBE:Fe Lite 0.1.10** | 1 detection, 66 clean | [`aa30d450...`](https://www.virustotal.com/gui/file/aa30d45011d21c184d7e3e0aab4155f8f69dadf8ae05a6073a2216b8a1590ee9) |
| **OOBE:Nd N42 0.1.1** | **0 detections**, 68 clean | [`445d76b1...`](https://www.virustotal.com/gui/file/445d76b1a44e103698fedb3f526aca99e4e2a9bdd8d158281b5230e3379143ea) |

> [!NOTE]
> **The one detection is Microsoft's `Trojan:Win32/Wacatac.B!ml`, and the `!ml` on the end is the whole story.** It marks a verdict reached by a machine learning model rather than a signature match, and it is the ordinary result for an installer that is newly built, carries no code signing certificate, and has been downloaded so far by almost nobody. **Nothing else agrees with it.** Sixty six engines return nothing, and the Android build is flagged by none at all.
>
> It is named here rather than left off, because one heuristic hit with the engine and the reason attached tells you more than a clean looking badge does.

Check that what you downloaded is the file that was scanned:

```
Lite 0.1.10   aa30d45011d21c184d7e3e0aab4155f8f69dadf8ae05a6073a2216b8a1590ee9
N42  0.1.1    445d76b1a44e103698fedb3f526aca99e4e2a9bdd8d158281b5230e3379143ea
```

```powershell
Get-FileHash .\OOBE-Fe-Lite_0.1.10_x64-setup.exe -Algorithm SHA256
```

```bash
sha256sum OOBE-Nd-N42-0.1.1.apk
```

---

> [!IMPORTANT]
> **Nothing leaves your machine.** Your library, your artwork, your play counts and every measurement stay on the machine that made them. There is no account, no telemetry and no server. The only outbound request this app ever makes is fetching the update file named above, and it is a plain public download that sends nothing about you.
