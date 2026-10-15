export GH_USERNAME='popsalife'
export GH_TOKEN=''
export GH_NAME='hello-world'
export GH_VER='1.0.0'
export TAG_NAME='ghcr.io/popsalife/hello-world:1.0.0'

echo $GH_TOKEN | docker login ghcr.io -u $GH_USERNAME --password-stdin

docker tag hello-world:latest ghcr.io/popsalife/hello-world:1.0.0

docker push $TAG_NAME

LABEL org.opencontainers.image.source https://github.com/OWNER/REPO