# [Request For Comments] Head-Up, A Standard Status API For Web Service Providers #

The following describes the mandatory requirements that must be adhered to allow remote monitoring of service status.

## Overview ##

 * The `/up` resource is REQUIRED
 * The `/up` resource MUST be reserved for the status API
 * The `/up` resource MUST reflect the service health status from a user's point of view
 * The `/up` resource SHOULD BE updated often and regularly

## Basic Status Data ##

 * A fully operational system MUST respond `200 OK` to `GET /up` and `HEAD /up` requests.
 * A fully operational system MUST respond to `GET /up` and `HEAD /up` requests in timely fashion.
 * A non-fully operational system MUST NOT respond `200 OK` to `GET /up` and `HEAD /up` requests.
 * `GET /up` and `HEAD /up` requests MUST NOT return a 404 response code, whether the system is operational or not
 * The response to `GET /up` and `HEAD /up` requests MUST contain a `Last-Modified` header, which value corresponds to the last health check date.

## Discussion ##

 * Please use the [Head-Up Google Group](https://groups.google.com/d/forum/head-up) for discussion before posting any pull request
