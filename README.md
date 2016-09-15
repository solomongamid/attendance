# attendace app

- A staff Management Application for all working days.
- Objective to control times, dates of arrivals.
- We have two types of use:
   1. Users
   2. Administrator that controls the database

## Prerequisites

-- Database: `ATS_SPC`
--

-- --------------------------------------------------------

--
-- Table structure for table `checkins`
--

CREATE TABLE IF NOT EXISTS `checkins` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `arrival_time` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `full_name` varchar(100) COLLATE latin1_bin NOT NULL,
  `date_a` date NOT NULL,
  `checks` varchar(100) COLLATE latin1_bin NOT NULL,
  `user_id` int(11) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM  DEFAULT CHARSET=latin1 COLLATE=latin1_bin AUTO_INCREMENT=101 ;

-- ---------------------------------------------------------  

-- Table structure for table `users`
--

CREATE TABLE IF NOT EXISTS `users` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(100) COLLATE latin1_bin NOT NULL,
  `surname` varchar(100) COLLATE latin1_bin NOT NULL,
  `email` varchar(200) COLLATE latin1_bin NOT NULL,
  `passcode` varchar(100) COLLATE latin1_bin NOT NULL,
  `session` date NOT NULL,
  `admin` int(11) NOT NULL,
  `username` varchar(100) COLLATE latin1_bin NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 COLLATE=latin1_bin AUTO_INCREMENT=19 ;


-- ----------------------------------------------------------

- in `config.php` and `configer.php` files:
```php
define('DB_SERVER', 'localhost'); // Host name
define('DB_USERNAME', 'YOUR-USER-NAME'); // Mysql username
define('DB_PASSWORD', 'YOUR-PASSWORD'); // Mysql password
define('DB_DATABASE', 'ATS_SPC'); // Database name
```
-- ---------------------------------------------------------- 
## Mockups

![main.png ](mockups/main.png )
![mainfr.png ](mockups/mainfr.png )
![adminfr.png ](mockups/adminfr.png )
![adminlist.png](mockups/adminlist.png)
![reportdate.png ](mockups/reportdate.png )
![searchdate.png ](mockups/searchdate.png )
![searchname.png ](mockups/searchname.png )
![regestration.png](mockups/regestration.png)
![empmain.png ](mockups/empmain.png )
![emppage.png ](mockups/emppage.png )

