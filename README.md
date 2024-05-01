# Dog age equivalence
Simple frontend application to calculate a dog's age human equivalent.

## Dev Instructions

After clonning this repository you need to install the dependencies using `npm install` command.

Once it finishes, you can run in developer mode using `npm run dev` command

## Deploy

A Dockerfile is provided for production deployment. You will only need to run the following commands from project root folder

```bash
cd dog-age-converter && \
docker image build -t "dog-human-age:latest" -f Dockerfile ./ && \
docker container run -p "8088:80" dog-human-age:latest
```

If everything goes well you will have the application running and accessible from a browser from `8088` port.

## Requirements
- Docker CE (>= 26.0.0)
- NodeJS (>= 20.0)
- NPM (>= 10.0)
