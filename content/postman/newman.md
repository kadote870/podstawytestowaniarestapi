# Newman CLI

* [Newman - Postman page](https://learning.postman.com/docs/collections/using-newman-cli/command-line-integration-with-newman/)
* [Newman - Git](https://github.com/postmanlabs/newman)
* [Newman HTML Extra](https://www.npmjs.com/package/newman-reporter-htmlextra)

## run tests

```text
newman run trello.json -e env.json
```

## run tests and generate htmlextra report

```text
newman run trello.json -e env.json -r htmlextra
```