PHP DAO scaffolder

This is web application for creating DAO objects from your DB (MySQL) tables

1) start index.php inside PHPDAO folder and give credentials and access to your
   database, these data will be stored inside 'models/DAO/DA.php' file for later
   use by classes
2) then PHP DAO will read all tables from given schema an ask you to select what
   tables should be included in build (creating DAO classes) and what are object
   names: singular is used for this object, plural for reference by other objects
3) then PHP DAO will read all columns for selected tables, show their attributes
   and you have to select what columns should be included in build and for which
   columns finders should be generated (indexed columns are selected by default)
4) core dao classes will be created inside modules/DAO folder, and working classes
   that extend them will be create inside modules folder. Every time when you run
   PHP DAO generator it will overwrite core classes inside 'modules/DAO/' folder
   and make backup of existing ones. Module classes inside modules folder (they
   should contain your own business logic) will not be overwritten. This way you
   can regenerate your DAO core classes upon every DB model change.




