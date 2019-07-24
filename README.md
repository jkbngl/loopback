# loopback

## Set UP

### Create a new Project

``` shell
mkdir test_rest_api
slc loopback test_rest_api
cd test_rest_api
```

### Create a Datasource

First we need to install the needed connector:

``` shell
npm install --save loopback-connector-postgresql
``` 

Then

``` shell
slc loopback:datasource tpDS

? Enter the data-source name: tpDS
? Select the connector for tpDS: PostgreSQL (supported by StrongLoop)
Connector-specific configuration:
? Connection String url to override other settings (eg: postgres://username:password@localhost/database): postgres://postgres:test@localhost/postgres
? host: localhost
? port: 5432
? user: postgres
? password: ****
? database: postgres
```

### Create a Model

``` shell
slc loopback:model tp_exercise

? Enter the model name: tp_exercise
? Select the data-source to attach tp_exercise to: tpDS (postgresql)
? Select model's base class PersistedModel
? Expose tp_exercise via the REST API? Yes
? Custom plural form (used to build REST URL): tp_exercises
? Common model or server only? common
Let's add some tp_exercise properties now.

Enter an empty property name when done.
? Property name: id
   invoke   loopback:property
? Property type: number
? Required? Yes
? Default value[leave blank for none]:

Let's add another tp_exercise property.
Enter an empty property name when done.
? Property name: name
   invoke   loopback:property
? Property type: string
? Required? Yes
? Default value[leave blank for none]:

Let's add another tp_exercise property.
Enter an empty property name when done.
? Property name:
```

### Start up our rest api

``` shell
node .
```


## Result


