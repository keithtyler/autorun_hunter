# autorun_hunter
Enterprise collection of Autorun details via autorunsc.exe and GRR

Script is intended to be run as a python_hack in GRR Rapid Response to collect SHA256 hash, location, path and digital signature of all autoruns available from autorunsc.exe and send them to the event log.

Details here: https://informationonsecurity.blogspot.com/2019/10/enterprise-autorun-collections-with.html

Example - adding this to your GRR server
```
sudo grr_config_updater upload_python --file grr_autorun_hunter.py --platform windows
```

Running the flow involves navigating to a particular host in question and running the administrative flow -> ExecutePythonHack. The syntax for the flow would be:
```
windows\grr_autorun_hunter.py
```
in our above example.

If you don't see Execute Python Hack, ensure your settings are in the "advanced" mode by selecting the gear icon in the web UI.
