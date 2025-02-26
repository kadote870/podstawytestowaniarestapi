## Examples
* [Rebel-pl generowanie adresów url](../postman/examples/rebel-pl.md)
* [Zestawy testów zależnie od kodu HTTP](../postman/examples/200-400-response-codes-tests.md)
* [Using the REST Client VSCode Plugi](https://www.youtube.com/watch?v=RcxvrhQKv8I)

```js
// UUID random gen
const uuidGen = require('uuid');
const uuid = uuidGen.v4()
pm.globals.set("uuid", uuid);

// random number from variable
const pageNumberRandom = Math.floor(Math.random() * globals.numPages) + 1;


// some tests
pm.test("name", function () {
    pm.expect(response[engine1].id).to.be.an("array");
});
pm.test("2. Validation: jsonData.data - array", function () {
    pm.expect(jsonData.data).to.be.an("array");
});
pm.test("Value: jsonData.meta.page is correct ", function () { 
        pm.expect(jsonData.meta.page).is.to.equal(1); 
    });  
pm.test("Value: jsonData.meta.hasNext is correct ", function () { 
        pm.expect(jsonData.meta.hasNext).is.to.equal(false); 
    });
pm.test("6. Validation: jsonData.data[0].auction_id - number", function () {
    pm.expect(jsonData.data[0].auction_id).to.be.a("number");
});
pm.test("7. Validation: jsonData.data[0].serial - string", function () {
    pm.expect(jsonData.data[0].serial).to.be.a("string");
});
 

// timeout
setTimeout(() => {}, 1000)
 
// clg request name + env
console.log('Request: ' + pm.info.requestName , 'env: ' + pm.environment.name )
```

```js
// Wybierz jedno z dwóch
const a = 10
const b = 5
console.log([a+a,a+b][Math.round(Math.random())])

// Przkykład z playwright - kliknij jedno z dwóch
await page.click([commonSelectors.errorWindow.button.close, commonSelectors.errorWindow.button.closeCircle][Math.round(Math.random())]);

// Losowy index z tablicy
const engine = Math.floor(Math.random() * (response.length - 1));

// dice roll
function dice_roll(dice) {
        return Math.floor(Math.random() * dice + 1);
};

// rando number
export function random_number(min, max) {
        return Math.floor(Math.random() * (max - min) + min);
}

// zwykła
const randomNum1 = Math.floor(Math.random() * 10 + 1);
// zaokrąglona liczba - zwracana jako string
const randomNum2 = Math.floor(Math.random() * (30 - 25) + 25).toFixed(2);
```