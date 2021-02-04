# FFmpeg Docker image


# Docker 설치

sudo snap install docker

# ffmpeg 설치

sudo docker pull jrottenberg/ffmpeg


# mp4 to h265  변환 

sudo docker run --rm -it \
  -v $(pwd):/config \
jrottenberg/ffmpeg \
  -i /config/10.mp4 \
  -c:v libx265 \
  -c:a copy \
  /config/output.mkv
