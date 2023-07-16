## pnr.sh

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

[pnr.sh](https://pnr.sh) is a tool for viewing hidden metadata on airline reservations, written in Go. It is fast and lightweight, stores no data, and displays useful data that would otherwise not be visible.

![pnr.sh demo image](.github/screenshot.png)

pnr.sh uses normal and public APIs to obtain reservation information that is already sent to mobile phones by the airline carrier during normal use of their mobile applications.

| Airline         | Supported | Notes                          |
| --------------- | --------- | ------------------------------ |
| Aeromexico      | ✅        | Provides most useful PNR data. |
| Delta Air Lines | ✅        | Provides most useful PNR data. |
| United          | ✅        | Provides most useful PNR data. |
| Virgin Atlantic | ✅        | Provides most useful PNR data. |
| Others          | ❌        | Not yet!                       |

pnr.sh is open-source and freely licensed under the MIT license.

## Building with Docker

A `Dockerfile` is included for easily building and deploying `pnr.sh`. By default, it will listen on `0.0.0.0:8080`. This can be overridden by changing the `PORT` environment variable.

build the docker image
`docker image build .`

get the image name
`docker image ls`

run the docker image
`docker run --name <whatever> -p 8080:8080 -d <theImage>`
`docker run --name pnrsh -p 8080:8080 -d 8732c4d9e33c`

you can see the running container
`docker container ls`

and it should be available on `http://0.0.0.0:8080`

or use the docker-compose.yml file i added and just run
`docker compose up`
