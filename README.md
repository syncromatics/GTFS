GTFS Feed Parser
================

Fork of https://github.com/itinero/GTFS

.Net/Mono implementation of a General Transit Feed Specification (GTFS) feed parser. (see https://developers.google.com/transit/gtfs/reference)

[![Visit our website](https://img.shields.io/badge/website-itinero.tech-020031.svg) ](http://www.itinero.tech/)
[![MIT licensed](https://img.shields.io/badge/license-GPLv2-blue.svg)](https://github.com/itinero/GTFS/blob/develop/LICENSE)

[![Travis](https://img.shields.io/travis/syncromatics/GTFS.svg)](https://travis-ci.org/syncromatics/GTFS)
[![NuGet](https://img.shields.io/nuget/v/GTFS.svg)](https://www.nuget.org/packages/GTFS/)
[![NuGet Pre Release](https://img.shields.io/nuget/vpre/GTFS.svg)](https://www.nuget.org/packages/GTFS/)


The implementation is deliberate kept very flexible and customizable because many GTFS feeds out there all have their specific little perks.

### A short example
```
// create the reader.
var reader = new GTFSReader<GTFSFeed>();

// execute the reader.
using (
  var sources = new GTFSDirectorySource(new DirectoryInfo("path/to/feed/directory")))
{
  var feed = reader.Read(sources);
  ...
}
```

### Install GTFS

    PM> Install-Package GTFS
