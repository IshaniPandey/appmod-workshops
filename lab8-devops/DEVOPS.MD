# Develop a Kubernetes app with Helm using Continuous Delivery & Continuous Integration

Learn how to create an application in IBM Cloud™ by using a basic starter kit and a Kubernetes toolchain, and continuously deliver the app to a secure container in IBM® Cloud Kubernetes Service. Your continuous integration DevOps pipeline can be configured so that your code changes are automatically built and propagated to the app that’s in the Kubernetes cluster. If you already have a pipeline, you can connect it to your app.

## Steps:

1. Create a [CONTINUOUS DELIVERY](https://cloud.ibm.com/catalog/services/continuous-delivery) service in IBM Cloud.
`Create the service in the same region where cluster is deployed`

2. Create a Namespace in [Container Registry](https://cloud.ibm.com/kubernetes/catalog/registry) service(if you haven't done it yet)

3. Click on **ACCESS** in the Kubernetes cluster page and click on **Enable Toolchain** 

![DevOps](https://github.com/IBMDevConnect/ibmdevday2019-cloud/blob/master/cicdworkshop/images/main.png)

4. Click on **Create** in the **Develop a Kubernetes app with Helm** option

![DevOps](https://github.com/IBMDevConnect/ibmdevday2019-cloud/blob/master/cicdworkshop/images/1.png)

5. In the redirected page, scroll down and, click CREATE next to **IBM Cloud API Key** Wait for the values to get auto populated and click on **CREATE** the toolchain. `SELECT same region of the deployed cluster region while creating the toolchain`

![DevOps](https://github.com/IBMDevConnect/ibmdevday2019-cloud/blob/master/cicdworkshop/images/7.png)

6. Click Delivery Pipeline and you can see the BUILD, VALIDATE and PROD stage(as shown below).

The Build stage pulls the source code from your repository. It then runs jobs to compile or otherwise process the code to produce artifacts suitable for deployment. Each job runs in its own container. The artifacts are passed to follow-on stages through the build archive directory in the container. By default, this directory is the same as the directory where the source code was checked out. The Simple build job type passes the source code from your repo on as the result without modifying it.

The Deploy stage contains jobs that deploy the artifacts created by the Build stage.

![DevOps](https://github.com/IBMDevConnect/ibmdevday2019-cloud/blob/master/cicdworkshop/images/6.png)

![DevOps](https://github.com/IBMDevConnect/ibmdevday2019-cloud/blob/master/cicdworkshop/images/new-main.png)

7. Click on **Deploy Helm Chart** within PROD stage to see the logs.

![DevOps](https://github.com/IBMDevConnect/ibmdevday2019-cloud/blob/master/cicdworkshop/images/2.png)

8. Scroll down and VIEW the application by clicking in the URL mentioned near **VIEW THE APPLICATION AT**

![DevOps](https://github.com/IBMDevConnect/ibmdevday2019-cloud/blob/master/cicdworkshop/images/5.png)

## Task 2: Update the application and redeploy it

1. Click on Eclipse Web Orion IDE in the Toolchain

2. Open the app.js file and edit res.send response to any message.

`For eg: res.send('Welcome to IBM Cloud DevOps with Docker, Kubernetes and Helm Charts.I have learnt how to use the Continuous Delivery Service');`

3. In the left side, click on Git icon(second icon) and commit the changes by entering commit message in the right side.

4. Push the changes in the Outgoing branch.

5. Goto Delivery Pipeline to see the changes getting updated automatically and refresh the URL to see the updates you have made.

Congratulations you have completed the lab! 

You have created a toolchain that deploys a "Hello World" app to a secure container in a Kubernetes cluster. You changed a message in the app and tested your change, and when you pushed the change to the repo, the delivery pipeline automatically redeployed the app!
