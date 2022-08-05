# تثبيت وإعداد "مونجو دي بي" وإتاحتها للإتصال عن بعد
# Install And Configure Mongodb For Remote Access


sudo ufw allow from 2.58.82.240 to any port 27017

db.createUser(

    {

       user: "MongoRoot",

       pwd: "SrongPWD!@#1",

       roles: [ { role: "userAdminAnyDatabase", db: "admin" } ]

    }
    
)

/etc/mongod.conf

mongo "mongodb://2.58.82.240:27017"

mongo -u MongoRoot -p

mongo -u MongoRoot -p --host 2.58.82.240:27017
