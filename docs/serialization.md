# SerializeWith(serializer)

When leveraging our serialization system, most datatype serialization concerns are managed by the base classes such as DatatypeBase, AliaseDatatypeBase, and StructuredDatatypeBase.

These classes facilitate the automatic serialization of information based on the abstract properties you define. In the examples provided below, we illustrate how datatypes are serialized, assuming the use of the JsonSerializer class. This overview aims to give you a practical understanding of what the serialization output looks like for both primitive and structured datatypes. Whether you're working with basic types or more complex structures, the mobject-types will automate much of the serialization (and deserialization) for you if you use the provided base types.

## Primatives

Example of a BOOL.

```json
{ "name": "BOOL" }
```

Example of a INT.

```json
{ "name": "INT" }
```

## Structures

Example of TIMESTRUCT.

```json
{
  "identifier": "TIMESTRUCT",
  "name": "STRUCT",
  "members": {
    "wDay": {
      "name": "WORD"
    },
    "wDayOfWeek": {
      "name": "WORD"
    },
    "wHour": {
      "name": "WORD"
    },
    "wMilliseconds": {
      "name": "WORD"
    },
    "wMinute": {
      "name": "WORD"
    },
    "wMonth": {
      "name": "WORD"
    },
    "wSecond": {
      "name": "WORD"
    },
    "wYear": {
      "name": "WORD"
    }
  }
}
```

## Enums

TBA

## Alias

Example of HRESULT

```json
{
  "identifier": "HRESULT",
  "name": "ALIAS",
  "baseDatatype": {
    "name": "DINT"
  }
}
```

## Unions

TBA

## Interfaces

TBA
