# crd-to-adoc

## Description

Goal of this command project is to generate adoc file that document CRD definition.

> This project is base on the [`po-docgen`](https://github.com/coreos/prometheus-operator/tree/master/cmd/po-docgen) used in the [prometheus-operator](https://github.com/coreos/prometheus-operator)

## How to use it

```console
$ ./crd-to-adoc --help
Usage of ./crd-to-adoc:
  -n, --crd-name SetStrings   root crd stuct
  -f, --file stringArray      list of types.go files
      --footer string         .md file to be include as footer of the generate doc (default "footer.md")
      --header string         .md file to be include as header of the generate doc (default "header.md")
      --links string          list of external structs document links (default "links.csv")
```

example:

```console
$ ./crd-to-adoc -f ~/datadog-operator/api/v1alpha1/datadogagent_types.go -n DatadogAgent
```

result: https://gist.github.com/fao89/f543ea634d04d74455bc2afb8efca7a4



## How to build it

```console
$ GO111MODULE=on go build .

```
