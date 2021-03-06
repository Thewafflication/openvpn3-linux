====================
openvpn3-log-service
====================

----------------------
OpenVPN 3 Linux client
----------------------

:Manual section: 8
:Manual group: OpenVPN 3 Linux

SYNOPSIS
========
| ``openvpn3 log`` ``[OPTIONS]``
| ``openvpn3 log`` ``-h`` | ``--help``


DESCRIPTION
===========
This manages a few adjustable knobs available in the ``openvpn3-service-logger``
when run as a D-Bus service.  The access control for this command is managed in
the D-Bus policy, which by default is only allowed for the *root* and *openvpn*
user accounts.


OPTIONS
=======

-h, --help      Print  usage and help details to the terminal

--log-level LEVEL
                Sets the system wide log verbosity for the log events being
                logged to file or any other log destination
                ``openvpn3-service-logger`` is configured to use.  Valid values
                are *0* to *6*.  The higher value, the more verbose the log
                events will be.  Log level *6* will retrieve all debug events.

--timestamp true|false
                Some of the log destinations supported by
                ``openvpn3-service-logger`` may allow to log with or without
                timestamps.  This option enables or disables timestamps attached
                to log events.

--dbus-details true|false
                Each log event contains some more detailed meta-data of the
                sender of the log event.  This is disabled by default, but when
                enabled it will add an additional line on the log destination
                before the log event itself with this meta-data.  This is mostly
                only useful when debugging and not recommended for normal
                production.


SEE ALSO
========

``openvpn3``\(8)
``openvpn3-service-logger``\(8)
