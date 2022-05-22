
compile:
	docker run --rm -i -v ${PWD}:/app hello g++ hello_world.cpp -o hello_world.app

run:
	docker run --rm -i -v ${PWD}:/app hello ./hello_world.app

clean:
	rm hello_world.app
