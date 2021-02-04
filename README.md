# FFmpeg Docker image


# 설치

docker pull cordob/ffmpeg








mp4 to h265  변환 

sudo docker run --rm -it \
  -v $(pwd):/config \
cordob/ffmpeg \
  -i /config/10.mp4 \
  -c:v libx265 \
  -c:a copy \
  /config/output.mkv
