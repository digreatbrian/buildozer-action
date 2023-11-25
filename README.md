# Action to build Kivy App to APK

### How to use  
```
on:
  push:
    branches: [ main ]

jobs:
  runs-on: ubuntu-latest
  steps:
    - name: Build
      uses: digreatbrian/buildozer-action@v1
      with:
        command: buildozer -v android debug
```
