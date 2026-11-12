DISCLAIMER:This patch was vibe-coded using Google Antigravity.
Feel free to to report any error messages with screenshots.

SEEK2 -SADISTIC BABYLON- (DMM Download Version)
Complete No-CD & New Game Error 500 Fix Patch


[About this patch]
The digital release of SEEK2 on DMM is distributed without an ISO / CD image.
When launched on modern Windows, the game normally encounters these issues:
  1) CD-ROM check error ("Please install correctly from CD-ROM!!")
  2) Installation path error ("Installation was not completed normally.")
  3) Error 500 when starting New Game ("Cannot open file: s2_SXCG.NSC")
     because the engine expects a physical CD subfolder (seek2dat\cg24\).

This patch permanently fixes all of them:
  - Bypasses all CD-ROM drive and volume checks cleanly in START_UP.SCC.
  - Automatically redirects CG and scene lookups to the local cg24/cg08 folders.
  - Automatically links seek2dat junctions so scenario commands find all assets.
  - Automatically configures C:\Windows\STONEHDS.INI with the correct game path.
  - Works with the original official DMM seek2.exe without crashes or modifications.

------------------------------------------------------------------------
[How to Install]
------------------------------------------------------------------------
1. Extract all files from this ZIP directly into your SEEK2 game folder
   (the folder that contains seek2.exe).
   When prompted, choose "Replace" / "Overwrite" for START_UP.SCC.

2. Double-click "Fix_Windows_INI.bat".
   Click "Yes" on the Windows Administrator prompt (UAC).
   A command window will configure the paths and display:
     "STONEHDS.INI configuration applied successfully!"
     "Setup complete!"
   Press any key to close the window.

3. Right-click "seek2.exe" -> "Locale Emulator" -> "Run in Japanese(ADMINISTRATOR)".
   Click "New Game" and enjoy!

------------------------------------------------------------------------
[Included Files]
------------------------------------------------------------------------
- START_UP.SCC       : Patched bytecode script (No-CD & local CG redirect).
- Fix_Windows_INI.bat: Automated path configuration and directory linker.
- STONEHDS.INI       : Standalone settings template.
- INSTRUCTIONS.txt   : This guide.
