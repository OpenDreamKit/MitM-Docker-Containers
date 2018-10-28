# mitm-docker-images

Docker Images for the MitM use case:

- MMT
- GAP
- Sage
- Singular

To run everything, use [Docker-Compose](https://docs.docker.com/compose/overview/):

```bash
    # to build all the images
    docker-compose build

    # to run them (use -d if you want it in the background)
    docker-compose up
```

This will expose the following services:

- GAP on port 26133
- MMT on port 26134
- Singular on port 26135
- Sage on port 26136