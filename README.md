# pc
php task manager

##### The project is not ready!

##### Coming soon...

#### How to use

Copy the project

    example: C:/apps/pc
    
Add "C:/apps/pc" to PATH system variable

In pc.cmd specify the path to php

    set php=path/to/php or php

Create a task in tasks.php

    $app->task('test', function() {
        // code...
    });
    
Call task in command line

    pc test
    
#### How to use with modules

    $app->task('concat', function() {
    
        $this->src('js/*.js');
        $this->next('concat', 'main.js');
        $this->dest(); // current directory
    
    });
    
* * *
    
#### App commands

All global commands start with a double dash

##### --init or --i

Create a directory in the user project

    .tools
    - pc
    -- modules
    -- tasks
    -- tasks.php
    -- config.php

##### --help or --h

Display help

* * *
    
#### PC API

##### src(globs)

Uses php glob function

##### dest(folder)

Saves the files in the specified directory

##### module(moduleName)

Load module

##### task(taskName)

Create a task

##### run(taskName)

Run task

##### next(moduleName, options)

Use module

##### config(index)

Returns a user configuration data

##### srcList()

It displays the selected files
