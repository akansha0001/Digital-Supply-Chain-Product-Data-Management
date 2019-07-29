# Digital-Supply-Chain-Product-Data-Management
Created a UI to manage the creation of new MBOM from given EBOM by overriding attributes, deleting attributes and adding a new attribute.
to run this first import database in MySQL
database dell.sql which contain the following table 
1.login
      attribute:
          1.mid
          2.password
2.mbominfo
      attribute:
          1.mbom_name(primary key)
3.newebom
     attribute:
          1.serial_no(primary key)
          2.Company 
          3.Product 
          4.TypeName 
          5.Inches 
          6.ScreenResolution 
          7.CPU
          8.RAM
          9.Memory
 
4.new table name mbom will be created with serial no as foreign key mbom from newebom. And attribute will be those selected by manager from newebom and some other attributes for packaging as well.
    
          
The first page is dell.php which users style.css which is linked to pages login.php which is for the login of managers. login.php is linked to server.php which fetches data from the login table. After login successfully, choice.php page will open. 
Choice.php has 4 options:
      1.add new attribute to m-bom
      2.delete attribute to m-bom
      3.modify mbom
      4.view mbom.
      5.back(go to the homepage that is dell.php)
1. It opens add.php which will add selected attribute selected in mbom using a checkbox. Manager can select the component suggested by an engineer. This page is connected to backend using serveradd.php page. serveradd.php creates a new table named mbom with attribute selected by the manager. It also updates the mbominfo table. It is then linked to addmbom_page.php. This page is similar to add.php But it option for packaging i.e(  silicone keyboard guard,  laptop bag, charger provided,   user manual, quantity) It is connected to packaging.php for updating backend. It updates mbominfo table and adds more attribute in mbom table. After pressing the submit button it goes back to  choice.php page.
2. It is linked to delete.php page which has a checkbox. It asks for attribute to be deleted. For updating backend, it is connected to deletembom.php.
3. It is used to update mbom. It is a form on the basis of an attribute name and serial no it updates the table. For updating table, it is linked with update.php.
4.view mbom: This page is linked to view_mbom.html and fetch mbom from mbom table and shows it in the table.
