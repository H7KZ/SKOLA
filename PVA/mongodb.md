# MongoDB Connection with C# .NET

## MongoDB Database setup

1. Sign into https://mongodb.com
2. Create new organization only for you (not for your company)
3. Create new project
4. Create a new cluster
5. Select shared for free tier
6. Select server provider (doesnt matter)
7. Select region (choose the closest one)
8. Set cluster name
9. Click create cluster
10. Wait for cluster to be created
11. Create new database user
12. Set username and password
13. Select read and write access
14. Click add user
15. Add new IP address record 0.0.0.0/0 for all IP addresses
16. Create new database inside cluster
17. Set database name
18. Click create database with collection name (doesnt matter)

## MongoDB Database connection

1. Copy your database user name and password
2. Replace your user name and password in connection string
3. Copy your database connection string

```csharp
using MongoDB.Driver;

MongoClientSettings settings = MongoClientSettings.FromConnectionString("{YOUR DATABASE CONNECTION STRING}");
MongoClient client = new(settings);
IMongoDatabase database = client.GetDatabase("test");
```