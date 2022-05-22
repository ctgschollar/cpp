
build:
	docker run --rm -v ${PWD}:/app cpp:base cmake -S . -B build
	docker run --rm -v ${PWD}:/app cpp:base cmake --build build

test:
	docker run --rm -v ${PWD}:/app cpp:base bash -c "cd build && ctest"

clean:
	rm -rf build
