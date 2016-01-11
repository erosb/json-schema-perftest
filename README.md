JSON Schema Validator performance test
======================================

This library provides a skeletal performance test suite for this JSON Schema Validator library:
https://github.com/everit-org/json-schema

It contains the same test suite: https://github.com/fge/json-schema-validator/wiki/Performance


Test results & comparison to the fge/json-schema-validator library
------------------------------------------------------------------

For testing the performance of the `fge/json-schema-validator` library I've used [this main class](https://github.com/fge/json-schema-validator/blob/master/src/test/java/com/github/fge/jsonschema/NewAPIPerfTest.java) .

I ran the testsuite of both libraries 10 times (each execution performing 500 validations).

Tests results on my local computer:

|   |fge|everit-org |
|---|---|-----------|
|min|6655 ms|1583 ms|
|max|7611 ms|2006 ms|
|avg|7178 ms|1699 ms|

Running the tests on other workstations gave a bit different numbers but similar ratios.

Running the tests
-----------------

Clone this repository:

`git clone https://github.com/erosb/json-schema-perftest.git`

Build the project with Maven:

`cd json-schema-perftest/`
`mvn clean install -Pdist`

Run the test:

`java -jar target/perftest.jar`
