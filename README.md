# Zamiana String | Znajdź i Zamień String

Program znajdzie i zamieni wszystkie String w twoich plikach projektowych.

## Użycie

### Przykład pracy

Przykład ten zamieni 'hello' na 'world' we w wszystkich twoich plikach projektowych.

```yaml
name: My Workflow
on: [push, pull_request]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: Find and Replace
      uses: shitiomatic/str-replace@master
      with:
        find: "hello"
        replace: "world"
```

### Inputs

| Wejście                                             | Opis                                       |
|------------------------------------------------------|-----------------------------------------------|
| `find`  | String do znalezienia i zamiany w twoim projekcie
| `replace`  | String do zamiany

### Outputs

| Wyjście                                             | Opis                                       |
|------------------------------------------------------|-----------------------------------------------|
| `modifiedFiles`  | Liczba plików, które zostały zmodyfikowane  |

