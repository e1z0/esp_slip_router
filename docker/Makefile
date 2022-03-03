all: libs

libs:
	docker build -t esp-open-sdk:latest -f Dockerfile_libs --no-cache=true .
upload:
	docker tag esp-open-sdk:latest nulldevil/esp-open-sdk:latest
	docker push nulldevil/esp-open-sdk:latest
clean:
	docker image prune -a -f
	docker volume prune -f
	docker network prune -f
	docker system prune --volumes -f
