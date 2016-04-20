# easy-config-class

 This class is create or maintain the config key and value pair for your application, 
where you  will create any new key for your application, you can load any config file from the file under the config directory,
you also create the date wise log file with custom name



include "config.php"; // include the main class 

$con=  new EasyConfig(); // create  the config class object

$con->load("app_seting"); // load the your config file like app_setting.php

//$con->load("email_config"); // load any file from config directory, just pass the file  as parameter when you calling the load function of the config class

echo "<br>".DIR_PATH;
echo $con->set('APPLICATION_PATH',DIR_PATH); // set any new danamic key=> value pair for config setting for your application
echo $con->set('copyright_text','all &copy;  are reserved for EES'); // set any new danamic key=> value pair for config setting for your application
easy_debug_data($con->data); // display all key pair for the your application
echo $con->get('appname'); // get the single key value  from your configuration file
