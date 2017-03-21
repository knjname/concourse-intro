See https://concourse.ci/docker-repository.html.

## Start with docker-compose

Generate keys and launch up docker-compose.

```console
$ ./init.sh
$ docker-compose up -d
```

## Download CLI (macOS)

```console
$ curl -L "http://localhost:8080/api/v1/cli?arch=amd64&platform=darwin" > fly
$ chmod +x fly
```

## Login to concourse (via CLI)

```console
$ ./fly -t lite login -c http://localhost:8080
$ # Account: concourse / changeme
```

## Upload hello.yml as a pipeline defintion

```console
$  ./fly -t lite set-pipeline -p hello-world -c hello.yml
```

Login to http://localhost:8080. Then you'll see `hello-world` pipeline in the site.

