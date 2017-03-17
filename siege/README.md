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
#### To run siege for a specific site:
```
# Run for 10s simulating 100 concurrent users
docker run --rm lopezs/siege -10s -c100 http://www.bbc.co.uk
```

#### Randomly hit urls from a list
```
# Run for 10s simulating 100 concurrent users, using example list specified in the Dockerfile
docker run --rm lopezs/siege -t10s -c100 -i -f urls.txt
```
