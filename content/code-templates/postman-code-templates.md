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
const uuidV4 = pm.variables.replaceIn("{{ site.data.postman.guid }}");
const timestamp = pm.variables.replaceIn("{{ site.data.postman.timestamp }}");
const soTimestamp = pm.variables.replaceIn("{{ site.data.postman.isoTimestamp }}");
const randomUUID = pm.variables.replaceIn("{{ site.data.postman.randomUUID }}");
const randomAlphaNumeric = pm.variables.replaceIn("{{ site.data.postman.randomAlphaNumeric }}");
const randomBoolean = pm.variables.replaceIn('{{ site.data.postman.randomBoolean }}');
const randomInt = pm.variables.replaceIn('{{ site.data.postman.randomInt }}'); // 1-1000
const randomColor = pm.variables.replaceIn('{{ site.data.postman.randomColor }}');
const randomHexColor = pm.variables.replaceIn('{{ site.data.postman.randomHexColor }}'); // "#47594a", "#431e48", "#106f21"
const randomAbbreviation = pm.variables.replaceIn('{{ site.data.postman.randomAbbreviation }}'); // SQL, PCI, JSON
const randomIP = pm.variables.replaceIn('{{ site.data.postman.randomIP }}'); // 241.102.234.100, 216.7.27.38
const randomIPV6 = pm.variables.replaceIn('{{ site.data.postman.randomIPV6 }}'); // dbe2:7ae6:119b:c161:1560:6dda:3a9b:90a9
const randomMACAddress = pm.variables.replaceIn('{{ site.data.postman.randomMACAddress }}'); // 1f:6e:db:3d:ed:fa
const randomPassword = pm.variables.replaceIn('{{ site.data.postman.randomPassword }}'); // t9iXe7COoDKv8k3, QAzNFQtvR9cg2rq
const randomUserAgent = pm.variables.replaceIn('{{ site.data.postman.randomUserAgent }}'); // Mozilla/5.0 (Macintosh; U; Intel Mac OS X 10.9.8; rv:15.6) Gecko/20100101 Firefox/15.6.6
const randomProtocol = pm.variables.replaceIn('{{ site.data.postman.randomProtocol }}'); // "http", "https"
const randomSemver = pm.variables.replaceIn('{{ site.data.postman.randomSemver }}'); // version number 7.0.5, 2.5.8, 6.4.9
```

### Names

```js
const randomFirstName = pm.variables.replaceIn('{{ site.data.postman.randomFirstName }}');
const randomLastName = pm.variables.replaceIn('{{ site.data.postman.randomLastName }}');
const randomFullName = pm.variables.replaceIn('{{ site.data.postman.randomFullName }}');
const randomNamePrefix = pm.variables.replaceIn('{{ site.data.postman.randomNamePrefix }}'); // Dr., Ms., Mr.
const randomPhoneNumber = pm.variables.replaceIn('{{ site.data.postman.randomPhoneNumber }}');
const randomPhoneNumberExt = pm.variables.replaceIn('{{ site.data.postman.randomPhoneNumberExt }}');
const randomCity = pm.variables.replaceIn('{{ site.data.postman.randomCity }}');
const randomStreetName = pm.variables.replaceIn('{{ site.data.postman.randomStreetName }}');
const randomStreetAddress = pm.variables.replaceIn('{{ site.data.postman.randomStreetAddress }}');
const randomCountry = pm.variables.replaceIn('{{ site.data.postman.randomCountry }}');
const randomCountryCode = pm.variables.replaceIn('{{ site.data.postman.randomCountryCode }}');
const randomLatitude = pm.variables.replaceIn('{{ site.data.postman.randomLatitude }}');
const randomLongitude = pm.variables.replaceIn('{{ site.data.postman.randomLongitude }}');
```

### Images

```js 
const randomAvatarImage = pm.variables.replaceIn('{{ site.data.postman.randomAvatarImage }}');
const randomImageUrl = pm.variables.replaceIn('{{ site.data.postman.randomImageUrl }}');
const randomAbstractImage = pm.variables.replaceIn('{{ site.data.postman.randomAbstractImage }}');
const randomAnimalsImage = pm.variables.replaceIn('{{ site.data.postman.randomAnimalsImage }}');
const randomBusinessImage = pm.variables.replaceIn('{{ site.data.postman.randomBusinessImage }}');
const randomCatsImage = pm.variables.replaceIn('{{ site.data.postman.randomCatsImage }}');
const randomCityImage = pm.variables.replaceIn('{{ site.data.postman.randomCityImage }}');
const randomFoodImage = pm.variables.replaceIn('{{ site.data.postman.randomFoodImage }}');
const randomFashionImage = pm.variables.replaceIn('{{ site.data.postman.randomFashionImage }}');
const randomPeopleImage = pm.variables.replaceIn('{{ site.data.postman.randomPeopleImage }}');
const randomNatureImage = pm.variables.replaceIn('{{ site.data.postman.randomNatureImage }}');
const randomSportsImage = pm.variables.replaceIn('{{ site.data.postman.randomSportsImage }}');
const randomNightlifeImage = pm.variables.replaceIn('{{ site.data.postman.randomNightlifeImage }}');
const randomTransportImage = pm.variables.replaceIn('{{ site.data.postman.randomTransportImage }}');
const randomImageDataUri = pm.variables.replaceIn('{{ site.data.postman.randomImageDataUri }}');
```

### Finance

```js
const randomBankAccount = pm.variables.replaceIn('{{ site.data.postman.randomBankAccount }}'); // 09454073, 65653440, 75728757
const randomBankAccountName = pm.variables.replaceIn('{{ site.data.postman.randomBankAccountName }}'); // Home Loan Account, Checking Account, Savings Account. Auto Loan Account
const randomCreditCardMask = pm.variables.replaceIn('{{ site.data.postman.randomCreditCardMask }}'); // 3622, 5815, 6257
const randomBankAccountIban = pm.variables.replaceIn('{{ site.data.postman.randomBankAccountIban }}'); // MU20ZPUN3039684000618086155TKZ
const randomBankAccountBic = pm.variables.replaceIn('{{ site.data.postman.randomBankAccountBic }}'); // EZIAUGJ1, KXCUTVJ1, DIVIPLL1
const randomTransactionType = pm.variables.replaceIn('{{ site.data.postman.randomTransactionType }}'); // invoice, payment, deposit
const randomCurrencyCode = pm.variables.replaceIn('{{ site.data.postman.randomCurrencyCode }}'); // CDF, ZMK, GNF
const randomCurrencyName = pm.variables.replaceIn('{{ site.data.postman.randomCurrencyName }}'); // CFP Franc, Cordoba Oro, Pound Sterling
const randomCurrencySymbol = pm.variables.replaceIn('{{ site.data.postman.randomCurrencySymbol }}');
const randomBitcoin = pm.variables.replaceIn('{{ site.data.postman.randomBitcoin }}'); // bitcoin address 3VB8JGT7Y4Z63U68KGGKDXMLLH5
```

### Business

```js 
const randomCompanyName = pm.variables.replaceIn('{{ site.data.postman.randomCompanyName }}');
const randomCompanySuffix = pm.variables.replaceIn('{{ site.data.postman.randomCompanySuffix }}'); // Inc, LLC, Group
const randomBs = pm.variables.replaceIn('{{ site.data.postman.randomBs }}'); // killer leverage schemas, bricks-and-clicks deploy markets, world-class unleash platforms
const randomBsAdjective = pm.variables.replaceIn('{{ site.data.postman.randomBsAdjective }}'); // viral, 24/7, 24/365
const randomBsBuzz = pm.variables.replaceIn('{{ site.data.postman.randomBsBuzz }}'); // repurpose, harness, transition
const randomBsNoun = pm.variables.replaceIn('{{ site.data.postman.randomBsNoun }}'); // e-services, markets, interfaces
```

### Catchphrases

```js
const randomCatchPhrase = pm.variables.replaceIn('{{ site.data.postman.randomCatchPhrase }}'); // Future-proofed heuristic openarchitecture
const randomCatchPhraseAdjective = pm.variables.replaceIn('{{ site.data.postman.randomCatchPhraseAdjective }}'); // Self-enabling,Business-focused, Down-sized
const randomCatchPhraseDescriptor = pm.variables.replaceIn('{{ site.data.postman.randomCatchPhraseDescriptor }}'); //bandwidth-monitored, needs-based, homogeneous
const randomCatchPhraseNoun = pm.variables.replaceIn('{{ site.data.postman.randomCatchPhraseNoun }}'); // secured line,superstructure,installation
```

### Databases

```js 
const randomDatabaseColumn = pm.variables.replaceIn('{{ site.data.postman.randomDatabaseColumn }}'); // updatedAt, token, group
const randomDatabaseType = pm.variables.replaceIn('{{ site.data.postman.randomDatabaseType }}'); // A random database column name
const randomDatabaseCollation = pm.variables.replaceIn('{{ site.data.postman.randomDatabaseCollation }}'); // cp1250_bin,utf8_general_ci, cp1250_general_ci
const randomDatabaseEngine = pm.variables.replaceIn('{{ site.data.postman.randomDatabaseEngine }}'); // MyISAM, InnoDB, Memory
```

### Dates

```js
const randomDateFuture = pm.variables.replaceIn('{{ site.data.postman.randomDateFuture }}'); // Tue Mar 17 2020 13:11:50 GMT+0530 (India Standard Time),
const randomDatePast = pm.variables.replaceIn('{{ site.data.postman.randomDatePast }}'); // Sat Mar 02 2019 09:09:26 GMT+0530 (India Standard Time),
const randomDateRecent = pm.variables.replaceIn('{{ site.data.postman.randomDateRecent }}'); // Tue Jul 09 2019 23:12:37 GMT+0530 (India Standard Time),
const randomWeekday = pm.variables.replaceIn('{{ site.data.postman.randomWeekday }}'); // Thursday, Friday, Monday
const randomMonth = pm.variables.replaceIn('{{ site.data.postman.randomMonth }}'); // February, May, January
```

### Domains, emails, and usernames

```js 
const randomDomainName = pm.variables.replaceIn('{{ site.data.postman.randomDomainName }}'); // gracie.biz, armando.biz, trevor.info
const randomDomainSuffix = pm.variables.replaceIn('{{ site.data.postman.randomDomainSuffix }}'); // org, net, com
const randomDomainWord = pm.variables.replaceIn('{{ site.data.postman.randomDomainWord }}'); // gwen, jaden, donnell
const randomEmail = pm.variables.replaceIn('{{ site.data.postman.randomEmail }}'); // Pablo62@gmail.com, Ruthe42@hotmail.com,Iva.Kovacek61@hotmail.com
const randomExampleEmail = pm.variables.replaceIn('{{ site.data.postman.randomExampleEmail }}'); // Talon28@example.com,Quinten_Kerluke45@example.net, Casey81@example.net
const randomUserName = pm.variables.replaceIn('{{ site.data.postman.randomUserName }}'); // Jarrell.Gutkowski, Lottie.Smitham24, Alia99
const randomUrl = pm.variables.replaceIn('{{ site.data.postman.randomUrl }}'); // https://anais.net, https://tristin.net, http://jakob.name
```

### Files and directories

```js
const randomFileName = pm.variables.replaceIn('{{ site.data.postman.randomFileName }}'); // neural_sri_lanka_rupee_gloves.gdoc,plastic_awesome_garden.tif,
const randomFileType = pm.variables.replaceIn('{{ site.data.postman.randomFileType }}'); //model, application, video
const randomFileExt = pm.variables.replaceIn('{{ site.data.postman.randomFileExt }}'); // war, book, fsc
const randomCommonFileName = pm.variables.replaceIn('{{ site.data.postman.randomCommonFileName }}'); // well_modulated.mpg4,rustic_plastic_tuna.gif,
const randomCommonFileType = pm.variables.replaceIn('{{ site.data.postman.randomCommonFileType }}'); // application, audio
const randomCommonFileExt = pm.variables.replaceIn('{{ site.data.postman.randomCommonFileExt }}'); // m2v, wav, png
const randomFilePath = pm.variables.replaceIn('{{ site.data.postman.randomFilePath }}'); // /home/programming_chicken.cpio,
const randomDirectoryPath = pm.variables.replaceIn('{{ site.data.postman.randomDirectoryPath }}'); // /usr/bin, /root, /usr/local/bin
const randomMimeType = pm.variables.replaceIn('{{ site.data.postman.randomMimeType }}'); // audio/vnd.vmx.cvsd,application/vnd.groove-identity-message
```

### Stores

```js 
const randomPrice = pm.variables.replaceIn('{{ site.data.postman.randomPrice }}'); // 0.00 and 1000.00 531.55, 488.76, 511.56
const randomProduct = pm.variables.replaceIn('{{ site.data.postman.randomProduct }}'); // Towels, Pizza, Pants
const randomProductAdjective = pm.variables.replaceIn('{{ site.data.postman.randomProductAdjective }}'); // Unbranded, Incredible, Tasty
const randomProductMaterial = pm.variables.replaceIn('{{ site.data.postman.randomProductMaterial }}'); // Steel, Plastic, Frozen
const randomProductName = pm.variables.replaceIn('{{ site.data.postman.randomProductName }}'); // Handmade Concrete Tuna, Refined Rubber Hat
const randomDepartment = pm.variables.replaceIn('{{ site.data.postman.randomDepartment }}'); // Tools, Movies, Electronics
```

### Grammar

```js
const randomNoun = pm.variables.replaceIn('{{ site.data.postman.randomNoun }}'); // matrix, bus, bandwidth
const randomVerb = pm.variables.replaceIn('{{ site.data.postman.randomVerb }}'); // parse, quantify, navigate
const randomIngverb = pm.variables.replaceIn('{{ site.data.postman.randomIngverb }}'); // synthesizing, navigating, backing up
const randomAdjective = pm.variables.replaceIn('{{ site.data.postman.randomAdjective }}'); // auxiliary, multi-byte, back-end
const randomWord = pm.variables.replaceIn('{{ site.data.postman.randomWord }}'); // withdrawal, infrastructures, IB
const randomWords = pm.variables.replaceIn('{{ site.data.postman.randomWords }}'); // A random phrase You can't program the monitor without navigating the mobile XML program!, overriding the capacitor won't do anything, we need to compress the optical SMS transmitter!, I'll generate the virtual AI program, that should microchip the RAM monitor!
```

### Lorem ipsum

```js 
const randomPhrase = pm.variables.replaceIn('{{ site.data.postman.randomPhrase }}');
const randomLoremWord = pm.variables.replaceIn('{{ site.data.postman.randomLoremWord }}');
const randomLoremWords = pm.variables.replaceIn('{{ site.data.postman.randomLoremWords }}');
const randomLoremSentence = pm.variables.replaceIn('{{ site.data.postman.randomLoremSentence }}');
const randomLoremSentences = pm.variables.replaceIn('{{ site.data.postman.randomLoremSentences }}');
const randomLoremParagraph = pm.variables.replaceIn('{{ site.data.postman.randomLoremParagraph }}');
const randomLoremParagraphs = pm.variables.replaceIn('{{ site.data.postman.randomLoremParagraphs }}');

const randomLoremText = pm.variables.replaceIn('{{ site.data.postman.randomLoremText }}');
const randomLoremSlug = pm.variables.replaceIn('{{ site.data.postman.randomLoremSlug }}');
const randomLoremLines = pm.variables.replaceIn('{{ site.data.postman.randomLoremLines }}');
```

{{ site.data.element.license }}