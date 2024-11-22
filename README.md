# APRSC Docker

A dockerized version of [hessu's aprsc](http://aprs-is.net/) APRS-IS server. [APRS-IS](http://aprs-is.net/) connects regional APRS packet radio networks together through the Internet. The original source for `aprsc` lives [here](https://github.com/hessu/aprsc).

![APRSC Screenshot](.images/aprsc-screenshot.png)

## Install
[Docker and Docker Compose need to be installed.](https://docs.docker.com/engine/install/debian/)
```bash
# clone the repo
git clone https://github.com/brannondorsey/aprsc-docker
cd aprsc-docker
```

```bash
# create an aprsc.conf file using the example. You MUST configure this to fit
# your needs. Configuration information is available here: 
#  http://he.fi/aprsc/CONFIGURATION.html
cp aprsc.conf.example aprsc.conf
```

```bash
# run the service in "detach" mode
docker compose up -d

# follow the logs
docker compose logs -f
```

You should now have an HTTP status server running at <http://localhost:14501>.

```bash
# shutdown
docker compose down
```

# Changes
* KE5KUL - Updated CMD for Dockerfile
* KE5KUL - Added working_dir to docker-compose.yaml
* KE5KUL - Added hostnames/network to docker-compose.yaml for integration with trackdirect container.
