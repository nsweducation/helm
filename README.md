# Helm Chart Repository

The Department Helm Chart repository is unfortunately hosted in GitHub pages, because it's the simplest method for managing
static files. This is suitable for platform services charts, but for application charts you will likely need a real chart repository.

## Package

```shell script
helm package charts/CHART -d docs
helm repo index docs
```

## Publish

```shell script
git add docs
git commit -am "Updated CHART to version 1.0.3"
git push
```

## Check

It takes about 20 seconds for the chart files to update, but once they have updated you can verify the chart is available.

```shell script
helm search repo nsweducation
```