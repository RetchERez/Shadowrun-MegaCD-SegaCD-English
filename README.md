SHADOWRUN SEGA CD / MEGA-CD ENGLISH TRANSLATION v1.3
====================================================

Release type: Region compatibility release
Package filename: Shadowrun_SegaCD_English_v13.zip

This package contains BPS patches only. It does not contain the game disc,
BIOS files, emulator files, CHD files, BIN/CUE files, or CD audio.

TABLE OF CONTENTS
-----------------
1. What Changed in v1.3
2. Which Patch to Use
3. Required Source Files
4. Patching Instructions
5. Finished Disc Layout
6. CHD Conversion
7. Verification Summary
8. Checksums
9. Troubleshooting
10. Changelog
11. Credits

1. WHAT CHANGED IN v1.3
-----------------------
v1.3 adds separate region-targeted patch files for stock Japanese, U.S., and
European BIOS setups.

Earlier v1.2/v1.1/v1.0 public patches were Japanese-region releases. They could
boot on Japanese-region setups, but stock U.S. and European BIOSes could reject
them and open the Sega CD / Mega-CD CD-player screen. Editing the CUE could not
fix that, because that symptom is a BIOS/region mismatch, not a track filename
problem.

v1.3 fixes this by providing separate Track 1 patch targets:

- JP patches for Japanese / NTSC-J Mega-CD BIOS
- US patches for U.S. / NTSC-U Sega CD BIOS
- EU patches for European / PAL Mega-CD BIOS

Translation content is based on v1.2. The JP v1.3 targets are byte-identical to
v1.2 game data. The US and EU targets add region-converted boot compatibility.

2. WHICH PATCH TO USE
---------------------
Choose one text style and one BIOS region. Apply only one BPS patch.

AllCaps:
- Shadowrun_SegaCD_English_v13_AllCaps_JP.bps
- Shadowrun_SegaCD_English_v13_AllCaps_US.bps
- Shadowrun_SegaCD_English_v13_AllCaps_EU.bps

MixedCase:
- Shadowrun_SegaCD_English_v13_MixedCase_JP.bps
- Shadowrun_SegaCD_English_v13_MixedCase_US.bps
- Shadowrun_SegaCD_English_v13_MixedCase_EU.bps

Use JP if your setup boots Japanese Mega-CD software.
Use US if your setup uses a stock U.S. Sega CD BIOS.
Use EU if your setup uses a stock European / PAL Mega-CD BIOS.

AllCaps and MixedCase contain the same translation content. AllCaps keeps more
of the original all-capital presentation. MixedCase uses sentence-style casing
where appropriate.

3. REQUIRED SOURCE FILES
------------------------
Use the clean Japanese three-track Shadowrun Mega-CD / Sega CD dump:

Shadowrun (Japan).cue
Shadowrun (Japan) (Track 1).bin
Shadowrun (Japan) (Track 2).bin
Shadowrun (Japan) (Track 3).bin

Patch only:

Shadowrun (Japan) (Track 1).bin

Do not patch Track 2, Track 3, the CUE, an ISO, a CHD, a combined BIN, or an
already patched Track 1.

Required clean Track 1 SHA-256:
13a8a2c028fd7ef41eddade9a16848b03e7dce2580e80a539ad349e7bc7e7e34

Optional full source-set hashes:
Shadowrun (Japan).cue
0abe829f21982c5ca5051713138d7776aa7dbac3a3f43473422d8aafd748407e

Shadowrun (Japan) (Track 2).bin
bcb4de28a9132f047239873334f9b001012bb657f6d3078f8394b2ec314d733a

Shadowrun (Japan) (Track 3).bin
bcb4de28a9132f047239873334f9b001012bb657f6d3078f8394b2ec314d733a

4. PATCHING INSTRUCTIONS
------------------------
1. Extract this release package.
2. Choose exactly one BPS patch for your BIOS region and text style.
3. Apply that BPS patch to the clean Japanese Track 1 BIN only.
4. Save the patched output as:

   Shadowrun (Japan) (Track 1).bin

5. Put the patched Track 1 beside the untouched Track 2, Track 3, and original
   CUE.
6. Load the CUE in your emulator or convert the CUE to CHD.

The BPS filename does not affect patching. The patched Track 1 filename does
matter if you use the original CUE unchanged.

5. FINISHED DISC LAYOUT
-----------------------
The finished folder should contain:

Shadowrun (Japan).cue                         original, unchanged
Shadowrun (Japan) (Track 1).bin               patched
Shadowrun (Japan) (Track 2).bin               original, unchanged
Shadowrun (Japan) (Track 3).bin               original, unchanged

The CUE should continue to reference these filenames. Do not edit the CUE to fix
region problems. Use the correct JP, US, or EU BPS patch instead.

6. CHD CONVERSION
-----------------
CHD is optional. If your emulator loads BIN/CUE, CHD is not required.

If you want CHD, convert the CUE, not Track 1 by itself:

chdman createcd -i "Shadowrun (Japan).cue" -o "Shadowrun Sega CD English v1.3.chd"
chdman verify -i "Shadowrun Sega CD English v1.3.chd"

v1.3 CHD creation and verification were tested with MAME 0.289 chdman for all
six BPS targets. Each test returned:

Raw SHA1 verification successful
Overall SHA1 verification successful

7. VERIFICATION SUMMARY
-----------------------
The release package includes proof images in the proof folder.

Controlled runtime tests:
- Clean Japanese source Track 1
- Fresh BPS application
- Original CUE
- Original Track 2 and Track 3
- No save states
- PicoDrive libretro 2.05-ab02114
- Matching regional BIOS for each regional patch

PicoDrive cold-boot results:
- AllCaps JP with Japanese BIOS: PASS, title menu reached
- AllCaps US with U.S. BIOS: PASS, title menu reached
- AllCaps EU with European BIOS: PASS, title menu reached
- MixedCase JP with Japanese BIOS: PASS, title menu reached
- MixedCase US with U.S. BIOS: PASS, title menu reached
- MixedCase EU with European BIOS: PASS, title menu reached

Additional cross-check:
- Genesis Plus GX libretro v1.7.4 c2838c7
- AllCaps JP, US, and EU each reached the title menu with matching BIOS

BPS reapply verification:
- All six BPS files reapply to the clean Track 1
- All six reapplied outputs match their expected target Track 1 byte-for-byte

8. CHECKSUMS
------------
BPS patch SHA-256:

Shadowrun_SegaCD_English_v13_AllCaps_JP.bps
6cd2a50d843923ebf0d86b04ef7afe16a62c41e511c7e8120cd2c8dc765bfea7

Shadowrun_SegaCD_English_v13_AllCaps_US.bps
90cc2850340254920b9a37639f237ac9138ed26ae92613409de1b8e3860455d2

Shadowrun_SegaCD_English_v13_AllCaps_EU.bps
19f6cc202e66ca6d7262c3565b2fd8379e2c08ca9cc6c570e161fa159075f399

Shadowrun_SegaCD_English_v13_MixedCase_JP.bps
699ed1b52dcfe2860cf74147bc9abfe553a23644c594d9d2c917c18efa38367f

Shadowrun_SegaCD_English_v13_MixedCase_US.bps
c9a4904ce7e0c4b2347b9db128a875acd4e6802e41bffbc9a78bb52ea3f796de

Shadowrun_SegaCD_English_v13_MixedCase_EU.bps
0b2170e41a8afe05c1079b590e35ea11ccc3ace27e196fb2e2de9fe98d074eb7

Expected patched Track 1 SHA-256:

AllCaps JP
b792c88b8356fbfe3731dedfafbe4903339562c8f78a0a5696ee3ebf21abec95

AllCaps US
d92a8f1e715f0606128a1e2f934dee9568d4a98d16b6def73932eb775e238597

AllCaps EU
7a88235e4ce146c9c05149eac982dac52a059392e9bbf296a2f8d9889f0cff99

MixedCase JP
ac5fef469a8fd13cec8b3e0f568a87c5384348ead9f80e98147fc26bf5f70ae2

MixedCase US
75d9f56910c76f4062ee0f492680e5eb46c9f0e90a6900d4dc1da4338a82b89e

MixedCase EU
bb279451f527ef4c4b0b26ec7b16e37bbd55f4147b3038909e5cb86c72f22d5f

Reference CHD SHA-256, if users choose to create CHDs with MAME 0.289 chdman:

AllCaps JP
1bf624cb34b66fa6c67fc59ad60eddad59fda9e0adfee0981221a3972475aa92

AllCaps US
eb7b2d0f41a73d1a8e5351f6dfafc778b4cde760f22a604d7aae996a7102ffc9

AllCaps EU
0fcacb4f24a9ef87ad641e02f9770ea5b35c5ade8c7df5819c2ab2fefa8c1852

MixedCase JP
b18f78c0d503531b046e84fe9bb5acba80fc3ae358191e2c79325867fbc16df0

MixedCase US
aa35917770cf8fb686792cb2b2836bfc9db55f15640f3cd9fa1b506b897b020d

MixedCase EU
c2232c392d79cc4fe69dd92100afd6d4aac75faefcd9ea10bd7bc1655939120f

9. TROUBLESHOOTING
------------------
Problem: The Sega CD / Mega-CD CD-player screen opens.
Check: You probably used the wrong regional patch for your BIOS. Use JP with a
Japanese BIOS, US with a U.S. BIOS, and EU with a European BIOS.

Problem: Editing the CUE does not make the game boot.
Check: CUE edits only fix filename/path problems. They do not change the disc
region. Use the correct regional BPS patch.

Problem: No CD audio or missing music.
Check: Track 2 or Track 3 is missing, renamed, moved, or no longer matches the
CUE. The patch modifies Track 1 only.

Problem: The patcher says the source file is wrong.
Check: You are not using the exact clean Japanese Track 1, or the file was
already modified. Compare the clean Track 1 SHA-256 above.

Problem: The game shows edge pixels or garbage in ares.
Check: Use the emulator's overscan crop or hide-overscan option as appropriate
for the installed ares version. Edge pixels may be outside the intended CRT
visible area.

10. CHANGELOG
-------------
v1.3
- Adds separate JP, US, and EU regional BPS patch targets
- Adds stock U.S. Sega CD BIOS boot support through US patch targets
- Adds stock European / PAL Mega-CD BIOS boot support through EU patch targets
- Keeps JP target byte-identical to v1.2 game data
- Keeps AllCaps and MixedCase text-style options
- Documents that CUE editing does not fix region mismatch
- Adds cold-boot proof sheets and validation report
- Adds CHD verification references for all six patch targets

v1.2
- Previous public release baseline used for translation content
- Japanese-region boot compatibility only unless using a region-free setup

11. CREDITS
-----------
Shadowrun is owned by its respective rights holders. This is an unofficial fan
translation patch. Support official releases.
