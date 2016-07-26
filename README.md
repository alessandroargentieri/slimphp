# slimphp
An example of the use of the Slim PHP framework with GET and POST calls

To be used it needs:
1) to be unzipped;
2) to be inserted into htdocs folder of XAMPP;
3) to recall a MySQL database "slimtestdb" with params (username: "root", password: "") 
4) this DB must have a "book" table with id (INT PRIMARY KEY AUTOINCREMENT), book_title (VARCHAR 250), author (VARCHAR 250), amazon_url (VARCHAR 250);
5) when everything it's on its own place, you have to start Apache Server and MySQL Server through the control panel of XAMPP;
6) go to the browser and write the URL of the api you want to test:

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




DUMP slimtestdb:
*********************
-- Database: `slimtestdb`

-- Struttura della tabella `books`

CREATE TABLE `books` (
  `id` int(11) NOT NULL,
  `book_title` varchar(250) NOT NULL,
  `author` varchar(250) NOT NULL,
  `amazon_url` varchar(250) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
--
-- Dump dei dati per la tabella `books`

INSERT INTO `books` (`id`, `book_title`, `author`, `amazon_url`) VALUES
(1, 'The four hour work week', 'Tim Ferris', 'www.amazon.com?id=3628'),
(2, 'Tomato Chips', 'Zoe Malis', 'www.amazon.com?id=3629'),
(3, 'Building priorities', 'Joe Attanada', 'www.amazon.com?id=3630'),
(4, 'Rutherless', 'Mai Chi Ling', 'www.amazon.com?id=1233'),
(6, 'Niagara', 'Robbinson Mary', 'www.amazon.com?id=2111'),
(7, 'Ladder Mimic', 'Phany Orton', 'www.amazon.com?id=3323');

--
-- Indici per le tabelle scaricate

-- Indici per le tabelle `books`
--
ALTER TABLE `books`
  ADD PRIMARY KEY (`id`);
--
-- AUTO_INCREMENT per le tabelle scaricate
--
-- AUTO_INCREMENT per la tabella `books`
--
ALTER TABLE `books`
  MODIFY `id` int(11) NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=8;

*********************


