
compile:
	docker run --rm -i -v ${PWD}:/app cpp:base g++ hello_world.cpp -o hello_world.app

run:
	docker run --rm -i -v ${PWD}:/app cpp:base ./hello_world.app

clean:
	rm hello_world.app
