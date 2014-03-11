desura-cef3
===========


Build Windows
-----------

 * Get depot tools from https://src.chromium.org/svn/trunk/tools/depot_tools.zip and add it to your path
 * In a new folder run "fetch --nohooks chromium --nosvn=True"
 * cd to the source dir
 * run "git svn find-rev r<revision>" (replace revision with the value from CHROMIUM_BUILD_COMPATIBILITY.txt)
 * cd up a dir
 * run "gclient sync --revision <commit_hash> --jobs 8 --force" (replace commit_hash with the result of the command before)
 * Clone this repo into src/cef
 * run "set GYP_GENERATORS='ninja'"
 * cd src/cef
 * run "cef_create_projects.bat"
 * cd up a dir
 * run "ninja -C out/Debug cef_desura"
