desura-cef3
===========


Build Windows
-----------

 * Get depot tools from https://src.chromium.org/svn/trunk/tools/depot_tools.zip and add it to your path
 * In a new folder run "fetch --nohooks chromium --nosvn=True"
 * cd to the source dir
 * run "gclient sync --revision src@[revision] --jobs 8 --force" (replace revision with the value from CHROMIUM_BUILD_COMPATIBILITY.txt)
 * Clone this repo into src/cef
 * run "set GYP_GENERATORS='ninja'"
 * cd src/cef
 * run "cef_create_projects.bat"
 * cd up a dir
 * run "ninja -C out/Debug cef_desura"

```
set GYP_MSVS_VERSION=2013
set GYP_GENERATORS=ninja
set GYP_DEFINES=windows_sdk_path="C:\Program Files (x86)\Microsoft SDKs\Windows\v7.1A"
```
