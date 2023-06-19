## MongoDB [![Build Status Image](https://github.com/mu-box/microbox-docker-mongodb/actions/workflows/ci.yaml/badge.svg)](https://github.com/mu-box/microbox-docker-mongodb/actions)

This is an MongoDB Docker image used to launch a MongoDB service on Microbox. To use this image, add a data component to your `boxfile.yml` with the `mubox/mongodb` image specified:

```yaml
data.db:
  image: mubox/mongodb:3.0
```

## MongoDB Configuration Options
MongoDB components are configured in your `boxfile.yml`. All available configuration options are outlined below.

###### Quick Links
[version](#version)
[objcheck](#objcheck)
[log\_verbosity](#log-verbosity)
[directoryperdb](#directoryperdb)
[logappend](#logappend)
[nojournal](#nojournal)
[noscripting](#noscripting)

#### Overview of MongoDB Boxfile Settings
```yaml
data.db:
  image: mubox/mongodb:3.0
  config:
    objcheck: true
    log_verbosity: 'v'
    directoryperdb: true
    logappend: true
    nojournal: false
    noscripting: false
```

### Version
When configuring a MongoDB service in your Boxfile, you can specify the version to use. The following version(s) are available:

- 2.6
- 3.0
- 3.2
- 3.4

**Note:** Due to version compatibility constraints, MongoDB versions cannot be changed after the service is created. To use a different version, you'll have to create a new MongoDB service and manually migrate data.

#### version
```yaml
# default setting
data.db:
  image: mubox/mongodb:3.4
```

### ObjCheck
View the [MongoDB documentation](http://docs.mongodb.org/manual/reference/configuration-options/#diaglog) for details and configuration options.

#### objcheck
```yaml
#default setting
data.db:
  image: mubox/mongodb
  config:
    objcheck: true
```

### Log Verbosity
View the [MongoDB documentation](http://docs.mongodb.org/manual/reference/configuration-options/#verbose) for details and configuration options.

#### log\_verbosity
```yaml
data.db:
  image: mubox/mongodb
  config:
    log_verbosity: 'v'
```

### DirectoryPerDB
View the [MongoDB documentation](http://docs.mongodb.org/manual/reference/configuration-options/#directoryperdb) for details and configuration options.

#### directoryperdb
```yaml
#default setting
data.db:
  image: mubox/mongodb
  config:
    directoryperdb: true
```

### LogAppend
View the [MongoDB documentation](http://docs.mongodb.org/manual/reference/configuration-options/#logappend) for details and configuration options.

#### logappend
```yaml
#default setting
data.db:
  image: mubox/mongodb
  config:
    logappend: true
```

### NoJournal
View the [MongoDB documentation](http://docs.mongodb.org/manual/reference/configuration-options/#nojournal) for details and configuration options.

#### nojournal
```yaml
#default setting
data.db:
  image: mubox/mongodb
  config:
    nojournal: false
```

### NoScripting
View the [MongoDB documentation](http://docs.mongodb.org/manual/reference/configuration-options/#noscripting) for details and configuration options.

#### noscripting
```yaml
#default setting
data.db:
  image: mubox/mongodb
  config:
    noscripting: false
```

## Help & Support
This is a MongoDB Docker image provided by [Microbox](http://microbox.cloud). If you need help with this image, you can reach out to us in the [Microbox Discord](https://discord.gg/MCDdHfy). If you are running into an issue with the image, feel free to [create a new issue on this project](https://github.com/mu-box/microbox-docker-mongodb/issues/new).

## License

This project is released under [The MIT License](http://opensource.org/licenses/MIT).
