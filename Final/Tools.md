## Tools

### Packer.io
- Packer is an open source tool for creating identical machine images for multiple platforms from a single source configuration.
- Machine image is a single static unit that contains pre-configured OS and installed suite of s/w.
- It uses CMs like Ansible, Chef, etc. to provision these images.
- These images can be run anywhere like AWS, OpenStack, etc. as they are identical.
- The images generated by Packer can be used in Continuous Delivery pipeline, where an environment is setup in all the prob instances before application is deployed.
- Same image can be used by all team like Dev, QA, Testing, so each team will have same environment and can be confident about their results.

### Docker swarm
- It is an orchestration, clustering and scheduling tool.
- Docker swarm helps to easily manage and establish a cluster of Docker nodes as a single virtual system, through a single CLI. User need not access each docker container.
- It helps to discover new service, perform load balancing and scale the services, if the current swarm cannot handle the load.
- Similar to Kubernetes and Nomad. While others can host VMs and system apps, Docker Swarm only work with Docker.

### AWS Lambda
- It is a serverless computing platform that manages resources automatically.
- Function is event driven like upload to S3, API actions, CRON events.
- Pay only for the time consume using the service.
- Flow:
Upload code to AWS Lambda -> Setup trigger points like AWS services, HTTP endpoints, etc. -> Lambda gauges resource requirement and fulfills request -> Pay for the time used.
- Supports java, python, nodejs, c#, .net apps
- Issues are the applications should be event driven, difficult to test locally, no control over env, execution time limit per request (5 mins)
- Other applications like fission.io, google cloud functions, azure functions, openwhisk

### LaunchDarkly
- It is a continuous delivery platform that provides benefits of feature flag driven development.
- Flagging of any feature is easy from the Dashboard.
- The features can be rolled out to specific users, and their feedback can be collected.
- Disable a part of application, without taking whole application out.
- Easily usable by non-technical people but the initial cost can be daunting.

### Spinnaker.io
- Easy to use browser based tool (open source) that creates flexible cloud deployment pipelines.
- Manages cluster by accessing the cloud resources like servers, clusters, application, load balancers, security groups, etc.
- Creates a canary env, performs tests, and automatically releases to prod and deletes canary.
- Jenkins is an automation server that has plugins to perform CI and CD, whereas SPinnaker is built for CD which can be triggered using Jenkins.
- Terraform defines and manages infrastructure, however spinnaker specializes these task from the perspective of CD tasks.
- Spinnaker is a costly investment.
- Spinnaker works on the idea of immutable architecture, so a new commit means deploying new instance, so things can be slow.

### Kafka
- A distributed streaming platform that process real-time records. Usually ran as a cluster of nodes and streams of data stored as topics.
- Used by message driven service and applications that consume streams of data.
- Flow:
Send streams of data to kafka -> kafka buffers the data and sends it to subscribers of that topic -> use spark, storm, etc to process the data -> Send it to end users
- Alternatives like RabbitMQ and ActiveMQ for message brokers. Spark, Flink, Storm for stream processing.
- It has dependency on zookeeper.
