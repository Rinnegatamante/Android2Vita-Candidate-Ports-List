# Android2Vita-Candidate-Ports-List
- A list of candidate Android games portable to Vita. ( https://android.rinnegatamante.it )
- Please read this README.md in full and check the candidate list before submitting a new port candidate. 
## Android Port Requirements for Vita SO Loader
✔️ ARMv6 or ARMv7 executable\
✔️ OpenGL: GLES 1 or GLES 2\
✔️ FMOD: No FMOD Usage or libfmod.so only\
🔶 OpenGL: GLES 3+\
🔶 FMOD: libfmodevent.so, libfmodex.so, libfmodstudio.so\
❌ ARMv8 executable only\
❌ Kotlin only\
❌ Unity games (libunity.so)\
❌ Java games (libgdx.so)
## How do I Check ARM Executable?
- Extract the APK using an archive extracter (7-ZIP, WinZip).
- Open the "lib" folder.
- If no "lib" folder is present, the game CANNOT be ported.
- If an "armeabi" folder is present, the game has an ARMv6 executable. 
- If an "armeabi-v7a" folder is present, the game has an ARMv7 executable. 
- It's possible for both folders to be present. 
- If only the "arm64-v8a" is present, the game CANNOT be ported. 
## How Do I Check OpenGL Version?
- Option 1: https://ghidra-sre.org/
  - Extract the APK using an archive extracter (7-ZIP, WinZip).
  - Locate the main game executable inside inside "armeabi" or "armeabi-v7a" folder.
  - Open the game executable in ghidra. 
  - Read the analysis summary, this will inform the OpenGL versions that are linked (libGLES.so, libGLESv2.so, libGLESv3.so). 
- Option 2: https://ibotpeaches.github.io/Apktool/ 
  - use apktool to decrypt the "AndroidManifest.xml" inside the APK. 
  - Read the OpenGL version under "glesVersion: " parameter. 
## How Do I Check FMOD Usage?
- Extract the APK using a archive extracter (7-ZIP, WinZip).
- Open the "lib" folder. 
- Open either the "armeabi" or "armeabi-v7a" folder. 
- Check for the following files: 
  - libfmod.so
  - libfmodevent.so
  - libfmodex.so
  - libfmodstudio.so
- If only libfmod.so is present, the game CAN be ported with sound. 
- If other FMOD files are there, the game CANNOT be ported with sound.  
## How Do I Check Unity, Java and Kotlin Usage?
- Extract the APK using an archive extracter (7-ZIP, WinZip)
- If a Kotlin folder is present, with no lib folder, the game CANNOT be ported. 
- Open the "lib" folder 
- Open either the "armeabi" or "armeabi-v7a" folder. 
- If lib folder contains libgdx.so or libunity.so, the game CANNOT be ported. 
