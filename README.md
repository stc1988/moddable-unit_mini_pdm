# UNIT MINI PDM

This is a library for using `UNIT MINI PDM` with Moddable SDK.

## inclide manifest

To use this driver, you need to add the following to the include section of the manifest file.

```jsonc
{
  "include": [
    // ...
    {
      "git": "https://github.com/stc1988/moddable-unit_mini_pdm.git"
    }
  ]
}
```

In the manifest file, each device is configured with pin asgins for connection to PORT A as default port. For details and pin assignments for other ports, please refer to the [linked page](https://docs.m5stack.com/en/unit/pdm).

| Moddable | UNIT   |
| -------- | ------ |
| datain   | DAT    |
| bck_pin  | unused |
| lr_pin   | CLK    |

If you want to use it connected to PORT B or PORT C, you can include `manifest_port_b.json` or `manifest_port_c.json`.

```jsonc
{
  "include": [
    // ...
    {
      "git": "https://github.com/stc1988/moddable-unit_mini_pdm.git",
      "manifest": "manifest_port_b.json"
    }
  ]
}
```