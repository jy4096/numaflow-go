.PHONY: build
build:
	CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -v -o ./dist/counter-example main.go

.PHONY: image
image: build
	docker build -t "quay.io/numaio/numaflow-go/reduce-stream-counter:v0.5.3" --target counter .

clean:
	-rm -rf ./dist
