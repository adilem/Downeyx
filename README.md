# Downey

Original repo can be found here https://github.com/dengskoloper/downey



To compile downey for your platform, download the golang installation package from here: https://go.dev/dl/. Make sure that the go executable is added to the PATH variable.

Next, clone the repo locally and change the directory to the root of the repo. Run this command to build the code for your platform:

```
go build -o downey[.exe] -a main.go
```

Tool options:

```
downey.exe --lic-server "<License Server URL>" [--add-headers]
--lic-server:   License Server URL for the manifest.mpd
--add-headers:   Read HTTP headers from headers.json 
```

If you use the --add-headers option, then you need to create a headers.json file with structure like so:

```
{
    "cookie": "hs_uid=b82f6b01-4bf2-4828-9cd9-ea64d514f9a6; ajs_group_id=null",
    "origin": "https://www.hotstar.com",
    "referer": "https://www.hotstar.com/",
    "user-agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/102.0.0.0 Safari/537.36"
}
```
Downey requires the MPD to be added to the root of the Downey directory, and has to be named as `manifest.mpd`