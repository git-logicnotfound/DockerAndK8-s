
To build the docker image

docker image build -t logicnotfound/learning_containers:<imageVersion> .

To Run the docker image by container,

docker run -d -p 5000:80 logicnotfound/<imageName>

To push the docker image into docker hub,

docker push logicnotfound/<imageName>:<imageVersion>