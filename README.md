# AutoSplit64Enhanced

AutoSplit64Enhanced is an experimental local customization of Kainev's AutoSplit64 rewrite for Super Mario 64 speedruns. This README records the changes made in that local build. This GitHub fork contains the upstream code and these project notes.

## Added

- **LiveSplit route following.** AutoSplit64 can read the saved splits path, reuse a matching `.as64` route, or convert the open `.lss` file. It switches routes while the timer is idle. This feature requires a LiveSplit build that supports `getsplitspath`.
- **Direct OBS capture.** The AS64+ Frame Grabber can supply the game feed directly from OBS.
- **Route tools.** The Route Editor has a category browser, a configurable route folder, and batch conversion for LiveSplit splits. Star count and fade counts are editable for all split types.
- **Live detection feedback.** The sidebar shows detected and target star counts. **More → Show Output** displays fades, X-Cam status, prediction confidence, and processing time.
- **Detection settings.** Settings include LiveSplit named-pipe and TCP connections, autostart, calibration, and error correction. Automatic undo for a corrected star count is opt-in.

## Changed

- Added route logic for LBLJ, Bowser, Mips, and Final splits. LBLJ counts confirmed gameplay fades. Final detection checks for a pickup after the Grand Star spawn camera returns to gameplay.
- Added category-based defaults for BitDW and BitFS, and recognition of BitS as a Final split when editing routes or importing LiveSplit splits.
- Separated game reset detection from LBLJ fade counting so a recognized reset can restart LiveSplit.
- Made OBS capture retry when the frame changes during a read, and skip a contested frame during detection.
- Updated the Windows app name to AutoSplit64Enhanced and restored the original AutoSplit64 icon.

## Upstream

AutoSplit64 was created by Kainev. The current upstream rewrite's license notice does not grant permission to distribute modified builds. See the [upstream project and license notice](https://github.com/kainev/AutoSplit64#license).
