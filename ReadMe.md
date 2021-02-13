# OpenHPSDR-PowerSDR

Latest Release v3.5.0 Beta 11 February 13, 2021

Read the RealeaseNotes.md for more information (Don't bother, they ain't up to date).

# 3.5.0 Beta 11 (2021-02-13)
- Add functionality for Hermes Lite
  - Added initial setup radio button to do basic setup
  - Adjusted setup form to reflect Hermes Lite functionality
  - Changes functionality of CPU utilisation to display temp/ver/PA current
  - Adjusted S-Att to utilise full LNA range, gain is shown as negative attenuation
  - Auto adjust of S-Att to utilise full range of ADC
  - Power meter scaled correctly
  - Fixed PS SetPk variable not being saved correctly
  - Changed database location for HL2 to not interfere with offical PowerSDR releases
  - Changed Setup/General/Hermes Lite Ctrl to repurpose Hercules button for N2ADR filter
  - Setup wizard creates initial Hermes Lite Ctrl pins for N2ADR filter
  - Fixed issue where changes to the Hermes Lite J16 receive pins were being lost over power cycle
  - Auto att keeps AGC gain constant
  - Corrected operation of "Rx/TX Ant" button so that it work with RX1 on Filter/Ant setup page (Alex renamed to Filter/Ant)  
  - Auto Att can now be switch off by setting "Auto delay" to 0
  - Re-enabled "MUT" button. It mightn't work on second Rx
  - Added experimental variable mouse wheel scroll. Enable/Disable via Setup/Display
  - Added ability to adjust Tx buffer latency and PTT hang time
  - Auto Att increases attenuation by 10 dB if overload exists on band change
  - Fixed bug which caused PTT to not obay hang time using CWX
  - Added display of minor revision and number of Rxs
  - Fixed bug in Tx latency up/down control
  - Added ability to key Tx via MIDI
  - Added ability to PTT (CWX) via MIDI
  - Added ability to trip PTT in CWX before keying. This is measured in dot periods, so will vary by WPM
  - Extended Tx latency control to 70 mSec 
  - Added option to switch between Fan PWM and Band Volts
  - Updated Hermes Lite Control to populate Tx fields
  - Fixed bug in Tx latency which cause roll over after 31 mSec
  - Fixed bug which caused Tx latency and PPT hang to initialise to zero
  - Set default latency to 20 mSec and PTT hang to 12 mSec
  - Auto Att backs off by 3db at limit to allow more headroom
  - Adjusted S meter calibration to better reflect correct signal level. Should be within +/- 2dB
  
# 3.4.9 (2018-3-19)
- Bug fix for manually entering frequency

# 3.4.8 (2018-3-17)
- Creates new wisdom file for each folder when using the -datapath command
- Bug fix for Behringer mini-wheels mapping issue when mapping AGC gain
- Added support for mapping drive level to a Behringer mini-wheel
- Added Panafall display for RX2
- Corrected a resizing problem when enabling RX2
- NB/NB2 is turned OFF while transmitting when DUP is enabled
- Added 2kHz Tune Step
- Changed ANF behavior so that it is disabled when in CW mode
- Removed the 750Hz CW filter and added a 150Hz CW filter (requires database reset to update)
- Added an Audio Adaptive Variable Resampler with monitor tools
- Increased display buffer to support larger than 4k displays
- Added separate VFO Lock controls for VFOA and VFOB. New VFO Lock button will require additional skin files to operate correctly.
- Added several CAT Commands. (see ReleaseNotes for details)
- Added a dropped packet ("OOOPs") counter that measures the number of dropped receive packets from radio to PC. This may be useful in identifying problems with network setup.
- fixed bug in CAT Command ZZPT## to change TXProfiles in different modes
- Updated CAT Commands documentation. Found in the Documentation/Radio folder

# 3.4.7 (2017-12-22)
- Control added to force the LPF to the 6m/ByPass position during receive. Filters must be under manual control to use. (Setup=>General=>Ant/Filters=>LPF, HPF/LPF, BPF1)
- VFO Lock correctly locks VFOA and VFOB.
- TX Amplitude scaling added to waterfall display. (Setup=>Display=>TX)

# 3.4.6 (2017-11-20)
- Corrected problem with blank waterfall display in Panafall mode.

# 3.4.5 (2017-11-20)
- Bug fix for .NET unhandled exception error when starting without radio online.

# 3.4.4 (2017-11-19)
- Added MIDI CAT support for the Behringer CMD Studio 2a
- Added support for the ANAN-7000DLE transceiver
- Added feature to select between receive or transmit antenna for receiving
- Use of seperate TX Profiles for various modes. 
  - LSB, USB, DSB, CWL, CWU, SPEC, & DRM 
  - FM
  - AM & SAM 
  - DIGL & DIGU
- PRO Latency feature added.

# 3.4.2 (2017-7-5)
- CTUN has had several modifications and bug fixes.
- Band Stacks have been increased to 5 deep for each band.
- CW Filters are now being saved correctly.

# 3.4.1 (2017-6-1)
- Swapped places with XIT and RIT controls on the console.
- Added 4 CAT Commands
 - ZZAP Audio Peak Filter On/Off
 - ZZAT APF Tune
 - ZZAB APB Bandwidth
 - ZZAA APF Gain
- Corrected compatibility issue with N1MM+ and FocusMaster.
- relabeled the 'CW Break-In' feature from 'Enabled' to 'Semi Break-In' to better describe the actual behavior. Toggles between Full Break-In and Semi Break-In.
- Single side-band Full Carrier (SSBFC)
- Continuous Frequency Compressor (CFC) audio tools
- Database enhancements allowing importing old databases

