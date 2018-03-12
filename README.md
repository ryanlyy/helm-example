# 1. Description
A Chart Repository for Kubernetes Deployment

NOTE: nginx is used to implement chart repository

# 2. Installation
* User can customalized values.yaml
* helm install --name mychartrepos chart-repos --values yourvalues.yaml

# 3. Add local chart repos
```
helm repo add [name] [URL]
example: helm repo add nokia http://10.96.6.1
10.96.6.1 is ip what your above repos created
```
# 4. Application Deployment
* Package appliation Chart
```
helm package [APPL_CHART_PATH]
```
* Package Index into Chart Repository
```
helm repo index --url=http://10.96.6.1 [tgz DIR]
helm repos update
```
