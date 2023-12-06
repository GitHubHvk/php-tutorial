# How to install PHP

1. go to site ((**https://www.php.net/downloads**))
2. click on (([Windows downloads](https://windows.php.net/download#php-8.3)))
3. download latest version of ((Thread Safe)) in zip format.
4. extract downloaded zip file to the path ((C:\Program Files\php-8.3.0-Win32-vs16-x64))
5. add path ((C:\Program Files\php-8.3.0-Win32-vs16-x64)) to the itme ((path)) in system variables of environment variables.



## Test PHP Installation 

open a CMD and run following command:

```powershell
php -v
```

this command should print current version of installed php.



## Test PHP working

in a folder for example ((d:\test)) create a file ((index.php)) and copy one of following content to it:

```php+HTML
<!DOCTYPE html>
<html>
<body>

<h1>My first PHP page</h1>

<?php
echo "Hello World!";
?>

<br/>
    
<h1>Installed PHP INFO:</h1>
<hr/>
<?php
phpinfo();
?>

</body>
</html>
```



then open a CMD and cd to the path ((d:\test)) and run the following command:

```powershell
php -S localhost:8000
```



now open web browser and navigate to the address ((http://localhost:8000/index.php)), this should browse a web page that consist a ((Hello World message)) and some info about installed PHP.



# Installing Apache

1. download Visual C++ Redistributable from ((https://aka.ms/vs/17/release/VC_redist.x64.exe)).

2. install Visual C++ Redistributable.

3. browse web page ((https://www.apachelounge.com/download/)).

4. download the zip file of latest Apache.

5. extract zip file in the default location defined in conf file, which is ((c:/Apache24)).

   1. if you want to extract it to another folder, for example ((D:\MyApache)), you should change the value of ((SRVROOT)) variable inside file ((C:\Apache24\conf\httpd.conf)) to ((D:\MyApache))

6. open file ((C:\Apache24\conf\httpd.conf)) and change the port in variable ((Listen)) to whatever you want. as an example to ((8090)).

7. open CMD and cd to the path ((C:\Apache24\bin)), and run the following command:

   ```powershell
   httpd
   ```

8. open a web browser and navigate to ((http://localhost:8090/)); this should browse you the content of the page that is reside in ((C:\Apache24\htdocs\index.html)) which is a text message as ((It works!))