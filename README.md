# multiple-services-for-Mysql
How to set a default Mysql service with Windows

Do you have multiple xampp or servers ? 
Do you have a wampserver and a xampp server ?
Do you have a wamp/xampp server and have mysql installed lonely on your machine ?

You maybe want to launch mysql from a server A but server B mysql or lonely installed mysql is launched instead.

To fix that, you can define in windows the default running service of mysql.

## Open the Registry Editor
Steps:
* win + r
![image](https://user-images.githubusercontent.com/96789008/199275200-c3d40efb-a66e-42cb-ae56-e5e561175673.png)
* type: regedit then enter
![image](https://user-images.githubusercontent.com/96789008/199275520-1f5d2751-de60-4b13-8614-df3eb954be34.png)
The Register Editor is opened 
![image](https://user-images.githubusercontent.com/96789008/199276068-ce3c3909-9658-4173-989d-1a1f942ad45b.png)

## Go to Services : HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services
You can type Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services in the Address bar
![image](https://user-images.githubusercontent.com/96789008/199276449-d4bed8be-2db2-4f08-8039-235a6811ad6a.png)

## Then Select the Mysql Service
![image](https://user-images.githubusercontent.com/96789008/199276857-508118a9-ffaa-4453-ab91-6f72c5a90f18.png)

## Double-click on the ImagePath variable
 ![image](https://user-images.githubusercontent.com/96789008/199277304-8bd49794-b8a4-4db9-a136-a24db2db2998.png)

## Set the value data to the mysqld.exe you want to launch when starting Mysql services
You can see the mysqld location in <mysql_you_want_to_launch>/bin/mysqld.exe

Hope that helps you.
