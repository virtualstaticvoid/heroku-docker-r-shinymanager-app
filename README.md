# Shiny Manager Example

Example project for using [shinymanager][shinymgr] on Heroku with the container stack.

> `shinymanager` is a simple and secure authentication mechanism for single [Shiny][shiny] applications.
> Credentials are stored in an encrypted ‘SQLite’ database. Password are hashed using ‘scrypt’ R package.
> Source code of main application is protected until authentication is successful.

This project demonstrates a workaround for [heroku-buildpack-r][buildpack] [issue #142][issue_142]

## Usage

[![Deploy](https://www.herokucdn.com/deploy/button.svg)][deployapp]

### Build

Run the following command to build the docker image.

```
docker build --tag shiny_manager_example .
```

### Run

Run the following command to run the docker image.

```
docker run -p "8080:8080" shiny_manager_example
```

Open your web browser to http://localhost:8080.

## Deploy to Heroku

Run the following commands to create the Heroku application and deploy the code.

Create a container stack application.

```
heroku create --stack=container
```

Deploy the code.

```
git push heroku main
```

View the application in your web browser

```
heroku open
```

Login with one of the following credentials:

| Role  | User Name | Password |
|-------|-----------|----------|
| Admin | `admin`   |`p@ssw0rd`|
| User  | `user`    |`p@ssw0rd`|

## License

MIT License. Copyright (c) 2021 Chris Stefano. See [LICENSE](LICENSE) for details.

<!-- Links -->
[buildpack]: https://github.com/virtualstaticvoid/heroku-buildpack-r
[deployapp]: https://heroku.com/deploy?template=https://github.com/virtualstaticvoid/heroku-docker-r-shiny-manager-app/tree/main
[issue_142]: https://github.com/virtualstaticvoid/heroku-buildpack-r/issues/142
[shiny]: https://shiny.rstudio.com/
[shinymgr]: https://datastorm-open.github.io/shinymanager/
