NAME
====

gas_price_de_ - Graph gas prices of gas stations in germany with munin
by using the http://tanken.t-online.de API

PREREQUISITES
=============

This plugin uses the "xmllint" program provided by 
libxml2 (http://www.xmlsoft.org) and the "wget" utility
(http://www.gnu.org/software/wget/)

CONFIGURATION
=============

The filename must be in this format: gas_price_de_latitude_longitude 
 latitude must be the exact latitude of the gas station
 longitude must be the exact longitude of the gas station

The following environment variables are used by this plugin
 
* fuel_type - The type of fuel. Supported values are:
--* diesel
--* super _[default]_
--* super%20e10
--* superplus
--* autogas
--* biodiesel
--* lkw-diesel
--* dieselplus

CONFIGURATION EXAMPLES
----------------------

 [gas_price_de_52.527567_13.416131]
  env.fuel_type autogas

AUTHOR
======

Copyright (C) 2013 D.Hiepler

LICENSE
=======

GPLv2

