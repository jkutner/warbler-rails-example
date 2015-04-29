## Heroku Warbler Example

This project demonstrates how to deploy a War file packaged with
[Warbler](https://github.com/jruby/warbler) and [JRuby](http://jruby.org)
to [Heroku](http://heroku.com).

There are three methods of doing this:

### Heroku Button

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

### Ruby Buildpack Deployment

```sh-session
$ git clone https://github.com/jkutner/warbler-rails-example
$ cd warbler-rails-example
$ heroku create
$ git push heroku master
```

### Standalone Toolbelt Deployment

```sh-session
$ git clone https://github.com/jkutner/warbler-rails-example
$ cd warbler-rails-example
$ heroku create
$ heroku plugins:install https://github.com/heroku/heroku-deploy
$ bundle install
$ warble
$ heroku deploy:jar --jar heroku-warbler-example.war
```

### Maven Deployment

Another method of deployment, not demonstrated here, uses a `pom.xml` to configure the app. For an example of this, see the [jruby-async-servlets-example](https://github.com/jkutner/jruby-async-servlets-example).

### Other Examples

+ 1.7.x - [kissaten/warbler-example](https://github.com/kissaten/warbler-example)
