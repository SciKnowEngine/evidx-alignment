## zerodayproducts-for-karma.jl

### PyTransforms
#### _item_id_
From column: _json_rep / itemId_
``` python
return "item/"+getValue("itemId")
```

#### _posted_date_iso_
From column: _json_rep / postedDate_
``` python
t =  getValue("postedDate")
return DM.iso8601date(t,"%d/%m/%Y")
 
```

#### _cdr_id_
From column: __id_
``` python
return getValue("_id")
```

#### _source_name_id_
From column: _source_name_
``` python
return getValue("source_name")
```

#### _marketplace_id_
From column: _json_rep / marketplaceId_
``` python
return "marketplace/" + getValue("marketplaceId")
```


### Semantic Types
| Column | Property | Class |
|  ----- | -------- | ----- |
| _cdr_id_ | `schema:source` | `memex:Exploit1`|
| _clusterName_ | `memex:hasType` | `memex:Exploit1`|
| _description_ | `schema:description` | `memex:Exploit1`|
| _itemCategory_ | `schema:category` | `memex:Exploit1`|
| _itemName_ | `schema:name` | `memex:Exploit1`|
| _item_id_ | `uri` | `memex:Exploit1`|
| _marketplace_id_ | `uri` | `memex:PersonOrOrganization1`|
| _posted_date_iso_ | `schema:datePosted` | `memex:Exploit1`|
| _sellingPriceUsd_ | `schema:price` | `schema:PriceSpecification1`|
| _source_name_id_ | `schema:publisher` | `memex:Exploit1`|


### Links
| From | Property | To |
|  --- | -------- | ---|
| `memex:Exploit1` | `schema:category` | `xsd:zero-day-exploit`|
| `memex:Exploit1` | `schema:priceSpecification` | `schema:PriceSpecification1`|
| `memex:Exploit1` | `schema:seller` | `memex:PersonOrOrganization1`|
| `schema:PriceSpecification1` | `schema:priceCurrency` | `xsd:USD`|