Building and deploying a simple multi-tier web application using Kubernetes and Docker. The application is written in PHP as its frontend tier and it uses redis as its backend storage.

- Here we will make a single instance of Redis to store the Guestbook entries
- We will also create multiple web frontend instances

Objectives:
Start up a Redis leader.
Start up two Redis followers.
Start up the guestbook frontend.
Expose and view the Frontend Service.

![image](https://user-images.githubusercontent.com/47093323/201601656-2f7b8685-ef22-4aee-b4ec-3334037fe420.png)
- Above is the Redis leader and follower

- Below is the deployed multiple frontends of 3 replicas

![image](https://user-images.githubusercontent.com/47093323/201602165-0dcfc57b-d60d-4483-ada9-342fabd46668.png)


- We have added the needed service to each deployment file and below is all the services of type Cluster IP:

![image](https://user-images.githubusercontent.com/47093323/201602734-39dce2a8-a2e9-4006-8fcc-4e5ab619dba4.png)

After using kubectl port forward to forward traaffic from localhost on port 8080 to cluster port of 80, we have the terminal image and corresponding browser image below:

![image](https://user-images.githubusercontent.com/47093323/201603745-0a06783b-929e-4b09-9bd3-72bac1920c3a.png)

![image](https://user-images.githubusercontent.com/47093323/201604230-be4d5301-f05f-4142-8d20-0d8ea698c94e.png)
