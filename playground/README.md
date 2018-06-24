# Simple MXNet Distributed Training using k8s Job and Services

* Dockerfile builds the mxnet image with examples
* mxnetjob.yaml is a simple k8s manifest to bring up a distributed mxnet job
* skaffold.yaml is the skaffold manifest to build and run the distributed mxnet job
  * `skaffold run` to run the job
    * This creates two pods - scheduler and worker.
    * scheduler runs the scheduler (coordinator)
    * worker runs two pods - worker and server
  * `skaffold delete` to delete the job
