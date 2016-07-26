# slimphp
An example of the use of the Slim PHP framework with GET and POST calls

To be used it needs:
1) to be inserted into htdocs folder of XAMPP;
2) to recall a MySQL database "slimdb" with params (username: "root", password: "") 
3) this DB must have a "book" table with id (INT PRIMARY KEY AUTOINCREMENT), book_title (VARCHAR 250), author (VARCHAR 250), amazon_url (VARCHAR 250);
4) when everything it's on its own place, you have to start Apache Server and MySQL Server through the control panel of XAMPP;
5) go to the browser and write the URLS:

HTTP GET METHODS:
http://localhost/againslim/public/index.php/hello/{name}
http://localhost/againslim/public/index.php/hi/{name}
http://localhost/againslim/public/index.php/api/books
http://localhost/againslim/public/index.php/api/books/{index}


HTTP POST METHODS:
http://localhost/againslim/public/index.php/hello   (POST: String "name")
http://localhost/againslim/public/index.php/hi     (POST: String "name")
http://localhost/againslim/public/index.php/api/books/insert (POST String "book_title", String "author", String "amazon_url")
http://localhost/againslim/public/index.php/api/books/insertJson (POST Json Array {"book_title":"title", "author": "Autore", "amazon_url": "www.blabla.com"})
http://localhost/againslim/public/index.php/api/books/insertJsonString (POST a String encoded from JSON with the same format of above)


