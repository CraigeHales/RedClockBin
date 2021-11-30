# RedClockBin

Compiled binary for RedClock project: Large binary blobs don't belong in the main source library because they make it slow.

The pushall.py script expects to find the tzblob.bin in the same directory the script is in, which may need to be .../RedClock/esp/RedClock/tzblob.bin. If you are just uploading tzblob.bin to update the clock, just find it in the browser and upload to the server as "Timezone_Update.Bin" (case matters).

Likewise, pushall.py expects to find RedClock.bin in the build directory. If you are just uploading RedClock.bin to update the clock, just find it in the browser and upload to the server as "Executable_Update.Bin" (case matters).

Unless there are other notes, the two bin files can be mixed-and-matched. The tz file is a blob of info about timezones, including both a GPS-location to timezone-name map AND the timezone-name's string describing when the time change occurs. Probably you don't want an older version.

RedClock.bin is the compiled executable. You might want an older version if an error seems to be in a newer version. When you visit the clock's internal webpage, you'll see the RedClock (not RedClockBin) number on the status page as app_desc_version: b2d4e8a (for example.) (dirty means built from code not checked in.)


I don't have a plan for the spiffs files, yet. Keeping them under source control in the RedClock project makes sense for now. They are also loosely coupled to the excutable. spiffs holds html, js, css files.

