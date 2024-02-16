docker run -d \
  --name=kasm \
  --privileged \
  -e KASM_PORT=443 \
  -e DOCKER_HUB_USERNAME=USER `#optional` \
  -e DOCKER_HUB_PASSWORD=PASS `#optional` \
  -e DOCKER_MTU=1500 `#optional` \
  -p 3000:3000 \
  -p 443:443 \
  -v /path/to/data:/opt \
  -v /path/to/profiles:/profiles `#optional` \
  -v /dev/input:/dev/input `#optional` \
  -v /run/udev/data:/run/udev/data `#optional` \
  --restart unless-stopped \
  lscr.io/linuxserver/kasm:latest
