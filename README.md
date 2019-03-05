## nogsantos/mongodb

Docker MongoDB container

<table>
    <tbody>
        <tr>
            <th></th>
            <th></th>
        </tr>
        <tr>
            <td>MongoDB</td>
            <td>4.1</td>
        </tr>
    </tbody>
</table>

### Usage

#### mongod

```bash
$ docker run -d -p 27017:27017 --name mongodb nogsantos/mongodb
```

#### Run `mongod` w/ persistent/shared directory

```bash
$ docker run -d -p 27017:27017 -v <db-dir>:/data/db --name mongodb nogsantos/mongodb
```

#### Run `mongod` w/ HTTP support

```bash
$ docker run -d -p 27017:27017 -p 28017:28017 --name mongodb nogsantos/mongodb mongod --rest --httpinterface
```

#### Run `mongod` w/ Smaller default file size

```bash
$ docker run -d -p 27017:27017 --name mongodb nogsantos/mongodb mongod --smallfiles
```

#### Run `mongo`

```bash
$ docker run -it --rm --link mongodb:mongodb nogsantos/mongodb bash -c 'mongo --host mongodb'
```

### Sugest: GUI for MongoDB

[Robot 3T](https://robomongo.org/)

To access, just add a local connection.
