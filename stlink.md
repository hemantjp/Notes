## need to pass to work properly
-c "reset_config none"

## absence of rst pin on st-link.. explained
https://github.com/chaosAD/ST-Link-SWD-No-SRST/wiki/Disabling-the-ST-Link-SRST
to be added after scripts imported

## command
openocd -f /usr/share/openocd/scripts/interface/stlink-v2.cfg -f /usr/share/openocd/scripts/target/stm32f1x.cfg -c "reset_config none" -c "gdb_port 4000" -c "telnet_port 0" -c "tcl_port 0" -c "hla_serial \x6b\x3f\x00\x01\x32\x12\x46\x47\x52\x4b\x4e\x00"
