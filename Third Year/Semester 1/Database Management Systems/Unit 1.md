# Database Management Systems

## Unit 1: Introduction to DBMS

### Database Concepts
#### What is a database?
A database is a collection of interrelated data which has been organised in such a way that it can be easily retrieved and managed.

#### What is a database management system?
A DBMS is a set of programs used to store, retrieve and update data in a way that is both convenient and efficient. Database management systems are designed to manage large bodies of information.

#### Differentiate between a file processing system and a database management system.

| <u>**Category**</u>    | <u>**File Processing System**</u>                            | <u>**DBMS**</u>                                              |
| :--------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Data Redundancy**    | Duplicate copies of data may exist in multiple files, leading to redundant copies of the data. | In a DBMS, the data is integrated into a single database, which avoids data redundancy. |
| **Data Inconsistency** | Data inconsistency occurs when multiple copies of the data present in different files are not updated simultaneously. | Data inconsistency is avoided by removing data redundancy.   |
| **Data Sharing**       | It is difficult to share data in a traditional file processing system. | In a DBMS, data can easily be shared by different applications. |
| **Data Independence**  | In files, data is stored in a particular format. If this format is changed, then the program which processes this file will also need to be changed. | In a DBMS, the data structures of the database and the programs/applications used to access the data can be completely separated. |
| **Data Control**       | Since the data is de-centralised or distributed, the traditional file system does not have centralised data control. | A DBMS provides centralised data storage. Hence, keeping control on the data is very easy. |
| **Data Security**      | It is very difficult to enforce security checks and access rights. | Different users can have different levels of access to the data based on their roles, which provides strong security to the data. |
| **Data Concurrency**   | Simultaneous updation of the same data by multiple users may result in irrelevant results. | DBMSs have sub-systems to control concurrency problems.      |
| **Data Modelling**     | It is difficult to represent complex data and interfile relationships in a file system. This results in poor data modelling. | A DBMS provides functionalities to represent complex data and interfile relationships. |

