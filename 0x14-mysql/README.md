# 0x14. MySQL
CREATE USER 'replica_user'@'%' IDENTIFIED BY '@Buddy000'

GRANT SELECT ON *.* TO holberton_user@localhost;

FLUSH PRIVILEGES;

cat -- script that creates a table called first_table in the current database in your MySQL server.
    -> CREATE TABLE first_table
    -> (
    -> id INT(5),
    -> name VARCHAR(256)
    -> ); | mysql -hlocalhost -uroot -p tyrell_corp

    -- script that creates a table called first_table in the current database in your MySQL server.
CREATE TABLE nexus6
(
id INT,
name VARCHAR(256)
);

+------------------+----------+--------------+------------------+-------------------+
| File             | Position | Binlog_Do_DB | Binlog_Ignore_DB | Executed_Gtid_Set |
+------------------+----------+--------------+------------------+-------------------+
| mysql-bin.000001 |      551 | tyrell_corp  |                  |                   |
+------------------+----------+--------------+------------------+-------------------+

GRANT SELECT, INSERT, UPDATE, DELETE, REPLICATION SLAVE ON *.* TO 'replica_user'@'%'
GRANT CREATE USER, RELOAD, REPLICATION CLIENT, REPLICATION SLAVE, REPLICATION_SLAVE_ADMIN ON *.* TO 'replica_user'@'%'

mysql -uholberton_user -p -e "SHOW GRANTS FOR 'replica_user'@'%'"

ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQC0AsCjyKqHs0RwcYrPBsTXPc+wvm71Kj+mqDqXhNucuYIN0q6RJou6MuZw5J8/pbSBBwNj+U1yKAZ6xZr8u270zR9xqHudYR5SLwbCHhDwEsNLdO1s6XkJsJtHQUHJjIV68tmDHd4FE7Z+3sLic64TBaa8fraYPup+iaIbaYtVGbe7VbouxQK2p+h455qaGhrVE5Engf3NryWuOXt0e5b2j/e5a/l6j5sRR/iQ+iqb76qovpwnkUc4/v+ZRXQHKZIUNFTIwTgVnG3O34A/+cPJg5JULfhPrBdc7CWqrkhDSJVZALv6vCMtrEQaKG7sJfKuCA8+4u+KCJkjKZiCj0UTXROa9gxbNnpTWwLRCrs4cCIjlIKh395TBhSBxkpSorKGtSpQYSpJmsQXpldgVgSFHtzkoqXuJFSYWDYQmmgGA+3jwehBITMOU0+lVI2k+gSSbEle7z9HdqyqOfhayW4Fm3ujvwvqsWz3N4TxIjrmUB5DbtQowN31RBa4kmLbq2k= ubuntu@71430-web-01