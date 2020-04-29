# Docker containers in separate compose files can talk to each other on the same network
* https://stackoverflow.com/a/48024244

Create a network for container(s) in first compose file
```
version: '3.7'
services:
...

networks:
  my-sweet-network:
```
Create a network for container(s) in second compose file and mark it external
```
version: '3.7'
services:
...
networks:
  custom-network:
    external:
      name: <compose_root>_my-sweet-network
```

Service join network in first compose file:
```
version: '3.7'
services:

  postgres:
    image: postgres:9.5-alpine
    networks:
      - my-sweet-network
    volumes:
    ...
```

Service join network in first second copose file:
```
version: '3.7'
services:

  some-service:
    image: http://path-to-image.com/library/image:latest
    networks:
      - custom-network
    volumes:
...
```
