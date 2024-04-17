# Changelog

## v0.2.0-alpha

- mobject-types change name to mobject-datatypes
- SerializeTypeWith refactored the following:
  - baseType -> baseDatatype
  - datatype -> name
  - isFloat added
- DatatypeBase has Datatype renamed to Name
- TryResolveAsAliasType renamed to TryResolveAsAliasDatatype
- TryResolveAsEnumType renamed to TryResolveAsEnumDatatype
- TryResolveAsStructuredType renamed to TryResolveAsStructuredDatatype
- Datatypes now supports adding enums
- Alias and Enums method names changed from Type to Datatype

## v0.1.2-alpha

- Corrected copy paste error, in which ULINT and UWORD were being treated as LINT when their bounds were serialized.

## v0.1.1-alpha

- Added mobject-converters 1.1.0
- Added Accept method to Datatypes to allow visitors
- Added I_EventEmitter to I_Datatypes
- Added event "OnDatatypeAdded" to Datatypes
- Added upper and lower bounds to integer datatypes
- Added new IntegerDatatypeBase
- Added IsSigned to integer datatypes
- Added enum datatype and tests

## v0.1.0-alpha

- Initial
