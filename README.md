NAME
====

gas_price_de_

DESCRIPTION
===========

Graph prices of certain fuel types at gas stations within an area (defined by center 
and radius) in germany using with munin. This uses the http://tanken.t-online.de API.

PREREQUISITES
=============

This plugin uses the "xmllint" program provided by 
libxml2 (http://www.xmlsoft.org) and the "wget" utility
(http://www.gnu.org/software/wget/)

CONFIGURATION
=============

The filename must be in this format: gas_price_de_ID with
ID being a freely choosable string to allow creating 
multiple graphs and to set the title of the graph. ID may be empty.

The following environment variables are used by this plugin

* latitude - center latitude of area to query   [52.527567]
* longitude - center longitude of area to query [13.416131]
* radius - size of area (in kilometer)          [1]
* fuel_type - The type of fuel                  [super]
  * diesel
  * super _[default]_
  * super%20e10
  * superplus
  * autogas
  * biodiesel
  * lkw-diesel
  * dieselplus

CONFIGURATION EXAMPLES
----------------------

<pre>
[gas_price_de_*]
  env.latitude 52.527567
  env.longitude 13.416131
  env.radius 5
  env.fuel_type autogas
</pre>

AUTHOR
======

Copyright (C) 2013 D.Hiepler

LICENSE
=======

GPLv2
