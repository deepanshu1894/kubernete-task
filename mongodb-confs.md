
### After creating the Stateful 

- set inititalze mongosb cluster

  ```rs.initiate(
          {
            _id: "rs0",
            version: 1,
            members: [
                { _id: 0, host : "mongodb-0.mongo.default.svc.cluster.local:27017" },
            ]
          }
        )
  ```

- Check status of cluster
  ```
      rs.stats()
  ```

- creat a user

  ```db.createUser({
        user: "admin",
        pwd: "test",
        roles: [{ role: "root", db: "admin" }]
    });
  ```

- Auth User
  ``` 
  db.auth('admin','test')
  ```
cfg.members = [
{ _id: 0, host: "mongodb-0.mongo.default.svc.cluster.local:27017" },
]


- database_url for express
  ```
      mongodb-0.mongo.default.svc.cluster.local
  ```

- Get users
  ```
    db.getUsers()
  ```
