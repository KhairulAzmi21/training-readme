# MINI PROJECT ( PATIENT MANAGEMENT )

## Objective
* New Patient Registration
* List All Patient Registered
* View Patient Details
* Ability to search sort patient record ( Datatables yajra )
* RBAC ( Roles Based Access Control )
* Log Error to Slack

### Create New Project
```sh
$ laravel new project
```

### Database
* users table ( id, email, password, user_type, remember_me, created_at, updated_at )
* patient_informations table 
```sh
    Schema::create('patients', function (Blueprint $table) {
            $table->increments('id');
            $table->integer('patient_type');
            $table->string('name');
            $table->string('gender');
            $table->string('birthDate');
            $table->string('bloodGroup');
            $table->string('mobile')->nullable;
            $table->string('email')->nullable();
            $table->string('address');
            $table->integer('employee_id');
            $table->timestamps();
        });
```
* roles and permissions table
    * we will use Laravel Spatie 
    * reference : https://github.com/spatie/laravel-permission
    * reference : https://laravel-news.com/two-best-roles-permissions-packages

### Yajra Datatables
> This package is created to handle server-side works of [datatables](https://datatables.net/) jQuery Plugin via AJAX option by using Eloquent ORM, Fluent Query Builder or Collection.

* reference : https://github.com/yajra/laravel-datatables

### Laravel Log To Slack
* https://laravel.com/docs/5.6/logging

### Others 

#### Bootstrap 4 scripts
```sh
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.0/css/bootstrap.min.css" integrity="sha384-9gVQ4dYFwwWSjIDZnLEWnxCjeSWFphJiwGPXr1jddIhOegiu1FwO5qRGvFXOdJZ4" crossorigin="anonymous">
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.0/js/bootstrap.min.js" integrity="sha384-uefMccjFJAIv6A+rW+L4AHf99KvxDjWSu1z9VI8SKNVmz4sk7buKt/6v9KI65qnm" crossorigin="anonymous"></script>
```

#### jQuery
```sh
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.0/umd/popper.min.js" integrity="sha384-cs/chFZiN24E4KMATLdqdvsezGxaGsi4hLGOzlXwp5UZB1LY//20VyM2taTB4QvJ" crossorigin="anonymous"></script>
```

#### Datatables
* reference : https://datatables.net/examples/styling/bootstrap4
* reference : https://datatables.net/examples/basic_init/zero_configuration.html

###### Javascript
#
```sh
https://cdn.datatables.net/1.10.19/js/jquery.dataTables.min.js
https://cdn.datatables.net/1.10.19/js/dataTables.bootstrap4.min.js
```

###### CSS
#
```sh
https://cdn.datatables.net/1.10.19/css/dataTables.bootstrap4.min.css
```




