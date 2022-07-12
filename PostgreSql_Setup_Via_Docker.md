### PostgreSql

#### How to setup PostgreSql via docker

* Download postgresql docker image
```
docker pull postgres
```

* Start container base on the new download image
```
docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres
```

> Need add **winpty** as prefix to above command if you running those command on Win 10 
