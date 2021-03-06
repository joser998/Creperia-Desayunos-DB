# Creperia-Desayunos-DB

Java Desktop Application 
Jose Luis Ramirez

This Project contains: 
*Java Project.
*Connector JDBC.
*Database in MySQL WorkBench - DB-Breakfast. 
*Document with Requirements for the creation of this Software.

-Purpose for this software:
This Java Application has the objective, get the control for products (breakfast) for inventory and sales.
Im attaching here document: "Especificación de requerimientos del sistema.pdf" where i explain the entire problematic, 
requirements for this software and my solution with this Java app. 

-This Java Project it's done with this next Models and Technologies: 
  *Java SE: Java Standard Edition I'm using JDK14 wich is really stable in comparison with others new JDK
   
  *Java Swing Library:
   I use this library to be able to create components like buttons, text boxes, combo boxes, labels and manipulate
   images, all this components give to user a better experience and an easy one, because they dont need read to know how 
   application works, its really interactive and simple at the same time.
   
  *Free Images for icons in Frame:
   I am using images like icons and i'm giving some actions inside this program, this is for a better user experience.
   This images are completly free rigths, this is the page where you can find it:  https://unsplash.com
  
  *Connection with MySQL - WorkBench:
   In this application i'm using a database so i'm using MySQL connector and i'm stablising connection directly with MySQL.
   All the modifications i'm doing in this project are been saved in this Database, this is because i'm trying
   to be more efficient and comfortable for user, so i dont have to worry about loosing information at all.

  *Relational Databases:
   I am using three different tables in this project the first one is to get the registry for food, in this case breakfast
   and all the characteristics for this one like, quantity, price, register, cathegory, and description. 
   The second table is used to get the cathegory for breakfast and this one has a relation with first table, so if i delete
   just one cathegory because i'm not gonna use it anymore i'm also deleting all the breakfasts for this erased cathegory, not
   sales only breakfast register.
   The third table is used to get all the sales done for user, so i'm saving the breakfast name, sales quantity and payment by
   client all this information comunicates with first table (registry food) and do the appropiate update in quantities for product.
   
  *CRUD:
   I am using Queries for MySQL like Create, Read, Update and Delete.
   All the actions for this project are based in this sentences, this sentences are able to insert registers in Database, update or modify
   registers, return registers (products, cathegories, sales) and delete each one of this.
   All this sentences are able to connect with Database and do all the changes that user need anytime.
   
  *MVC(Model, View, Controller):
   One of the most important parts in the contruction for this project is the MVC Pattern, because this philosophy prettends divide all the 
   project in three phases.
   1.-Model: This one has the representation for all the data in the system, the business logical and the persistence. 
   2.-View: This one is the interface for user, it has comunications directly with user and receives all the requests, in this project the 
            view was used only to hide icons or show icons in the frame, also i used a small method to protect the text boxes for posible 
            wrong characters but all the logical and the controller code is not here in the view.
            This can bring us the posibility to replace really easy this components maybe for another ones or maybe just change the place 
            for this components and we are not depending entirely for this ones.
   3.-Controller: This one is working between model and view, managing all the information and transformations to adapt data for each one.
                  In this part, the code that i'm using are built by methods assigned to buttons for insert, modify or delete in the entire
                  application, all this code was used in communication with the model and view.
                  
                  
   The Application Starts in this way:
![image](https://user-images.githubusercontent.com/61565954/93434497-dcff0880-f88d-11ea-973d-2dba059d0f56.png)

  We can select any option in the Menu, but it is necessary register Category and Product so we can do the Sale...

               
 Now I'm inside the Menu "Registro"              
 ![image](https://user-images.githubusercontent.com/61565954/93435588-43d0f180-f88f-11ea-885a-d371938318bd.png)
 We can select Categoria or Desayuno and do the registry for each one of this.                 
                  
 I'm inside "Categoria" in this moment so i am doing the registry for a new kind of breakfast                 
![image](https://user-images.githubusercontent.com/61565954/93436175-0caf1000-f890-11ea-8f95-8f3d16de5465.png)  

I'm done with the first Category in this moment
![image](https://user-images.githubusercontent.com/61565954/93436585-9d85eb80-f890-11ea-95aa-8e7e8efd6078.png)
So the app shows me the new profile created and it's ready to save another Category in the Database

Here we are able to see the insertion for this new Category in MySQL WorkBench, so this first option is working perfectly
![image](https://user-images.githubusercontent.com/61565954/93437291-6e23ae80-f891-11ea-9510-8356063b154d.png)


![image](https://user-images.githubusercontent.com/61565954/93437895-25202a00-f892-11ea-8533-c9322209e68f.png)
In this moment i did a registry for breakfast and this is working good, i received a message telling me "Registro Insertado Correctamente"
to let know about this last action.


![image](https://user-images.githubusercontent.com/61565954/93438298-b8f1f600-f892-11ea-9909-b6f0b32c693e.png)
Breakfast saved on Database


In this image i am showing the "Buscar" Menu, so in the same way i can take a look for a register in Category or a Breakfast.
![image](https://user-images.githubusercontent.com/61565954/93501868-9cc67700-f8db-11ea-9cab-c341414a1afd.png)


Inside this last option i can find the breakfast or maybe not depending the register that i'm using it here, in this case i found the correct breakfast.
![image](https://user-images.githubusercontent.com/61565954/93502826-e1064700-f8dc-11ea-8470-5a2579b11e00.png)


Once i get the right register i am able to modify this same register or maybe just see all the attributes belonging on this plate
![image](https://user-images.githubusercontent.com/61565954/93503860-4870c680-f8de-11ea-864b-a466913d61d9.png)


In this only case i just changed the quantity for this product, imaging i did more of this in the business
![image](https://user-images.githubusercontent.com/61565954/93504218-cf25a380-f8de-11ea-975c-3ae41e3b99c0.png)


Here we are in the sales option, it is really simple and easy use this module...
I starting lookgin for the breakfast availability, if i am able to sale at least one of this the program asks me for the payment and it has to be 
the rigth payment o more than expected but never less, if the payment its more the programm tell me how much money i have to return to this client
![image](https://user-images.githubusercontent.com/61565954/93505351-5c1d2c80-f8e0-11ea-9fc0-f7bf0eadbb24.png)


Program asking for quantity
![image](https://user-images.githubusercontent.com/61565954/93509524-79a0c500-f8e5-11ea-991e-2258d087a8ab.png)


Wrong payment, program does not execute the sale
![image](https://user-images.githubusercontent.com/61565954/93509754-cd131300-f8e5-11ea-83df-fa6b34811cc2.png)


Correct payment, program tell user how much money needs to return to client
![image](https://user-images.githubusercontent.com/61565954/93510087-4d397880-f8e6-11ea-8906-2051d7f78049.png)


Database in MySQL Workbench, we can see the table Ventas and we have registered this last sale we did
![image](https://user-images.githubusercontent.com/61565954/93510508-e8325280-f8e6-11ea-8ed4-e9385d03ac9f.png)


In the same Menu we are able to delete the sale, here i'm trying to delete the last sale we did
![image](https://user-images.githubusercontent.com/61565954/93510821-71498980-f8e7-11ea-8380-477a450d26c1.png)


Sale deleted
![image](https://user-images.githubusercontent.com/61565954/93511097-dc935b80-f8e7-11ea-922d-c65b9b5ae9f5.png)


Also we are able to delete the register for the product (breakfast) or the Category if we need it, this is directly for inventory
![image](https://user-images.githubusercontent.com/61565954/93511261-2419e780-f8e8-11ea-8df9-03a038051f51.png)


Profile for this product deleted in Database too
![image](https://user-images.githubusercontent.com/61565954/93511532-97bbf480-f8e8-11ea-9c72-d597006b877e.png)

Also i would like to add, if we delete some category, we are deleting at same time all the products matched with this category 

Finally we have the option to close our app with this button "Exit" in this way
![image](https://user-images.githubusercontent.com/61565954/93512189-90e1b180-f8e9-11ea-82b8-ae5f96ceb0e7.png)
End Of Program
![image](https://user-images.githubusercontent.com/61565954/93512443-ecac3a80-f8e9-11ea-86ef-adcd9a15e929.png)


All the project is here in this repository including the Database in MySQL...

I invite you to check and test this application and do your own annotations and if you wanted collaborate and expand this Software

Regards...
               
               
                  
                  
                  
                  
                  
   
