# loopback

## Set UP

### Create a new Project

``` shell
slc loopback test_rest_api # Note, the creation of the project must happen in an empty directory
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

Server our content on: http://localhost:3000/explorer

``` shell
node .
```


## Result

The exposed landing page
![alt text](https://raw.githubusercontent.com/jkbngl/loopback/master/images/landing_page.png)

The main page of our model
![alt text](https://raw.githubusercontent.com/jkbngl/loopback/master/images/main_page.png	)

The result shown in the WEB-UI
![alt text](https://raw.githubusercontent.com/jkbngl/loopback/master/images/result.png)

The result shown as json reult
![alt text](https://raw.githubusercontent.com/jkbngl/loopback/master/images/production_result.png)

