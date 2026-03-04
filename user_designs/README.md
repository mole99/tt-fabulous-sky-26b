# User Designs

Currently, forks of Yosys and nextpnr are required in order to implement the user designs. The changes to these forks are being upstreamed.

## Requirements

Enable a Nix shell with the forks of Yosys and nextpnr:

```
nix-shell
```

**Note:** To generate the bitstreams you need to `pip3 install fasm`. (Still to be added to the Nix shell.)

## Implement the Designs

To build all user designs, run:

```
make all
```

To build individual user designs, use their name:

```
make counter
```

The following Make targets are available:

```
make counter-clean
make counter-synth
make counter-pnr
make counter-bit
make counter-hex
```

You can also enter the individual design directories and run make from there:

```
Commands:
 synth           ... Synthesize the user design
 pnr             ... Run Place and Route
 bitstream       ... Generate the bitstream
 clean           ... Delete all generated files
 help            ... Show this help message
```
