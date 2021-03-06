---
description: >-
  The Appsmith platform includes Javascript utility libraries, which can be used
  to work with data within `{{ }}` bindings.
---

# Working with JS libraries

## Included JS libraries

The following JS libraries are supported in the Appsmith platform.

* [lodash](https://lodash.com/docs/4.17.15)
* [moment](https://momentjs.com/docs/)
* [btoa](https://github.com/dankogai/js-base64#readme)
* [atob](https://github.com/dankogai/js-base64#readme)

## Using JS libraries

The utility functions provided by the included libraries can be used when transforming data.

### Example: lodash

An example of lodash's `_.map` utility, in use.

```javascript
{{
  _.map(fetchFruits.data, (fruit) => { 
    return { label: fruit.name, value: fruit.id } 
    })
}}

// fetchFruits is the name of the API / Query
```

### Example: moment

An example of moment's `format` utility, in use in a Table's data property.

```javascript
{{
  _.map(getTickets.data, (ticket) => ({
      label: ticket.name,
      description: ticket.desc,
      displayDate: moment(ticket.created_date).format("L")  // user friendly display date
    }))
}}

// getTickets is the name of the API / Query
```

