# Library-System 
(library_id number(10),library_addressnumber(10),library_name varchar2(50),library_details varchar2(50));
Inser into libraries (library_id,library_address,library_name,library_details)
Values(1,1,'Al amal library','next to my factory');
Inser into libraries (library_id,library_address,library_name,library_details)
Values(2,1,' Cairo library','next to my house');
Inser into libraries (library_id,library_address,library_name,library_details)
Values(3,1,Alex library','next to my factory');
Hot to get number of  library in my database?
Select count(*) from library;
How to update data library(Cairo)?
Update library
Set library_name='al rahman'
Where library_id=2;



How to delete library(Al Amal)?
Delete from library
Where library_id=1
Hot to create to Book and insert data in this table
Create table Book
(isbn number(10),Book_title varchar2(50),date_of_publication date);
Insert into books (isbn,Book_title,date_of_publication)
Values(1,'Database',to_date('13/6/2020','dd/mm/yyyy'));
Insert into books (isbn,Book_title,date_of_publication)
Values(2,'Programming',to_date('13/6/2020','dd/mm/yyyy'));
Insert into books (isbn,Book_title,date_of_publication)
Values(3,'Network',to_date('13/6/2020','dd/mm/yyyy'));
Hot to get number of  Book in my database?
Select count(*) from Book;
How to update data Book(Database)?
Update Book
Set Book_name='IT Book'
Where Book_id=1;
How to delete Book(Database)?
Delete from Book
Where Book_id=1





Many Queries to use in this program:(Select Statement)
How get all books to begin with the character 'a'?
Select book name,date_of_publication,library_name
From books,libraries,book_at_libraries
Where books.isbn= book_at_libraries.isbn
And book_at_libraries.library_id=libraries.library_id
And upper(library_name) like upper('%a%');
How get all Libraries?
Select library_name,library_details,city
From libraries,addresses
Where library.address_id=addresses.address_id;
How to get the auther name of the book with id =1?
Select from books ,Authers,Book_by_auther
Where books.isbn= Book_by_auther.isbn
And Book_by_auther.auther_id=Authers.auther_id
And book_id=1;
statements of count and Group functions
-select count(*)from Books
-select max(Book_id),Book_id
Group by Book_id
