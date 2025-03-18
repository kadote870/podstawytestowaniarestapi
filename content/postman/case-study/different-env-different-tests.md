# Case study: Different env - Different tests

```js
if (pm.environment.name = "Postman PROD") {

   // Przykładowe testy
   pm.test("Status code is 200", function () {
      pm.response.to.have.status(200);
   });

} else if (pm.environment.name = "Postman DEV") {

   // Przykładowe testy
   pm.test("Status code is 200", function () {
      pm.response.to.have.status(200);
   });

} else {

   // Przykładowe testy
   pm.test("Status code is 200", function () {
      pm.response.to.have.status(200);
   });

}
```

{{ site.data.element.license }}