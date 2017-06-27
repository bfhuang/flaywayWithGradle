# how to run flyway locally
1. clone this project locally and then cd to the project directory
2. run command: gradle idea(this will generate the idea project file *.ipr)
3. open *.ipr in Intellij
4. change the mysql configuration in build.grale to your mysql configuration
```
flyway {
    url = 'jdbc:mysql://localhost:3306/flyway'
    user = 'root'
    password = ''
}
```
5. run command: gradle flywayMigrate -i(after the task finished, you can check yout database the person table the data in this table exit)
6. if you want to add more table, just add more sql file under src/main/resources/db/migraiton directory and the name should be in the same format as exiting sql files

