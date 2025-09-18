To flash :
```python -m esptool --port /dev/ttyACM0 --chip auto --baud 921600 --before default_reset --after hard_reset write_flash -u --flash_size detect 0x0```
Console :
```python -m serial.tools.miniterm /dev/ttyACM0```
