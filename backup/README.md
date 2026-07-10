# Stock firmware backup (sanitized)

Full 4 MB flash dump of the original PetKit Fresh Element Solo firmware
(ESP32-D0WD board revision, 2024 unit).

**Sanitized:** the following partitions are erased (0xFF) to remove personal data:
nvs, user_sn, user_id, user_bind, user_wifi_mg, user_schdl, user_msg,
user_sys_sta, user_config, user_server.

Restore to stock:

    esptool --chip esp32 --port COM6 --baud 460800 write-flash 0 esp32_stock_backup_SANITIZED.bin

Then re-pair the feeder through the PetKit app.
Always prefer your OWN backup — see the main README.
