# ✨ Build Kivy App to APK using Buildozer ✨

Effortlessly build your Kivy app into an APK with this GitHub Action! 🚀

## Key features:
 * Simple setup: Use the provided code snippet in your workflow.
 * Automates builds: Triggered on every push to the main branch.
 * Customizable: Adjust the buildozer-cmd, python-version and work-dir parameters if needed.

## How to use:
 * Copy the code below into your .github/workflows/ directory.
 * Modify the buildozer-cmd, python-version and work-dir if necessary.
 * Commit and push to your main branch to trigger the build.

### How to use  
```yml
on:
  push:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Build APK
        uses: digreatbrian/buildozer-action@v1
        with:
          buildozer-cmd: buildozer -v android debug
          work-dir: . # directory where your main.py file rests

      - name: Upload artifacts
        uses: actions/upload-artifact@v2
        with:
          name: package
          path: ./bin/*.apk
```

## Contributions welcome!
Feel free to submit issues, suggestions, or pull requests to improve this action. Let's make it even better together! 🤗  

Happy coding! 😄
