`Github` repo is a mirror of `Gitlab` repo

# Json schema to Typed classes

This is a container packaging [quicktype](https://github.com/quicktype/quicktype) to generate Type classes from [Json Schema](http://json-schema.org/). Purpose of this pacakge is to provide convenience of avoiding installing all tools and requirements to use quicktype to generate type classes from json schema

# To build on local

> `docker build  --build-arg BUILD_DATE=$(date -u +'%Y-%m-%dT%H:%M:%SZ') -t jsonschema2quicktype:latest .`

> `docker run -i -e QUICKTYPE='-l ruby' jsonschema2quicktype:latest  < input-schema.json > output-class.rb`

`QUICKTYPE` variable takes all quicktype options. Don't pass the `-s`, `--src` or `--src-lang` as that is defined to use `-s schema`


# To run via docker on your files locally

> `docker run --rm -i -e QUICKTYPE='-l ruby' darahsan/jsonschema2quicktype  < input-schema.json > output-class.rb`



#  To go inside the container for fun or else 


> `docker-compose up` 

> `docker exec -it jsonschema2quicktype sh`