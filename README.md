# Pinentry Switcher

`pinentry-switcher` is a pinetry tool that lets you switch between pinentry
tools using an environment variable `$PINENTRY_USER_DATA` instead of having
to update the symbolic link.

Supported pinetry programs:

- **pinentry-qt**
- **pinentry-tty**
- [**pinentry-rofi**](https://github.com/zamlz/pinentry-rofi.git)

If the environment variable is not recognized, it will default to using your
system's pinentry.
