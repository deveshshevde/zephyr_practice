### To flash :
```python -m esptool --port /dev/ttyACM0 --chip auto --baud 921600 --before default_reset --after hard_reset write_flash -u --flash_size detect 0x0```
### Console :
```python -m serial.tools.miniterm /dev/ttyACM0```
### Remote server
```pi@raspberrypi:/mnt/sda1/shared/zephyr_practice $ docker run -it \
  -p 2222:22 \
  -p 8800:8800 \
  -v $(pwd):/workspace \
  -w /workspace \
  env-zephyr-espressif
docker: permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Head "http://%2Fvar%2Frun%2Fdocker.sock/_ping": dial unix /var/run/docker.sock: connect: permission denied

Run 'docker run --help' for more information
pi@raspberrypi:/mnt/sda1/shared/zephyr_practice $ sudo docker run -it   -p 2222:22   -p 8800:8800   -v $(pwd):/workspace   -w /workspace   env-zephyr-espressif
[2025-09-18T19:03:24.454Z] info  code-server 4.93.1 69df01185ce2f80e99c9e4f8c8de1907cc7a9bc5
[2025-09-18T19:03:24.455Z] info  Using user-data-dir /root/.local/share/code-server
[2025-09-18T19:03:24.475Z] info  Using config file /root/.config/code-server/config.yaml
[2025-09-18T19:03:24.475Z] info  HTTP server listening on http://0.0.0.0:8800/
[2025-09-18T19:03:24.475Z] info    - Authentication is disabled
[2025-09-18T19:03:24.475Z] info    - Not serving HTTPS
[2025-09-18T19:03:24.475Z] info  Session server listening on /root/.local/share/code-server/code-server-ipc.sock
[19:04:04] 

```
