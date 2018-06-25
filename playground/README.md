# MXNet Distributed Training using k8s Job and Services

* Dockerfile builds the mxnet image with examples
* mxnetjob.yaml is a simple k8s manifest to bring up a distributed mxnet job
    * Creates three jobs - scheduler(aka Master/Chief/Coordinator), server(PS) and worker.
    * Creates a service mx-scheduler for the mx-scheduler pod
* skaffold.yaml is the skaffold manifest to build and run the distributed mxnet job
  * `skaffold run` to run the job
  * `skaffold delete` to delete the job
