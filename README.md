[Mailcatcher][1] application for [Otto][2].

## Usage

Add as a dependency in your Appfile:

```
application {
    name = "example-app"

    dependency {
        source = "github.com/withassociates/otto-mailcatcher"
    }
}
```

Configure ActionMailer to use mailcatcher’s SMTP server:

```rb
# config/environments/development.rb

config.action_mailer.smtp_settings = {
  port: 1025,
  address: "mailcatcher.service.consul",
}
```

Access Mailcatcher’s UI on the host machine:

```sh
$ open "http://$(otto dev address):1080/"
```


[1]: http://mailcatcher.me/
[2]: https://ottoproject.io/
