# akilli/gogs

`akilli/base` based Gogs image including MySQL, PostgreSQL, SQLite and TiDB support.

## Usage

In your `docker-compose.yml` include something like

    version: '3'
    volumes:
        gogs: {}
    services:
        gogs:
            image: akilli/gogs
            ports:
                - "3000:3000"
            volumes:
                - gogs:/data

Then browse to `http://localhost:3000`

**NOTE**
Runs as `app` user that is created in the `akilli/base` image.
