# Postman code templates

## Main

```js
console.clear();
```

```js
const response = pm.response.json();
console.log(response)
```

```js
const response = pm.response.json()
const obj = {
    id: response.id,
    name: response.name
}
console.log(obj)
```

```js
pm.globals.set("key", value)
```

```js
const response = pm.response.json();
const userId = response.user.id
pm.globals.set("userId", userId)
```

```js
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

```js
pm.test("Your test name", function () {
    pm.expect(response.value).to.eql(100);
});
```

```js
const exampleDatas = []

for (const element of response) {
    if (element.value === condition) {
        exampleDatas.push(element);
    }
}

console.log(objects);
```

## Dynamic variable

```js
const someVariable = pm.variables.get("variable_key");
pm.globals.set("variable_key", someVariable);
```

```js
const a = pm.variables.replaceIn('{{$randomFirstName}}');
const b = pm.variables.replaceIn('{{$randomFirstName}} {{$randomLastName}}');

console.log(a)
console.log(b)
```

### Data

```js
const uuidV4 = pm.variables.replaceIn("{{$guid}}");
const timestamp = pm.variables.replaceIn("{{$timestamp}}");
const soTimestamp = pm.variables.replaceIn("{{$isoTimestamp}}");
const randomUUID = pm.variables.replaceIn("{{$randomUUID}}");
const randomAlphaNumeric = pm.variables.replaceIn("{{$randomAlphaNumeric}}");
const randomBoolean = pm.variables.replaceIn('{{$randomBoolean}}');
const randomInt = pm.variables.replaceIn('{{$randomInt}}'); // 1-1000
const randomColor = pm.variables.replaceIn('{{$randomColor}}');
const randomHexColor = pm.variables.replaceIn('{{$randomHexColor}}'); // "#47594a", "#431e48", "#106f21"
const randomAbbreviation = pm.variables.replaceIn('{{$randomAbbreviation}}'); // SQL, PCI, JSON
const randomIP = pm.variables.replaceIn('{{$randomIP}}'); // 241.102.234.100, 216.7.27.38
const randomIPV6 = pm.variables.replaceIn('{{$randomIPV6}}'); // dbe2:7ae6:119b:c161:1560:6dda:3a9b:90a9
const randomMACAddress = pm.variables.replaceIn('{{$randomMACAddress}}'); // 1f:6e:db:3d:ed:fa
const randomPassword = pm.variables.replaceIn('{{$randomPassword}}'); // t9iXe7COoDKv8k3, QAzNFQtvR9cg2rq
const randomUserAgent = pm.variables.replaceIn('{{$randomUserAgent}}'); // Mozilla/5.0 (Macintosh; U; Intel Mac OS X 10.9.8; rv:15.6) Gecko/20100101 Firefox/15.6.6
const randomProtocol = pm.variables.replaceIn('{{$randomProtocol}}'); // "http", "https"
const randomSemver = pm.variables.replaceIn('{{$randomSemver}}'); //  version number 7.0.5, 2.5.8, 6.4.9
```

### Names

```js
const randomFirstName = pm.variables.replaceIn('{{$randomFirstName}}');
const randomLastName = pm.variables.replaceIn('{{$randomLastName}}');
const randomFullName = pm.variables.replaceIn('{{$randomFullName}}');
const randomNamePrefix = pm.variables.replaceIn('{{$randomNamePrefix}}'); // Dr., Ms., Mr.
const randomPhoneNumber = pm.variables.replaceIn('{{$randomPhoneNumber}}');
const randomPhoneNumberExt = pm.variables.replaceIn('{{$randomPhoneNumberExt}}');
const randomCity = pm.variables.replaceIn('{{$randomCity}}');
const randomStreetName = pm.variables.replaceIn('{{$randomStreetName}}');
const randomStreetAddress = pm.variables.replaceIn('{{$randomStreetAddress}}');
const randomCountry = pm.variables.replaceIn('{{$randomCountry}}');
const randomCountryCode = pm.variables.replaceIn('{{$randomCountryCode}}');
const randomLatitude = pm.variables.replaceIn('{{$randomLatitude}}');
const randomLongitude = pm.variables.replaceIn('{{$randomLongitude}}');
```

### Data

```js
const uuidV4 = pm.variables.replaceIn('{{$guid}}');
const timestamp = pm.variables.replaceIn('{{$timestamp}}');
const soTimestamp = pm.variables.replaceIn('{{$isoTimestamp}}');
const randomUUID = pm.variables.replaceIn('{{$randomUUID}}');
const randomAlphaNumeric = pm.variables.replaceIn('{{$randomAlphaNumeric}}');
const randomBoolean = pm.variables.replaceIn('{{$randomBoolean}}');
const randomInt = pm.variables.replaceIn('{{$randomInt}}'); // 1-1000
const randomColor = pm.variables.replaceIn('{{$randomColor}}');
const randomHexColor = pm.variables.replaceIn('{{$randomHexColor}}'); // "#47594a", "#431e48", "#106f21"
const randomAbbreviation = pm.variables.replaceIn('{{$randomAbbreviation}}'); // SQL, PCI, JSON
const randomIP = pm.variables.replaceIn('{{$randomIP}}'); // 241.102.234.100, 216.7.27.38
const randomIPV6 = pm.variables.replaceIn('{{$randomIPV6}}'); // dbe2:7ae6:119b:c161:1560:6dda:3a9b:90a9
const randomMACAddress = pm.variables.replaceIn('{{$randomMACAddress}}'); // 1f:6e:db:3d:ed:fa
const randomPassword = pm.variables.replaceIn('{{$randomPassword}}'); // t9iXe7COoDKv8k3, QAzNFQtvR9cg2rq
const randomUserAgent = pm.variables.replaceIn('{{$randomUserAgent}}'); // Mozilla/5.0 (Macintosh; U; Intel Mac OS X 10.9.8; rv:15.6) Gecko/20100101 Firefox/15.6.6
const randomProtocol = pm.variables.replaceIn('{{$randomProtocol}}'); // "http", "https"
const randomSemver = pm.variables.replaceIn('{{$randomSemver}}'); // version number 7.0.5, 2.5.8, 6.4.9
```

### Images

```js
const randomAvatarImage = pm.variables.replaceIn('{{$randomAvatarImage}}');
const randomImageUrl = pm.variables.replaceIn('{{$randomImageUrl}}');
const randomAbstractImage = pm.variables.replaceIn('{{$randomAbstractImage}}');
const randomAnimalsImage = pm.variables.replaceIn('{{$randomAnimalsImage}}');
const randomBusinessImage = pm.variables.replaceIn('{{$randomBusinessImage}}');
const randomCatsImage = pm.variables.replaceIn('{{$randomCatsImage}}');
const randomCityImage = pm.variables.replaceIn('{{$randomCityImage}}');
const randomFoodImage = pm.variables.replaceIn('{{$randomFoodImage}}');
const randomFashionImage = pm.variables.replaceIn('{{$randomFashionImage}}');
const randomPeopleImage = pm.variables.replaceIn('{{$randomPeopleImage}}');
const randomNatureImage = pm.variables.replaceIn('{{$randomNatureImage}}');
const randomSportsImage = pm.variables.replaceIn('{{$randomSportsImage}}');
const randomNightlifeImage = pm.variables.replaceIn('{{$randomNightlifeImage}}');
const randomTransportImage = pm.variables.replaceIn('{{$randomTransportImage}}');
const randomImageDataUri = pm.variables.replaceIn('{{$randomImageDataUri}}');

```

### Finance

```js
const randomBankAccount = pm.variables.replaceIn('{{$randomBankAccount}}'); // 09454073, 65653440, 75728757
const randomBankAccountName = pm.variables.replaceIn('{{$randomBankAccountName}}'); // Home Loan Account, Checking Account, Savings Account. Auto Loan Account
const randomCreditCardMask = pm.variables.replaceIn('{{$randomCreditCardMask}}'); // 3622, 5815, 6257
const randomBankAccountIban = pm.variables.replaceIn('{{$randomBankAccountIban}}'); // MU20ZPUN3039684000618086155TKZ
const randomBankAccountBic = pm.variables.replaceIn('{{$randomBankAccountBic}}'); // EZIAUGJ1, KXCUTVJ1, DIVIPLL1
const randomTransactionType = pm.variables.replaceIn('{{$randomTransactionType}}'); // invoice, payment, deposit
const randomCurrencyCode = pm.variables.replaceIn('{{$randomCurrencyCode}}'); // CDF, ZMK, GNF
const randomCurrencyName = pm.variables.replaceIn('{{$randomCurrencyName}}'); // CFP Franc, Cordoba Oro, Pound Sterling
const randomCurrencySymbol = pm.variables.replaceIn('{{$randomCurrencySymbol}}'); // $, £
const randomBitcoin = pm.variables.replaceIn('{{$randomBitcoin}}'); // bitcoin address 3VB8JGT7Y4Z63U68KGGKDXMLLH5
```

### Business

```js
const randomCompanyName = pm.variables.replaceIn('{{$randomCompanyName}}');
const randomCompanySuffix = pm.variables.replaceIn('{{$randomCompanySuffix}}'); // Inc, LLC, Group
const randomBs = pm.variables.replaceIn('{{$randomBs}}'); // killer leverage schemas, bricks-and-clicks deploy markets, world-class unleash platforms
const randomBsAdjective = pm.variables.replaceIn('{{$randomBsAdjective}}'); // viral, 24/7, 24/365
const randomBsBuzz = pm.variables.replaceIn('{{$randomBsBuzz}}'); // repurpose, harness, transition
const randomBsNoun = pm.variables.replaceIn('{{$randomBsNoun}}'); // e-services, markets, interfaces
```

### Catchphrases

```js
const randomCatchPhrase = pm.variables.replaceIn('{{$randomCatchPhrase}}'); // Future-proofed heuristic open architecture
const randomCatchPhraseAdjective = pm.variables.replaceIn('{{$randomCatchPhraseAdjective}}'); // Self-enabling, Business-focused, Down-sized
const randomCatchPhraseDescriptor = pm.variables.replaceIn('{{$randomCatchPhraseDescriptor}}'); // bandwidth-monitored, needs-based, homogeneous
const randomCatchPhraseNoun = pm.variables.replaceIn('{{$randomCatchPhraseNoun}}'); // secured line, superstructure,installation
```

### Databases

```js
const randomDatabaseColumn = pm.variables.replaceIn('{{$randomDatabaseColumn}}'); // updatedAt, token, group
const randomDatabaseType = pm.variables.replaceIn('{{$randomDatabaseType}}'); // A random database column name
const randomDatabaseCollation = pm.variables.replaceIn('{{$randomDatabaseCollation}}'); //  cp1250_bin, utf8_general_ci, cp1250_general_ci
const randomDatabaseEngine = pm.variables.replaceIn('{{$randomDatabaseEngine}}'); // MyISAM, InnoDB, Memory
```

### Dates

```js
const randomDateFuture = pm.variables.replaceIn('{{$randomDateFuture}}'); // Tue Mar 17 2020 13:11:50 GMT+0530 (India Standard Time),
const randomDatePast = pm.variables.replaceIn('{{$randomDatePast}}'); // Sat Mar 02 2019 09:09:26 GMT+0530 (India Standard Time),
const randomDateRecent = pm.variables.replaceIn('{{$randomDateRecent}}'); // Tue Jul 09 2019 23:12:37 GMT+0530 (India Standard Time),
const randomWeekday = pm.variables.replaceIn('{{$randomWeekday}}'); // Thursday, Friday, Monday
const randomMonth = pm.variables.replaceIn('{{$randomMonth}}'); // February, May, January
```

### Domains, emails, and usernames

```js
const randomDomainName = pm.variables.replaceIn('{{$randomDomainName}}'); // gracie.biz, armando.biz, trevor.info
const randomDomainSuffix = pm.variables.replaceIn('{{$randomDomainSuffix}}'); // org, net, com
const randomDomainWord = pm.variables.replaceIn('{{$randomDomainWord}}'); // gwen, jaden, donnell
const randomEmail = pm.variables.replaceIn('{{$randomEmail}}'); // Pablo62@gmail.com, Ruthe42@hotmail.com, Iva.Kovacek61@hotmail.com
const randomExampleEmail = pm.variables.replaceIn('{{$randomExampleEmail}}'); // Talon28@example.com, Quinten_Kerluke45@example.net, Casey81@example.net
const randomUserName = pm.variables.replaceIn('{{$randomUserName}}'); // Jarrell.Gutkowski, Lottie.Smitham24, Alia99
const randomUrl = pm.variables.replaceIn('{{$randomUrl}}'); // https://anais.net, https://tristin.net, http://jakob.name
```

### Files and directories

```js
const randomFileName = pm.variables.replaceIn('{{$randomFileName}}'); // neural_sri_lanka_rupee_gloves.gdoc, plastic_awesome_garden.tif,
const randomFileType = pm.variables.replaceIn('{{$randomFileType}}'); //model, application, video
const randomFileExt = pm.variables.replaceIn('{{$randomFileExt}}'); // war, book, fsc
const randomCommonFileName = pm.variables.replaceIn('{{$randomCommonFileName}}'); // well_modulated.mpg4, rustic_plastic_tuna.gif,
const randomCommonFileType = pm.variables.replaceIn('{{$randomCommonFileType}}'); // application, audio
const randomCommonFileExt = pm.variables.replaceIn('{{$randomCommonFileExt}}'); // m2v, wav, png
const randomFilePath = pm.variables.replaceIn('{{$randomFilePath}}'); // /home/programming_chicken.cpio,
const randomDirectoryPath = pm.variables.replaceIn('{{$randomDirectoryPath}}'); // /usr/bin, /root, /usr/local/bin
const randomMimeType = pm.variables.replaceIn('{{$randomMimeType}}'); // audio/vnd.vmx.cvsd, application/vnd.groove-identity-message
```

### Stores

```js
const randomPrice = pm.variables.replaceIn('{{$randomPrice}}'); // 0.00 and 1000.00	531.55, 488.76, 511.56
const randomProduct = pm.variables.replaceIn('{{$randomProduct}}'); // Towels, Pizza, Pants
const randomProductAdjective = pm.variables.replaceIn('{{$randomProductAdjective}}'); // Unbranded, Incredible, Tasty
const randomProductMaterial = pm.variables.replaceIn('{{$randomProductMaterial}}'); // Steel, Plastic, Frozen
const randomProductName = pm.variables.replaceIn('{{$randomProductName}}'); // Handmade Concrete Tuna, Refined Rubber Hat
const randomDepartment = pm.variables.replaceIn('{{$randomDepartment}}'); // Tools, Movies, Electronics
```

### Grammar

```js
const randomNoun = pm.variables.replaceIn('{{$randomNoun}}'); // matrix, bus, bandwidth
const randomVerb = pm.variables.replaceIn('{{$randomVerb}}'); // parse, quantify, navigate
const randomIngverb = pm.variables.replaceIn('{{$randomIngverb}}'); // synthesizing, navigating, backing up
const randomAdjective = pm.variables.replaceIn('{{$randomAdjective}}'); // auxiliary, multi-byte, back-end
const randomWord = pm.variables.replaceIn('{{$randomWord}}'); // withdrawal, infrastructures, IB
const randomWords = pm.variables.replaceIn('{{$randomWords}}'); // A random phrase	You can't program the monitor without navigating the mobile XML program!, overriding the capacitor won't do anything, we need to compress the optical SMS transmitter!, I'll generate the virtual AI program, that should microchip the RAM monitor!
```

### Lorem ipsum

```js
const randomPhrase = pm.variables.replaceIn('{{$randomPhrase}}');
const randomLoremWord = pm.variables.replaceIn('{{$randomLoremWord}}');
const randomLoremWords = pm.variables.replaceIn('{{$randomLoremWords}}');
const randomLoremSentence = pm.variables.replaceIn('{{$randomLoremSentence}}');
const randomLoremSentences = pm.variables.replaceIn('{{$randomLoremSentences}}');
const randomLoremParagraph = pm.variables.replaceIn('{{$randomLoremParagraph}}');
const randomLoremParagraphs = pm.variables.replaceIn('{{$randomLoremParagraphs}}');
```

```js
const randomLoremText = pm.variables.replaceIn('{{$randomLoremText}}');
const randomLoremSlug = pm.variables.replaceIn('{{$randomLoremSlug}}');
const randomLoremLines = pm.variables.replaceIn('{{$randomLoremLines}}');
```