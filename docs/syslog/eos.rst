.. _syslog-eos:

==========
Arista EOS
==========

In general, the structure of the syslog messages generated by EOS has the
following format:

``<PRI><datetime> <hostname> <process-name>: %<facility-name>-<severity>-<tag>: <MSG>``

Where:

- ``hostname``: The device that generated the message. To ensure that the hostname is included, follow the instructions from :ref:`device-configuration-eos`.
- ``datetime``: The time when the message was generated in the format: ``MMM dd hh:mm:ss``.
- ``process-name``: The name of the process that generated the mesage.
- ``facility-name``: The name of the Facility.
- ``severify``: The value of the Severity.
- ``tag``: The syslog message tag.

Examples:

``<149>Apr 16 11:04:17 edge01 Rib: %BGP-3-NOTIFICATION: received from neighbor 194.53.172.97 (AS 2611) 6/1 (Cease/maximum number of prefixes reached) 0 bytes
``
