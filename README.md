SHADOWRUN SEGA CD / MEGA-CD ENGLISH TRANSLATION
v1.2a Documentation / Compatibility Hotfix
Release filename convention: v12a
By RetchERezzed

======================================================================
TABLE OF CONTENTS
======================================================================
  1. Quick Start
  2. Package Contents
  3. What v1.2a Changes
  4. AllCaps vs. MixedCase
  5. Region and BIOS Compatibility
  6. Required Original Disc
  7. Tools and References
  8. Patch Files and Checksums
  9. Patching Instructions
 10. Finished Disc Layout and CUE
 11. Patched Track 1 Verification
 12. CHD Conversion
 13. Troubleshooting
 14. FAQ
 15. Updating from Older Releases
 16. Emulator Note: ares Overscan
 17. Technical Verification
 18. Changelog / Version History
 19. Reporting a Problem
 20. Credits

======================================================================
1. QUICK START
======================================================================
This patch is for the JAPANESE / NTSC-J Mega-CD release of Shadowrun.
It does NOT convert the game to U.S. / NTSC-U or European / PAL region.

1. Start with a clean Japanese three-track BIN/CUE dump
2. Patch ONLY: Shadowrun (Japan) (Track 1).bin
3. Choose ONE patch:
   Shadowrun_SegaCD_English_v12a_AllCaps.bps
   OR
   Shadowrun_SegaCD_English_v12a_MixedCase.bps
4. Save the patched output as:
   Shadowrun (Japan) (Track 1).bin
5. Keep these original files beside it, unchanged:
   Shadowrun (Japan).cue
   Shadowrun (Japan) (Track 2).bin
   Shadowrun (Japan) (Track 3).bin
6. Load Shadowrun (Japan).cue in your emulator
7. Use Japanese / NTSC-J Mega-CD boot compatibility

Region summary:
- Japanese / NTSC-J Mega-CD BIOS: intended stock region
- U.S. / NTSC-U Sega CD BIOS: NOT supported as a stock BIOS target
- European / PAL Mega-CD BIOS: NOT supported as a stock BIOS target

A wrong-region stock BIOS may open the Sega CD / Mega-CD CD-player screen
instead of booting Shadowrun. That does not by itself indicate a bad patch.

Do NOT patch the CUE, Track 2, Track 3, an ISO, a CHD, a combined BIN, or an
already translated Track 1.

======================================================================
2. PACKAGE CONTENTS
======================================================================
README.txt
Shadowrun_SegaCD_English_v12a_AllCaps.bps
Shadowrun_SegaCD_English_v12a_MixedCase.bps

This package does not include the game, BIOS, BIN/CUE disc image, CHD,
emulator, or patching software.

======================================================================
3. WHAT v1.2a CHANGES
======================================================================
v1.2a is a documentation, installation, and compatibility hotfix for v1.2.
The translated game data is unchanged from v1.2. The AllCaps and MixedCase BPS
payloads are byte-for-byte identical to the v1.2 game data.

v1.2a exists because:
- Some users had trouble reconstructing the three-track Sega CD image
- v1.1 unnecessarily encouraged renaming Track 1 and manually editing the CUE
- Some users attempted CHD conversion without preserving all three tracks
- Region and BIOS requirements were not clear enough
- A user with a stock U.S. Sega CD BIOS reached the CD-player screen
- v1.2 had not yet been certified through actual CHD creation and verification

No translation text, gameplay, graphics, balance, scripts, or game logic were
changed for v1.2a.

======================================================================
4. ALLCAPS VS. MIXEDCASE
======================================================================
Choose exactly ONE edition.

AllCaps
- Uppercase dialogue
- Uses the heavier all-caps font introduced in v1.1

MixedCase
- Sentence-case dialogue
- Mixed-case menus, spells, and equipment where appropriate
- Some artwork, abbreviations, battle labels, and fixed-format UI remain uppercase

Both editions contain the same translated game content. This is an unofficial
English machine translation with editing and playtesting, not a professional
human translation. Some wording or nuance may differ from the original Japanese.

======================================================================
5. REGION AND BIOS COMPATIBILITY
======================================================================
Original game region: Japan / NTSC-J Mega-CD
Region conversion performed by this patch: NONE

INTENDED STOCK REGION
- Japanese / NTSC-J Mega-CD BIOS

NOT SUPPORTED AS STOCK BIOS TARGETS
- U.S. / NTSC-U Sega CD BIOS
- European / PAL Mega-CD BIOS

The English translation does not make the disc U.S.-region software. The
original Japanese boot/security region data remain Japanese. A stock U.S. or
European BIOS may reject the disc before the game starts. One possible symptom
is the Sega CD / Mega-CD CD-player interface appearing while Shadowrun does not
boot.

Check BIOS/system region before assuming the patch, CUE, CHD, or patched
Track 1 is bad.

REGION-FREE / AUTO-REGION / HLE SETUPS
These may work depending on emulator and configuration, but behavior varies.
v1.2a does not claim universal compatibility with every modified BIOS,
region-free BIOS, HLE BIOS, auto-region mode, FPGA implementation,
optical-drive emulator, or physical-console modification. If your emulator
offers a region choice, select JAPAN unless its documentation says otherwise.

======================================================================
6. REQUIRED ORIGINAL DISC
======================================================================
Use your own clean Japanese three-track BIN/CUE dump of Shadowrun:

  Shadowrun (Japan).cue
  Shadowrun (Japan) (Track 1).bin
  Shadowrun (Japan) (Track 2).bin
  Shadowrun (Japan) (Track 3).bin

Only Track 1 is patched. Tracks 2 and 3 are CD-audio tracks and remain
untouched. The CUE describes the complete three-track disc and must be retained.

REQUIRED CLEAN TRACK 1
Filename: Shadowrun (Japan) (Track 1).bin
Size:     218,696,016 bytes
CRC32:    04F1BC85
SHA-256:  13a8a2c028fd7ef41eddade9a16848b03e7dce2580e80a539ad349e7bc7e7e34

OPTIONAL FULL-SOURCE VERIFICATION
Track 2 size:    15,690,192 bytes
Track 2 SHA-256: bcb4de28a9132f047239873334f9b001012bb657f6d3078f8394b2ec314d733a
Track 3 size:    15,690,192 bytes
Track 3 SHA-256: bcb4de28a9132f047239873334f9b001012bb657f6d3078f8394b2ec314d733a
CUE size:        315 bytes
CUE SHA-256:     0abe829f21982c5ca5051713138d7776aa7dbac3a3f43473422d8aafd748407e

If Track 1 does not match the required values, stop. Do not force the patch.
Always apply v1.2a directly to the verified clean Japanese Track 1.

Do NOT patch the ZIP, CUE, Track 2, Track 3, ISO, CHD, combined single-BIN
image, previously translated Track 1, or any older patched output.

======================================================================
7. TOOLS AND REFERENCES
======================================================================
BPS PATCHER
Recommended: Floating IPS / Flips
Project:  https://github.com/bates64/flips
Releases: https://github.com/bates64/flips/releases

Use Apply Patch and select exactly one v1.2a BPS file. Do not force the patch if
Flips reports that the source file is wrong.

EMULATOR
Use a Sega CD / Mega-CD emulator that supports BIN/CUE or CHD and Japanese
Mega-CD software. One emulator used during this project is ares:
Official site: https://ares-emu.net/
Downloads:     https://ares-emu.net/download

Configure the emulator for JAPAN / NTSC-J where applicable. Other emulators
may work, but v1.2a does not claim universal compatibility with every emulator
or version.

JAPANESE MEGA-CD BIOS
No BIOS file is included. If your emulator requires a real BIOS, provide your
own legally obtained Japanese / NTSC-J Mega-CD BIOS and follow that emulator's
instructions for filename and location. Do not substitute a stock U.S. or
European BIOS. This README does not provide BIOS download sites.

CHDMAN
chdman is included with MAME. v1.2a CHD certification used MAME 0.289.
MAME:         https://www.mamedev.org/release.html
chdman docs:  https://docs.mamedev.org/tools/chdman.html

Windows: chdman.exe is included in the official x64 MAME package
Linux:   many distributions provide chdman through MAME or mame-tools packages
macOS:   use a current MAME package/build that includes chdman

chdman is optional if your emulator loads the finished BIN/CUE set directly.

SHA-256 CHECKS
Windows PowerShell:
  Get-FileHash "Shadowrun (Japan) (Track 1).bin" -Algorithm SHA256
Windows Command Prompt:
  certutil -hashfile "Shadowrun (Japan) (Track 1).bin" SHA256
Linux:
  sha256sum "Shadowrun (Japan) (Track 1).bin"
macOS:
  shasum -a 256 "Shadowrun (Japan) (Track 1).bin"

======================================================================
8. PATCH FILES AND CHECKSUMS
======================================================================
Choose exactly ONE patch. Do not stack them.

AllCaps BPS
File:    Shadowrun_SegaCD_English_v12a_AllCaps.bps
SHA-256: 247529aee341fcc673d64bdd722a34e018ad531dd599a063ae0411cf5be06c0d

MixedCase BPS
File:    Shadowrun_SegaCD_English_v12a_MixedCase.bps
SHA-256: 3be4fccf9b8d4c034e385a31a6beb92978b58988f95d1f4da85d869513497f75

The BPS filename does not control how the patch works. Renaming a .bps file is
safe, but keeping the supplied names is recommended for identification and
support.

The finished Track 1 filename should remain exactly:
  Shadowrun (Japan) (Track 1).bin
when using the original CUE unchanged.

======================================================================
9. PATCHING INSTRUCTIONS
======================================================================
1. Create a folder for the translated game
2. Copy these untouched files into it:
   Shadowrun (Japan).cue
   Shadowrun (Japan) (Track 2).bin
   Shadowrun (Japan) (Track 3).bin
3. In Flips, choose Apply Patch
4. Select ONE v1.2a BPS patch
5. For the original file, select the verified clean:
   Shadowrun (Japan) (Track 1).bin
6. Save the patched output into the new folder as exactly:
   Shadowrun (Japan) (Track 1).bin
7. Confirm the finished folder matches the layout in Section 10
8. Load Shadowrun (Japan).cue in your emulator

Do not load Track 1 alone when CUE loading is available. Track 1 alone is not
the complete original CD because Tracks 2 and 3 contain CD audio.

======================================================================
10. FINISHED DISC LAYOUT AND CUE
======================================================================
The finished folder should contain:

  Shadowrun (Japan).cue
  Shadowrun (Japan) (Track 1).bin    <- PATCHED
  Shadowrun (Japan) (Track 2).bin    <- ORIGINAL, UNCHANGED
  Shadowrun (Japan) (Track 3).bin    <- ORIGINAL, UNCHANGED

For normal installation, DO NOT edit the CUE. v1.2a preserves the original
Track 1 filename so the original CUE works unchanged.

Canonical disc layout:
  Track 1: MODE1/2352 data
  Track 2: AUDIO
  Track 3: AUDIO

Do not rebuild the disc as a one-track image. If you intentionally rename a
BIN, its FILE line in the CUE must exactly match the new filename. Do not change
TRACK types, INDEX values, pregaps, or timing unless you specifically know why.

======================================================================
11. PATCHED TRACK 1 VERIFICATION
======================================================================
Both patched editions remain exactly 218,696,016 bytes.

AllCaps patched Track 1 SHA-256:
  b792c88b8356fbfe3731dedfafbe4903339562c8f78a0a5696ee3ebf21abec95

MixedCase patched Track 1 SHA-256:
  ac5fef469a8fd13cec8b3e0f568a87c5384348ead9f80e98147fc26bf5f70ae2

These are hashes for the patched Track 1 outputs, not the BPS files.

======================================================================
12. CHD CONVERSION
======================================================================
CHD conversion is optional. If your emulator supports BIN/CUE directly, the
finished three-track set can be used as-is.

To create a CHD, keep all four files from Section 10 together and convert the
CUE, not an individual BIN.

Tested tool: MAME chdman 0.289

Create:
  chdman createcd -i "Shadowrun (Japan).cue" -o "Shadowrun Sega CD English v12a.chd"

Verify:
  chdman verify -i "Shadowrun Sega CD English v12a.chd"

CERTIFICATION RESULTS
AllCaps:   createcd PASS | verify PASS | Raw SHA1 PASS | Overall SHA1 PASS
MixedCase: createcd PASS | verify PASS | Raw SHA1 PASS | Overall SHA1 PASS

Both tested CHDs retained:
- Track 1: MODE1_RAW
- Track 2: AUDIO
- Track 3: AUDIO
- Track 2 pregap: 150 frames
- Track 3 pregap: 150 frames

REFERENCE CHD RESULTS FROM MAME 0.289
AllCaps
Size:    165,537,909 bytes
SHA-1:   b79d40853fe6273c8e13f56badbfcdd642b69780
SHA-256: 1bf624cb34b66fa6c67fc59ad60eddad59fda9e0adfee0981221a3972475aa92

MixedCase
Size:    165,547,466 bytes
SHA-1:   3b426df70a4c13495d4633ceb4f8662f0032c239
SHA-256: b18f78c0d503531b046e84fe9bb5acba80fc3ae358191e2c79325867fbc16df0

Different chdman versions may produce different CHD files while representing
the same valid disc. Use chdman verify and the patched Track 1 SHA-256 as the
primary checks.

======================================================================
13. TROUBLESHOOTING
======================================================================
GAME OPENS THE CD PLAYER INSTEAD OF BOOTING
- Confirm the BIOS/system region is Japanese / NTSC-J
- If a real BIOS is required, use a Japanese Mega-CD BIOS
- Restart the emulator after changing BIOS/region settings
- Load the CUE or complete CHD, not Track 1 alone

A stock U.S. or European BIOS is not a supported stock target. Do not repeatedly
repatch the game solely because a wrong-region BIOS will not boot it.

PATCHER SAYS THE PATCH IS NOT INTENDED FOR THIS FILE
Required clean Track 1:
Size:    218,696,016 bytes
CRC32:   04F1BC85
SHA-256: 13a8a2c028fd7ef41eddade9a16848b03e7dce2580e80a539ad349e7bc7e7e34

Common causes include the wrong region/dump, a combined BIN, ISO conversion,
a previously patched file, or selecting the CUE, Track 2, or Track 3. Do not
disable checksum protection or force the patch.

EMULATOR OR CHDMAN CANNOT FIND A BIN FILE
The CUE filenames must exactly match the real BIN filenames:
  Shadowrun (Japan) (Track 1).bin
  Shadowrun (Japan) (Track 2).bin
  Shadowrun (Japan) (Track 3).bin

Filename matching may be case-sensitive. Do not change TRACK, INDEX, pregap,
or timing values to solve a filename problem.

CHDMAN WILL NOT CONVERT THE DISC
- Input Shadowrun (Japan).cue, not a BIN
- Keep all three BIN files beside the CUE
- Confirm Track 1 filename matches the CUE
- Keep Tracks 2 and 3 untouched
- Do not use a one-track replacement CUE
- Verify the patched Track 1 SHA-256 in Section 11

Both canonical editions converted and verified with MAME 0.289 during audit.

GAME BOOTS BUT CD AUDIO IS MISSING
Confirm Tracks 2 and 3 are present and load the CUE, or a CHD made from the
complete three-track CUE. Patched Track 1 alone is not the complete CD image.

======================================================================
14. FAQ
======================================================================
Q: Which patch should I use?
A: Choose ONE: AllCaps or MixedCase. Do not apply both. They contain the same
translated game content; only the text presentation differs.

Q: What exact file do I patch?
A: Patch only Shadowrun (Japan) (Track 1).bin from the supported clean Japanese
three-track dump.

Q: Why does the Sega CD / Mega-CD CD player open instead of the game?
A: Check region first. Shadowrun remains Japanese / NTSC-J software. A stock
U.S. / NTSC-U or European / PAL BIOS is not a supported stock target.

Q: Can I use CHD?
A: Yes. Convert the full three-track CUE with chdman. Do not convert Track 1 by
itself. Both v1.2a editions passed MAME 0.289 createcd and verify.

Q: Why is the music missing?
A: Tracks 2 and 3 contain CD audio. Make sure both are present, unchanged, and
referenced by the CUE.

Q: Can I rename the patch or patched BIN?
A: Renaming the .bps patch is harmless. Renaming the patched Track 1 BIN requires
updating the matching FILE line in the CUE. Keeping the original BIN filename is
recommended.

Q: Can I patch over v1.0, v1.1, or v1.2?
A: No. Always start from the verified clean Japanese Track 1 and apply exactly
one v1.2a patch.

Q: Why is the ZIP called v12a when the version is v1.2a?
A: v12a is the project's filename convention. The actual release version is
v1.2a.

======================================================================
15. UPDATING FROM OLDER RELEASES
======================================================================
Do not patch an older translated Track 1. Start again from the clean Japanese
Track 1 and apply exactly one v1.2a BPS.

Normal in-game saves may continue to work, but old emulator savestates can
retain old code, graphics, or runtime state and are not recommended for testing
a new patch. For clean troubleshooting, restart the emulator, load the newly
reconstructed CUE/CHD, and use the game's normal LOAD function where possible.

In town, SAVE is under ITEMS. Continue past NO ITEMS if it appears. Check EQUIP
before difficult fights. Owning a weapon does not automatically equip it.

======================================================================
16. EMULATOR NOTE: ARES OVERSCAN
======================================================================
If colored speckles appear along the bottom border in ares, try disabling
overscan. This removed the border pixels in previously tested ares v148 intro
scenes without changing the game picture. This is a display-setting workaround,
not a game-data correction or a universal guarantee for every ares version.

======================================================================
17. TECHNICAL VERIFICATION
======================================================================
v1.2a verification covered:
- canonical clean Japanese Track 1 hash
- exact AllCaps and MixedCase BPS application
- expected patched Track 1 hashes and preserved size
- raw MODE1/2352 sector structure
- changed-sector EDC, ECC P, and ECC Q verification
- original three-track CUE geometry
- original Track 2 and Track 3 preservation
- MAME 0.289 chdman createcd and verify for both editions

Raw sector audit:
AllCaps:   1,161 changed sectors | 0 invalid EDC/ECC checks
MixedCase: 1,164 changed sectors | 0 invalid EDC/ECC checks

No v1.2a sector sync/header corruption was found.

v1.2a does not claim testing on every emulator, modified BIOS, flash cart,
optical-drive emulator, FPGA implementation, burned-disc setup, or physical
console configuration. It also does not convert the Japanese disc region to
U.S. or Europe.

======================================================================
18. CHANGELOG / VERSION HISTORY
======================================================================
v1.2a - DOCUMENTATION / COMPATIBILITY HOTFIX
The game data is unchanged from v1.2. AllCaps and MixedCase BPS payloads are
byte-for-byte identical to v1.2 game data.

WHY v1.2a WAS RELEASED
Users reported trouble getting later releases running or converting to CHD, and
one user reached the Sega CD audio-player screen with a U.S. BIOS. Audit found
the v1.2 patched data itself valid: correct 218,696,016-byte MODE1/2352 Track 1,
0 changed-sector EDC/ECC failures, no track-boundary/header corruption, and both
editions successfully passed MAME 0.289 createcd and verify. The primary issue
was documentation/setup ambiguity rather than corrupt v1.2 game data.

CHANGES IN v1.2a
- Rewrote installation around one exact recommended three-track layout
- Explicitly states only Track 1 is patched; Tracks 2 and 3 remain untouched
- Removed the ordinary need to rename Track 1 or manually edit the CUE
- Added clean-source size, CRC32, and SHA-256 verification
- Added separate BPS and patched-Track-1 SHA-256 values
- Added CUE/filename troubleshooting and certified CHD instructions
- Added MODE1/2352 EDC/ECC audit results
- Added explicit Japanese / NTSC-J requirements
- Explicitly states no U.S./European region conversion is performed
- Explicitly states stock U.S. and European BIOSes are unsupported stock targets
- Added CD-player-screen region-mismatch guidance
- Added patcher, missing-BIN, CHD, CD-audio, and savestate troubleshooting
- Added official references for Flips, MAME/chdman, and ares
- Clarified compatibility limits and the optional nature of CHD conversion

UNCHANGED FROM v1.2
- Translation content
- AllCaps/MixedCase presentation
- Fonts and dialogue layout
- Interface changes and Blackbird battle-name correction
- Game logic, gameplay balance, scripts, and raw Track 1 target data

v1.2
- Corrected Blackbird's scrambled battle name in target panel/attack message
- Retained v1.1 fonts, dialogue layout, interface updates, and previous fixes
- Added ares display guidance

v1.1
- Introduced revised font/presentation options and AllCaps/MixedCase editions
- Added dialogue-layout and interface updates
- Its recommendation to rename Track 1 and manually edit the CUE proved
  unnecessarily fragile; v1.2a preserves the original Track 1 filename and CUE

======================================================================
19. REPORTING A PROBLEM
======================================================================
Please include:
- AllCaps or MixedCase
- Patch version: v1.2a
- Emulator/hardware name and version
- BIOS region: Japan, USA, Europe/PAL, region-free, HLE, or unknown
- BIN/CUE or CHD
- Whether the game boots or only reaches the CD player
- Scenario/location if the issue occurs in-game
- Exact error message, if any
- Screenshot if useful
- Patched Track 1 SHA-256 if possible

Do not share copyrighted game BINs, CHDs, BIOS files, or other original game
data when reporting problems.

======================================================================
20. CREDITS
======================================================================
Translation project: RetchERezzed
Tester: Blamhammer

Special thanks to Blamhammer for thorough playtesting and feedback that helped
uncover script inconsistencies and repair progression problems.
Thanks to RetroGameTalk and its community for their support.

Shadowrun and the original game belong to their respective rights holders.
No game files, BIOS files, emulator binaries, saves, or savestates are included
in this translation package.
