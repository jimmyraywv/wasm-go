
.PHONY: build-wasm clean-wasm build clean clean-all

build-wasm:	clean-wasm
	GOOS=js GOARCH=wasm go build -o main.wasm

clean-wasm:
	rm -f main.wasm

build:	clean
	go build -o main

clean:
	rm -f main

clean-all:	clean	clean-wasm

DEFAULT:	build-wasm


