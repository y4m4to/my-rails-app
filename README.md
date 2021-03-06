# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## Usage
### How to start the app
Execute the command in the directory where the file is located.
If you want logging to a terminal, you remove "-d" option.

```
$ docker-compose up -d
```

If you can't start the app, a pid file may be left.
```
web_1  | A server is already running. Check /app/tmp/pids/server.pid.
web_1  | Exiting
```

In that case, you nedd to delete a pid file.

```
$ rm tmp/pids/server.pid
```

### How to check the app status
```
docker-compose ps
```

### How to stop the app
Execute the command in the directory where the file is located.

```
$ docker-compose stop
```

### How to delete the container
Execute the command in the directory where the file is located.

```
$ docker-compose down
```

### How to stop the attach
```
Ctrl + p + q
```

### If you add a gem...
If youa add a gem, you run the following command to create a docker image with gem added.
```
docker-build
```

### How to test
```
docker-compose exec web bundle exec rspec ./past/to/test/target/
```

### How to create a migration
```
docker-compose exec web bundle exec rails g migration ClassName fieldName:Type
```

Example
```
docker-compose exec web bundle exec rails g migration AddBirthdayToUser birthday:date
```

### How to execute migration
```
docker-compose exec web bundle exec rails db:migarate
```
