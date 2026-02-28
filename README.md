# snap-sync

> This is an actively maintained fork of [wesbarnett/snap-sync](https://github.com/wesbarnett/snap-sync), focussed on keeping the original project's simplicity. My goal is to fix existing bugs without adding extensive new features.

Backs up btrfs snapshots incrementally to an external drive using snapper. Mount any btrfs-formatted device and run the script — you'll be prompted to select it, or specify it by UUID on the command line.

By default the script iterates through all snapper configurations (override with `-c`). For each, it creates a new local snapshot. On first sync to a device you'll be prompted for a backup directory. On subsequent runs only the changes since the last backup are sent.

## Installation

Clone the repository and run `make install`. snapper is required.

If your system uses a non-default location for the snapper configuration file, specify it with `SNAPPER_CONFIG`:

    make SNAPPER_CONFIG=/etc/conf.d/snapper install

To uninstall:

    make uninstall

## Documentation

See `snap-sync(8)` after installation.

## Troubleshooting

After reviewing the man page, check the [issues page] and open a new issue if your problem is not covered.

## Contributing

Feel free to open a pull request to add features or fix an issue.

[issues page]: https://github.com/jhayden02/snap-sync/issues
