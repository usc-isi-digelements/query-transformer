# query-transformer

A Polymer Element that makes a POST request via `<iron-ajax>` element and transforms the data returned with a function specified by the user. This is an alternative to using the elastic-client-search component, in case your end point is a different data store or webservice.

```html
    <query-transformer
      search-on-empty-params
      error="{{searchError}}"
      loading="{{searchLoading}}"
      page="1"
      page-size="5"
      process-request="[[processRequest]]"
      result-function="[[resultFunction]]"
      results="{{searchResults}}"
      total="{{totalCount}}"
      search-parameters="[[searchParameters]]"
      search-function="[[searchFunction]]"
      url="http://localhost:9200/mockads/ad/_search">
    </query-transformer>
```

### Dependencies

Dependencies are installed using [Bower](http://bower.io/):

    npm install -g bower
    bower install

### Testing

Tests are run using [web-component-tester](https://github.com/Polymer/web-component-tester):

    npm install -g web-component-tester
    wct

### Demonstration & Documentation

Demonstration and documentation are viewed using [polyserve](https://github.com/PolymerLabs/polyserve):

    npm install -g polyserve
    polyserve

The demo will require a local instance of elasticsearch with the `mockads` index created by running `data/import_test_data.sh`.
