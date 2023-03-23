# Android2Vita-Candidate-Ports-List
- A list of candidate Android games portable to Vita. ( https://android.rinnegatamante.it )
- Please read this README.md in full and check the candidate list, before submitting a new port candidate. 
# Android Port Requirements for Vita SO Loader 
## Requirements Summary
✔️ ARMv6 OR ARMv7 exexutable\
✔️ OpenGL: GLES 1 or GLES 2\
✔️ FMOD: No FMOD Usage OR libfmod.so only\
🔶 OpenGL: GLES 3+\
🔶 FMOD: libfmodevent.so, libfmodex.so, libfmodstudio.so\
❌ ARMv8 executable only\
❌ Kotlin only\
❌ Unity games (libunity.so)\
❌ Java games (libgdx.so)
## How do I Check ARM Executable?
- Extract the APK using a archive extracter (7-ZIP, WinZip)
- Open the "lib" folder 
- If an "armeabi" folder is present, the game has an ARMv6 executable. 
- If an "armeabi-v7a" folder is present, the game has an ARMv7 executable. 
- It's possible for both folders to be present. 
- If only the "arm64-v8a" is present, the game CANNOT be ported. 
## How Do I Check OpenGL Version?
- ???
## How Do I Check FMOD Usage?
- Extract the APK using a archive extracter (7-ZIP, WinZip)
- Open the "lib" folder 
- Open either the "armeabi" or "armeabi-v7a" folder. 
- Check for the following files: 
  - libfmod.so
  - libfmodevent.so
  - libfmodex.so
  - libfmodstudio.so
- If only libfmod.so is present, the game CAN be ported with sound. 
- If other FMOD files are there, the game CANNOT be ported with sound.  
## How Do I Check Unity, Java and Kotlin Usage?
- Extract the APK using a archive extracter (7-ZIP, WinZip)
- If a Kotlin folder is present, with no lib folder, the game CANNOT be ported. 
- Open the "lib" folder 
- Open either the "armeabi" or "armeabi-v7a" folder. 
- If lib folder contains libgdx.so or libunity.so, the game CANNOT be ported. 
