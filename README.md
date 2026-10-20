# Arm Robot Sorting Machine

## View the AMB82-Mini RTSP stream with FFplay

Install FFmpeg if `ffplay` is not recognized by PowerShell:

```powershell
winget install --id Gyan.FFmpeg --exact
```

Close and reopen PowerShell, then check the installation:

```powershell
ffplay -version
```

Run FFplay with low buffering and UDP transport (update the address if the board's IP changes):

```powershell
ffplay -rtsp_transport udp -fflags nobuffer -flags low_delay -framedrop -an "rtsp://192.168.0.25:554"
```
