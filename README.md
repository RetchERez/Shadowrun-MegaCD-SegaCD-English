SHADOWRUN | SEGA CD / MEGA-CD ENGLISH TRANSLATION
v1.4 FINAL | By RetchERezzed
========================================================================
Machine-assisted English translation of the original Japanese Mega-CD game
6 BPS patches + README only | Clean Japanese 3-track BIN/CUE source required

CONTENTS
--------
1  Release summary
2  Patch selection and required source
3  Installation
4  Optional CHD conversion
5  Checksums
6  Verification and limitations
7  Troubleshooting
8  Changelog and credits

1. RELEASE SUMMARY
------------------
v1.4 Final combines all retained v1.4 translation, speaker/dialogue and
MixedCase capitalization corrections into one release. Six variants are
provided: AllCaps and MixedCase for Japanese, U.S. and European BIOS regions.

The combined v1.4 Final includes the 12 additional corrected MixedCase rows
found during the full 5,993-page editorial review. These 15 capitalization
edits fix Akihabara, Aida, Ehara, Gozm Corp., and incorrect sentence or
page-continuation capitals. Text positions, controls, row lengths and timing
are unchanged. The AllCaps patch payloads are unaffected by these corrections.

The earlier v1.4 Nat speaker-perspective fix, Busora/retaliation/street
terminology and prior comma-continuation revisions remain included.
This v1.4 Final package supersedes the previous v1.4 distribution.
Apply a patch ONLY to the original Japanese Track 1, never to another patch.

2. PATCH SELECTION AND REQUIRED SOURCE
-------------------------------------
Choose ONE capitalization style and ONE matching boot-region BIOS:
  AllCaps    All-capital dialogue
  MixedCase  Contextual upper/lowercase dialogue
  JP         Japanese / NTSC-J Mega-CD BIOS
  US         U.S. / NTSC-U Sega CD BIOS
  EU         European / PAL Mega-CD BIOS

Included patches:
  Shadowrun_SegaCD_English_v14_AllCaps_JP.bps
  Shadowrun_SegaCD_English_v14_AllCaps_US.bps
  Shadowrun_SegaCD_English_v14_AllCaps_EU.bps
  Shadowrun_SegaCD_English_v14_MixedCase_JP.bps
  Shadowrun_SegaCD_English_v14_MixedCase_US.bps
  Shadowrun_SegaCD_English_v14_MixedCase_EU.bps

All six BPS files require the SAME clean Japanese Track 1 source:
  Shadowrun (Japan) (Track 1).bin
  Size: 218,696,016 bytes (raw MODE1/2352 sectors)
  SHA-256: 13a8a2c028fd7ef41eddade9a16848b03e7dce2580e80a539ad349e7bc7e7e34

Do not use a previously patched Track 1, an ISO, a CHD, or a combined BIN.
The finished disc also needs the original Track 2, Track 3 and CUE.
No disc tracks, BIOS, emulator, or commercial game resources are included.

3. INSTALLATION
---------------
1  Use Flips or another BPS-compatible patcher to apply ONE BPS file
   to the clean Japanese Track 1 BIN
2  Save the output to a separate folder under its original name:
   Shadowrun (Japan) (Track 1).bin
3  Place the untouched original Track 2, Track 3 and CUE beside it
4  Open the CUE in a Sega/Mega-CD-capable emulator using the matching BIOS

Required resulting folder:
  Shadowrun (Japan).cue
  Shadowrun (Japan) (Track 1).bin  (patched)
  Shadowrun (Japan) (Track 2).bin  (unchanged audio)
  Shadowrun (Japan) (Track 3).bin  (unchanged audio)

The CUE must reference these exact filenames. A wrong BIOS region is not
repaired by renaming a BIN or modifying the CUE.
Flips: https://github.com/bates64/flips

4. OPTIONAL CHD CONVERSION
--------------------------
Use the prepared CUE, never Track 1 by itself:
  chdman createcd -i "Shadowrun (Japan).cue" -o "Shadowrun_v14.chd"
  chdman verify -i "Shadowrun_v14.chd"

CHD does not change BIOS region. The three MixedCase JP/US/EU outputs passed MAME 0.289 createcd
and raw/overall SHA-1 verification. AllCaps CHD checks were previously
recorded for the same unchanged patch payloads.
Reference: https://docs.mamedev.org/tools/chdman.html

5. CHECKSUMS
------------
BPS file SHA-256 values (these hashes are for the patches, NOT the game):
  AllCaps_EU     8381ce3e9caa4849562d0e86bfce50b69a3c3fd08600dd6f5e2251a305c271e3
  AllCaps_JP     9cdfd946d74107987d724b25945727e018b0d76e36cf065070b92d0564c9e21c
  AllCaps_US     3622f8b7f5558009c080ef7c590bf8dc21345053ee7c0dc159f0830ffcdf540e
  MixedCase_EU   31af5fa7cfa0f0f6e522efb834813e09ad6865b6867a7dcddcb727a9778911bf
  MixedCase_JP   5419a94ef19bb39fcf68b14baf7db2ba56be556c08621630580e9e96d6cd3584
  MixedCase_US   434394d5410b72b904121512248a84dfe4671531b7f106de448eaaca167f3f16

Patched Track 1 SHA-256 values (218,696,016-byte output BIN):
  AllCaps_EU     03d320aa2d65062a30eafc90bdc1b33300e8273466952fbd9bfe58550b0234e5
  AllCaps_JP     0e672c205ed28f9b60c1e590b858ea30cecfeff57ae70465524a547f38b5062a
  AllCaps_US     fb1e01e1a77c6d94e2ec59ca336999ffe060772e052572a0741dd95b56f65da0
  MixedCase_EU   a8edefaf274e7912af4e73e1d2cb87a67119a7cc82ab47de5c0515efeaeb3cf7
  MixedCase_JP   bbb89c5f4f2087d9d4037efd958c82c865b1abbb0a7e5dbf0fdb4804148d2db3
  MixedCase_US   ca9d5ee066fc7ca77944b6d91dd7ea37349f5e9abfe24b891692e92d5cd3189a

6. VERIFICATION AND LIMITATIONS
------------------------------
Previously recorded clean-source BPS reapplication: 6/6 PASS
Current patch-only repack: 6/6 SHA-256, BPS CRC32 + bounds PASS
Final MixedCase case-only additions: 15 character edits per edition
Changed raw sectors in MixedCase: 9 per edition, all MODE1 EDC/ECC PASS
Dialogue page layout/control comparison: all 5,993 pages, zero changes
AllCaps/MixedCase English text equal when case-normalized: 5,993 pages

Fresh v1.4 FINAL gameplay verification on November 5, 2026:
  PicoDrive libretro 2.05-733c711; clean disc and actual JP BIOS
  MixedCase JP: cold boot, interactive Silver Moon and Hajime briefing,
  Nat video conversation, Shibuya exploration and passerby dialogue,
  CIRCUS Datanet Slasher Case/Shibuya War, Gyakushimaya location
  LIVE PASS: Nat wording, representative comma-continuation pages,
  retaliation sentence, Shibuya side-street wording, Busora sentence
  PARTIAL: Nat video-call portraits/perspective visibly functional;
  original forum wrong-speaker screenshot is missing, so the exact
  original reported attribution cannot be definitively compared
  JP/US/EU AllCaps and MixedCase: 6/6 fresh cold boot into English
  prologue with corresponding BIOS and individually hashed patch output
  Only JP MixedCase was deeply runtime-played for the editorial scenes
  Independent 6/6 region patch integrity remains as described above
  Complete campaign and late-game dialogue are NOT certified
  Separate evidence: Shadowrun_v14_Actual_Gameplay_Proof.zip
  This evidence ZIP contains untouched raw emulator PNG frames,
  their SHA-256s, one assembled contact sheet, and a provenance index

Previously recorded PicoDrive libretro 2.05-ab02114 tests:
  (these tests have NOT been rerun for this minimal repack)
  6/6 cold boots: 32,430 frames, opening dialogue reached
  6/6 Nat regressions: 25,920 frames, corrected speech visible
  No old savestate for cold boot; later Nat route used each new build's
  own saved checkpoint
Genesis Plus GX: 6/6 title/menu captures, no post-title certification
MAME 0.289 chdman: 3/3 newly modified MixedCase CHDs verified

Actual captured gameplay evidence is distributed SEPARATELY from this ZIP:
  Shadowrun_v14_Actual_Gameplay_Proof.zip (fresh JP runtime frames)
  Shadowrun_v14_Final_ContactSheet.png (earlier intro + Nat call)
  Shadowrun_v14_SixEdition_Story_Progression_Proof.png
  Shadowrun_v14_Yokohama_Hibunro_6Edition_Proof.png
  Shadowrun_v14_Hibunro_ClosedClub_6Edition_Proof.png
These are retained PicoDrive capture PROOF SHEETS from earlier tests.
They are not newly recorded raw frame PNGs from this repack. The
newest lettering corrections were verified in patch data, not
reached in live late-game screenshots.

LIMITS: This release is not exhaustive certification
of the seven-scenario campaign, every branch, combat, Matrix, or ending.
Kega, ares, and physical hardware are not certified for this release.
The inaccessible original forum screenshot prevents proving that every
speaker-attribution complaint concerned the corrected Nat scene.

7. TROUBLESHOOTING
------------------
CD player instead of game: ensure selected patch region matches the BIOS
CUE cannot load: confirm the four exact source filenames in Section 3
Patch rejected: verify the required clean Track 1 hash in Section 2
No CD audio: keep both original audio tracks and the three-track CUE
CHD conversion failure: supply the complete CUE/BIN set to chdman
Emulator edge garbage: use the appropriate hide/crop overscan setting
Unexpected text: supply the scene, version, BIOS and actual screenshot

8. CHANGELOG AND CREDITS
------------------------
v1.4 Final
- Corrected the speaker perspective in the initial Nat video-call dialogue
  without changing the portrait assignment or dialogue-control sequence
- Integrated all prior v1.4 wording improvements, including Nat, Busora,
  retaliation phrasing and selected side-street/backstreet terminology
- Reviewed and corrected 98 MixedCase comma continuations in the earlier pass
- Retained earlier proper-name and three "God" capitalization fixes
- Corrected 12 further MixedCase dialogue rows containing 15 case errors
  across Akihabara, Aida, Ehara, Gozm Corp. and sentence continuations
- Fixed mid-sentence "Which", "Began", and cross-page "And" casing
- Preserved AllCaps output unchanged by the 12 additional MixedCase edits
- Retained Japanese, U.S. and European BIOS region patch selection
- Preserved text controls, box dimensions, row lengths and display timing
- Verified patch-specific SHA-256 hashes and target checksums
- Recorded six regional cold-boot, Nat and title-screen smoke test results
  and three revised MixedCase CHD verification results
- Full seven-scenario and ending traversal remains unverified

By RetchERezzed | Unofficial, machine-assisted fan translation
Shadowrun and related trademarks belong to their respective owners
Use a lawfully obtained original Japanese disc image
