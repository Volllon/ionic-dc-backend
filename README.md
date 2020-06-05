# ionic-backend
## Requirements for use

+ installed node
  + https://nodejs.org/en/download/
+ installed mongoDB
    + https://docs.mongodb.com/manual/installation/
### Super Easy Install
You need to add keys.js in /config. Templates in mock.keys.js 


Pay attention to the fields {emailFrom: ' ', gmailPassword: ' '}. Set them real to use Mail.service. 

You can also use without them the application will not break
```
yarn 
yarn start
```
or 
```
yarn 
yarn start-dev
```

Congratulations, the server is running locally! 🎉🎉🎉

If you need ad default admin user? 
You can use the robo 3t or compas app.
And change the role from 0 ---> 1 to the inside of the user.
Also, if you do not have such an opportunity, I added a script for you that will help create the first admin
```
yarn default-admin
```

console output:
```$xslt
$ node ./config/database/createDefaultAdmin.js
MongoDB connected.
done
```
you will get a default user with admin rights

{ email: 'root@mail.com', password: 'root' } 


Also you can use docker, I added the ability to work with our application without installing a database, they can run the command
```docker-compose up --build```

the application will be available on the same local port as in development mode

### Features

For unlogged user:
- registration;
- authorization;
- password recovery;

For user:
- cleaner/my order list;
- add order;
- balance.

For admin:
- user/cleaner/all order/my order list;
- create/edit cleaner;
- change status order;
- balance.
