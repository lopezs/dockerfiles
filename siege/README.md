# container-siege
siege stress testing tool based on ubuntu

### Building
```
docker build -t lopezs/siege .
```

### Usage
To show valid parameters/help:
```
docker run --rm lopezs/siege
```
To run siege for a specific site:
```
docker run --rm lopezs/siege [attibutes] [site]
```
