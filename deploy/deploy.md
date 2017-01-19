1) Retrieve the docker login command that you can use to authenticate your Docker client to your registry:
aws ecr get-login --region eu-west-1

2) Run the docker login command that was returned in the previous step.
3) Build your Docker image using the following command. For information on building a Docker file from scratch see the instructions here. You can skip this step if your image is already built:
docker build -t demo .

4) After the build completes, tag your image so you can push the image to this repository:
docker tag demo:latest 831650818513.dkr.ecr.eu-west-1.amazonaws.com/demo:latest

5) Run the following command to push this image to your newly created AWS repository:
docker push 831650818513.dkr.ecr.eu-west-1.amazonaws.com/demo:latest


6) docker build -f Dockerfile .

7) docker push

8) aws ecs register-task-definition --cli-input-json file://./sample_task.json
9) aws ecs run-task --cluster BloxLocalCluster-ECSCluster-1QCSFTJ192MWC --task-definition BloxDemoFamily
