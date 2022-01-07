#!/bin/sh

# pinentry-switcher: Simple pinetry program to change pinentry tools
# Copyright (C) 2022  Amlesh Sivanantham

# choose pinentry depending on PINENTRY_USER_DATA environment variable
# this *only works* with gpg 2, ssh.
# see https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=802020

#echo "PINENTRY_USER_DATA=<${PINENTRY_USER_DATA}>, options=<$@>" >> \
#    /tmp/pinentry.log

case $PINENTRY_USER_DATA in
    qt)
        exec /usr/bin/pinentry-qt4 "$@"
        ;;
    tty)
        exec /usr/bin/pinentry-tty "$@"
        ;;
    rofi)
        exec /usr/bin/pinentry-rofi "$@"
        ;;
    none)
        echo "pinentry-switcher Error"
        exit 1 # do not ask for passphrase
        ;;
    *)
        exec /usr/bin/pinentry "$@"
        ;;
esac
