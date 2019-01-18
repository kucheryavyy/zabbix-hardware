# zabbix-hardware
Current features:
- RAM info for Windows through WMI

![ram-items](https://raw.githubusercontent.com/nobodysu/zabbix-hardware/master/screenshots/hardware-ram-items.png)
## Testing
```bash
zabbix_get -s 192.0.2.1 -k hw.ram.discovery[get,"Example host"]
```
Default operation mode. Displays json that server should get, detaches, then waits and sends data with zabbix-sender. `Example host` is your `Host name` field in zabbix.
<br /><br />

```bash
zabbix_get -s 192.0.2.1 -k hw.ram.discovery[getverb,"Example host"]
```
Verbose mode. Does not detaches or prints LLD. Lists all items sent to zabbix-sender, also it is possible to see sender output in this mode.
