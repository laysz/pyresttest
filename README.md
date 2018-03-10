## How to use PyRestTest to test APIs

PyRestTest official page: https://github.com/svanoort/pyresttest

--------------------------------------------------------------------------------------------
Example on US Tax Gateway API for RMSg project.
--------------------------------------------------------------------------------------------


PASSED test:
```bash
$ pyresttest http://qa-rmsg-api.stg.jp.local r10_ustaxgw.yaml --import_extensions 'find_in_json'
Test Group Default SUCCEEDED: : 5/5 Tests Passed!
```


FAILED test:
```bash
$ pyresttest http://qa-rmsg-api.stg.jp.local r10_ustaxgw.yaml --import_extensions 'find_in_json'

[('server', 'openresty'), ('date', 'Thu, 18 Jan 2018 06:58:10 GMT'), ('transfer-encoding', 'chunked'), ('connection', 'close'), ('x-request-id', 'f19050d4-fc1c-11e7-83a5-54ab3a295732'), ('x-application-context', 'gep-tax-gateway-api:qa:31906')]
ERROR:Test Failed: GET category-codes: EXAMPLE OF FAILED TEST URL=http://qa-rmsg-api.stg.jp.local/ustaxgw/v1/category-codes Group=Default HTTP Status Code: 400
ERROR:Test Failure, failure type: Invalid HTTP Response Code, Reason: Invalid HTTP response code: response code 400 not in expected codes [[200]]
Test Group Default FAILED: : 5/6 Tests Passed!
```
----------------------------------------------------------------------------------------------
Example for sample app for RAPID CRUD merchants
----------------------------------------------------------------------------------------------

```bash
resttest.py  http://rapid-samples-crud-spring-boot-crud.rwasp-stg.hnd2.bdd.local CRUDLifecycleTest.yaml --absolute-urls 
Test Group Lifecycle SUCCEEDED: : 8/8 Tests Passed!
```
# This a few tests I wrote for pyresttest framework
