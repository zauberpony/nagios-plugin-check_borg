# check_borg

Check borg repository for date of latest archive.

Usable with nagios, icinga2 or any other nagios-fork.

Fork from [bebehei/nagios-plugin-check_borg](https://github.com/bebehei/nagios-plugin-check_borg). Changes:

- uses hours as threshold-values for critical and warning
- works only with borg >= 1.1
- works on FreeBSD and Linux

# Usage

    ./check_borg -R <borg-repo-url> [ -c hours ] [ -w hours ]

Hours must be an integer.

## Passwords

Export `BORG_PASSPHRASE`.

# Warnings

- Be sure about the implications, when monitoring a repository secured with a passphrase.
- I don't know how to exclude checkpoints in `borg list` in combination with `--format='{time}{NUL}'`.
