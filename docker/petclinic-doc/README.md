# Petclinic Documents CI Image

## build

```bash
$ docker build --pull --build-arg http_proxy --build-arg https_proxy -t docker.pkg.github.com/t-kiyono/github-actions-test/petclinic-doc .
```

## push

```bash
$ docker push docker.pkg.github.com/t-kiyono/github-actions-test/petclinic-doc
```
