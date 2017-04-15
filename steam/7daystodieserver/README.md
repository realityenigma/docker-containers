
Make sure to create a sevendays directory within your PWD or specify a different mount location for the "sevendays" volume.

```
docker run -d --name sevendays -P -v `pwd`/sevendays:/opt/7daystodie realityenigma/7daystodiesever
```
