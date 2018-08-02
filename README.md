# docker proftpd alpine

A proftpd docker container based on alpine.

## Usage

### without compilation

Create a docker-compose.yml in root project folder. Fill free to change mysql credentials.

```
proftpd:
  image: blueapple/docker-alpine-proftpd
  volumes:
    - ./proftpd.conf:/usr/local/etc/proftpd.conf
    - ./data/ftp:/data
  links:
    - mysql
  ports:
    - "20:20"
    - "21:21"
    - "60000-60100:60000-60100"
```

Get a proftpd configuration file (like this one : https://github.com/blueapple168/docker-alpine-proftpd/blob/master/proftpd.conf) and run the containers.
