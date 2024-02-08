# Seralization Notes

This is a work in progress. The information below is a guide to common serialization patterns used.

## Primative

```json
{
  "type": "BOOL"
}
```

## Structures

```json
{
  "name": "MachineSettings",
  "type": "STRUCT",
  "fields": [
    {
      "name": "Enabled",
      "type": "BOOL"
    },
    {
      "name": "Speed",
      "type": "INT",
      "defaultValue": 123
    }
  ]
}
```

## Enums

```json
{
  "name": "MachineState",
  "type": "ENUM",
  "baseType": "DINT",
  "attributes": ["qualified_only", "strict"],
  "members": [
    {
      "name": "STOPPED",
      "value": 0
    },
    {
      "name": "RUNNING",
      "value": 1
    }
  ],
  "defaultValue": "STOPPED"
}
```

## Alias

```json
{
  "name": "Speed",
  "type": "ALIAS",
  "baseType": "INT"
}
```

## Unions

```json
{
  "name": "Buffer",
  "type": "UNION",
  "members": [
    {
      "name": "AsWord",
      "type": "WORD"
    },
    {
      "name": "AsBytes",
      "type": "ARRAY",
      "elementType": "BYTE",
      "dimensions": [
        {
          "lowerBound": 0,
          "upperBound": 1
        }
      ]
    }
  ]
}
```

## Interfaces

```json
{
  "name": "I_Echo",
  "type": "INTERFACE",
  "methods": [
    {
      "name": "Echo",
      "returnType": "STRING",
      "parameters": [
        {
          "name": "input",
          "type": "STRING"
        }
      ]
    }
  ]
}
```

## Other

```json
// when adding an array to a UDT

{
	"name": "AsBytes",
	"type": "ARRAY",
	"elementType": "BYTE",
	"dimensions": [
	{
		"lowerBound": 0,
		"upperBound": 1
	}
	]
}

// when items have default values

{
  "name": "MachineSettings",
  "type": "STRUCT",
  "fields": [
    {
      "name": "Enabled",
      "type": "BOOL",
      "defaultValue": true
    },
    {
      "name": "SpeedSetpoints",
      "type": "ARRAY",
      "elementType": "INT",
      "dimensions": [
        {
          "lowerBound": 0,
          "upperBound": 3
        }
      ],
      "defaultValue": [1, 2, 3, 4]
    }
  ]
}

```
