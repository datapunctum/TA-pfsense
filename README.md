# Technology Add-on for pfsense

**Author:** Datapunctum GmbH

**Version:**

* @version@

**Supported products:**

* pfsense >= 2.2.0

**Supported CIM Version:**

* &gt;=4.0.0

**Supported CIM Datamodels:**

* Authentication
* Network Traffic

**Sourcetypes:**

* `pfsense:filterlog`
* `pfsense:dhcpd`
* `pfsense:openvpn`
* `pfsense:nginx`
* `pfsense:unbound`
* `pfsense:*`

**Add-on contains:**

* Search and Parsing-Time configuration

**Input requirements:**

* This release requires pfsense to send data in syslog format
* Adjust pfsense sed replacements to remove duplicate timestamps / or set `no_appending_timestamp = true` in inputs.conf for udp input

## Using this Technology Add-on

* The add-on has to be installed on Search Heads
* If data is collected through Intermediate Heavy Forwarders, it has to be installed on Heavy Forwarders, otherwise on indexers
* The add-on expects an initial sourcetype named `pfsesnse`, the sourcetype will be transformed into more specific ones (see sourcetype list)
* A sample `inputs.conf` is provided (`default/inputs.conf.sample`)

## Compatibility

* Compatible with pfsense 2.2.0 or higher

## Release Notes

* **2.0.0 / 2015-03-10** mbo

  * First release to support new logformat
  * License Update to Apache

* **2.1.0 / 2017-05-17** mbo

  * Basic Nginx Support
  * Basic Unbound Support

* **2.2.0 / 2019-09-22** mbo

  * Additional support for pfsense =>2.4.0

## Change Log

* **2.2.0 / 2019-09-22** mbo

  * Additional Extracts for igmp and hbh
  * Fixed some timestamp stripping issues
  * Rebuild Build Process
