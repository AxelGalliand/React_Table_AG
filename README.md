
## Installation guide for the React Table AG plugin:

## 1. Prerequisites

- [NodesJS (**vestion 16**)] (https://nodejs.org/en/)

If you are working with several versions of NodeJS, we recommend you install [nvm](https://github.com/nvm-sh/nvm). This tool will allow you to easily manage your NodeJS versions.

the plugin need too data array :
 - first one for the columns section, you need a array of objects that use a 
    "dataField" for the type of the column,
    "text" for the name of the column,
    "sortOrder" for the boolean of the sorting (ASC = Ascending/alphabetic order and DSC = Descending/anti alphabetic order),
    "type" for string or date or number

    ex: 
    {
      dataField: 'firstName',
      text: 'First Name',
      sortOrder: "ASC",
      type: "String",
    },

 - second one for the data you want in the table, you'r object property must match with you'r dataField in the culumn array

    ex: 
    {
        "firstName": "Alice",
        "lastName": "LAROCHE",
        "dateBirth": "1990-12-05",
        "dateStart": "2015-09-20",
        "street": "12 avenue des roses"
    },

## 2. Call Part

For the calling, you need the too array in a props and call it like :

 <TableMaker columns={columns} rows={data}/>

## 3. Style Part

The style is simple for let you the liberty and the personalisation of the table. You can do it juste in adding the class name in the parent element of the table calling. All the name are simple for a good comprehension like : paginate; button; sizeSelect; columnTitle...