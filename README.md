# dokku-couchdb-multi-containers

dokku-couchdb-multi-containers is a plugin for [dokku][dokku] that provides a CouchDB container per application. It is inspired by the [Redis plugin][redis_plugin] from [Michael Yoo][sekjun9878].

This version is compatible with dokku 0.3.17+ and 0.4+.

## Installation

```shell
# dokku 0.3.x
$ git clone https://github.com/Flink/dokku-couchdb-multi-containers /var/lib/dokku/plugins/couchdb-mc
$ dokku plugins-install

# dokku 0.4+
$ dokku plugin:install https://github.com/Flink/dokku-couchdb-multi-containers.git
```

## Commands
```
$ sudo dokku help
    couchdb:enable <app>     Enable CouchDB for an app for next build/deploy
    couchdb:destroy <app>    Destroy CouchDB container and volume of an app
```

## Info
This plugin adds the following environment variables to your app automatically (they are available via `dokku config`):

* COUCH\_URL
* COUCH\_HOST
* COUCH\_PASS
* COUCH\_PORT
* COUCH\_USER

## License

This plugin is released under the MIT license. See the file [LICENSE](LICENSE).

[dokku]: https://github.com/progrium/dokku
[redis_plugin]: https://github.com/sekjun9878/dokku-redis-plugin
[sekjun9878]: https://github.com/sekjun9878
