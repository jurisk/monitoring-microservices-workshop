Kamon Versions:

kamon-core: 1.0.0-RC1-1d0548cb8281202738d8d48cbe9cdd62cf209e21
kamon-scala: 1.0.0-RC1-933bb552dab8c322a30363f8a56a4e66274367ce
kamon-executors: 1.0.0-RC1-5d6a5ebffba5eea7933b2d40808136a878bb15b0
kamon-akka: 1.0.0-RC1-5472bca942c01bb87720263b36978cc0b243365e
kamon-play: 1.0.0-RC1-cf7506f2d05b7e868ab5291c73f45188b7db8069
kamon-prometheus: 1.0.0-RC1-2d76dd57df52b4bf0b31cc6f2bfb9f393dfa915e
kamon-datadog: 1.0.0-RC1-2dcf4510efe9df12e640504bfa30ecabb3422638
kamon-jaeger: 1.0.0-RC1-6cbd74406aac0bedc20746abc78f27e566de1f90



Docker Containers:


Docker Containers:

docker run -d --rm --net=host --name prometheus prom/prometheus

docker run -d --net=host --name=prometheus -v /home/ivantopo/projects/monitoring-microservices-workshop/container-data/prometheus.yml:/etc/prometheus/prometheus.yml prom/prometheus -config.file=/etc/prometheus/prometheus.yml -storage.local.path=/prometheus


docker run -d --rm --net=host --name grafana grafana/grafana
docker run -d --rm --net=host --name jaeger jaegertracing/all-in-one:latest

docker kill --signal=HUP prometheus