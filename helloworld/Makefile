
.PHONY: build-wasm clean-wasm build clean clean-all serve

.SILENT:

build-wasm:	clean-wasm
	GOOS=js GOARCH=wasm go build -o main.wasm

clean-wasm:
	rm -f main.wasm

serve:
	goexec "http.ListenAndServe(\`:8080\`, http.FileServer(http.Dir(\`.\`)))"

build:	clean
	go build -o main

clean:
	rm -f main

clean-all:	clean	clean-wasm

DEFAULT:	build-wasm


