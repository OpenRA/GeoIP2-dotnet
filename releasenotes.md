GeoIP2 .NET API Release Notes
=============================

2.1.0 (2014-11-06)
------------------

* Added support for the GeoIP2 Anonymous IP database. The `DatabaseReader`
  class now has an `AnonymousIP()` method which returns an
  `AnonymousIpResponse` object.

2.0.0 (2014-09-29)
------------------

* First production release.

0.5.0 (2014-09-24)
------------------

* The deprecated `CityIspOrg` and `Omni` methods were removed.
* `DatabaseReader` methods will now throw an `InvalidOperationException` when
  called for the wrong database type.
* `DatabaseReader` now has a `Metadata` property that provides an object
   containing the metadata for the open database.

0.4.0 (2014-07-22)
------------------

* The web service client API has been updated for the v2.1 release of the web
  service. In particular, the `CityIspOrg` and `Omni` methods on
  `WebServiceClient` have been deprecated. The `City` method now provides all
  of the data formerly provided by `CityIspOrg`, and the `Omni` method has
  been replaced by the `Insights` method.
* Support was added for the GeoIP2 Connection Type, Domain, and ISP databases.


0.3.3 (2014-06-02)
------------------

* Constructors with named parameters were added to the model and response
  classes. (Jon Wynveen)

0.3.2 (2014-04-09)
------------------

* A constructor taking a `Stream` was added to `DatabaseReader`.
* Fixed dependency on wrong version of `Newtonsoft.Json`.

0.3.1 (2014-02-13)
------------------

* Fixed broken error handling. Previously the wrong exceptions and error
  messages were returned for some web service errors.

0.3.0 (2013-11-15)
------------------

* API CHANGE: Renamed exceptions to remove GeoIP2 prefixes.
* Improved error messages when RestSharp does not return an HTTP status code.

0.2.0 (2013-10-25)
------------------

* First release with GeoIP2 database support. See `DatabaseReader` class.

0.1.1 (2013-10-04)
------------------

* Build documentation.

0.1.0 (2013-09-20)
------------------

* Initial release.
