# Action to build Kivy App to APK using Buildozer

### How to use  
```
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
```
