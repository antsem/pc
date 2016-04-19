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