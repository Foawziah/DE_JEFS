
Follow these steps:
- run on your terminal: `git clone https://github.com/apache/superset.git`
- edit docker-compose-non-dev.yml in `superset` folder by changing the image name to: `x-superset-image: &superset-image apache/superset:2.1.0`
- run on your terminal: `cd superset`
- run on your terminal:  `docker-compose -f docker-compose-non-dev.yml pull`
- run on your terminal: `docker-compose -f docker-compose-non-dev.yml up -d`
- wait a few minutes till containers are up and running then run on your terminal (it sets up the login credentials for admin): `docker exec -it superset_app bash ./docker/docker-init.sh`
- go to http://localhost:8088 and log in by `user: admin` and `pass: admin`.

Run on your terminal: `docker-compose down` for terminating the application.
