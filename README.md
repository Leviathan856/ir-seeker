# IR-missile seeker

STM32F411 based project that utilizes MLX90614 IR sensor for thermal image capturing with 4-fin targeting simulation

## Dependencies

- Zephyr v4.2.99
- west zephyr-sdk v0.17.4

## Steps to flash

1. Build the project
```
west build -p always -b blackpill_f411ce
```

2. Flash the project via ST-Link v2
```
west flash -r openocd --cmd-pre-init "reset_config none"
```

3. Attach to RTT console
```
probe-rs attach --chip STM32F411CEUx build/zephyr/zephyr.elf
```
