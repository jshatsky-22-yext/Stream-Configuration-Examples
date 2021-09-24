## Example Configurations 

**mixedArray**: This example defines fields as an array. Non-object fields are defined with just the field name. Object fields are defined as objects.

**streamConfig.gql**: The GraphQL example configuration.

**gqlTypeExampleinJSON**: The JSON representation which matches the gql proposal very closely. In this example, fields is an object, and each individual field is a property of that object. The ```fields``` object can either be a list of strings for the simple case or an object mapping field name to configuration.

**simpleSyntheticFields**: This example extends our current stream configuration format, adding synthetic fields for each of the proposed new features. The user would have limited configuration. In this model, the listings, reviews, and reviewsAgg additional data is assumed to be an object keyed by publisher, so the user specifies {dataSource}.{publisher} to get a specific publisher. 

**simpleSyntheticFieldsWithSomeConfiguration**: This example is similar to *simpleSynthicFields*, but leverages a mixed array where each additional data source is an object, allowing for additional configuration. 

## Open Questions
* How generic does the format need to be?
* How much configuration is required per additional source?
* Do we like mixed arrays?
* Do we want to remove the current requirement to use dot notation to specify multiple fields from the same relationship? See *gqlTypeExampleinJSON* - currently, it's somewhat repititive to have to c_relationshipField.{field1}, c_relationshipField.{field2}, etc. 