# Project-4-Continous-Integration-Pipeline-For-Tooling-Website

# TOOLING WEBSITE DEPLOYMENT AUTOMATION WITH CONTINUOUS INTEGRATION. 
## INTRODUCTION TO JENKINS

#### Project Descirbtion
**Adding a Jenkins server, configure a job to automatically deploy source codes changes from Git to NFS server.**

![Capture](https://user-images.githubusercontent.com/74002629/184101792-3c29fba2-78dd-4333-8aee-3385c605ecf1.PNG)

#### Step 1- Jenkins server
1. Create an AWS EC2 server based on Ubuntu Server.
2.Jenkins is up and running.

![install jenkins](https://github.com/Hatem-sudo/Project-4-Continous-Integration-Pipeline-For-Tooling-Website/assets/113099054/c0700a46-43c2-4029-9281-1e8b360edd45)

3.Configure Jenkins to retrieve source codes from GitHub using Webhooks

![webhook](https://github.com/Hatem-sudo/Project-4-Continous-Integration-Pipeline-For-Tooling-Website/assets/113099054/070bad05-bfad-4876-936f-1bbe3ab58ea1)

4. Enable webhooks in your GitHub repository settings: 
5. Connect GitHub repository.
5. Save the configuration and try it manually.
7. Open the build and successfully.
   
![Configure Jenkins](https://github.com/Hatem-sudo/Project-4-Continous-Integration-Pipeline-For-Tooling-Website/assets/113099054/75e469b4-1641-4441-a142-362e830b77b1)


9.Make some change in any file in your GitHub repository (e.g. README.MD file) and push the changes to the master branch.
10.A new build has been launched automatically (by webhook) and you can see its results – artifacts, saved on Jenkins server.
11. We have successfully configured an automated Jenkins job that receives files from GitHub by webhook trigger.
![Configure jenkins on web site](https://github.com/Hatem-sudo/Project-4-Continous-Integration-Pipeline-For-Tooling-Website/assets/113099054/fbbf1dff-cc10-429f-9331-258590d5a3a0)

12. By default, the artifacts are stored on Jenkins server.

#### Step 3 – Configure Jenkins to copy files to NFS server via SSH
1. Now our artifacts saved locally on Jenkins server
2. Navigate to the dashboard.
3. Configure the job/project to copy artifacts over to NFS server.
4.Make sure the connection returns **Success** Remember, that TCP port 22 on NFS server must be open to receive SSH connections.
5. Webhook will trigger a new job and in the "Console Output" of the job.
   
![Builds](https://github.com/Hatem-sudo/Project-4-Continous-Integration-Pipeline-For-Tooling-Website/assets/113099054/fe998f43-7835-4f77-a1e3-20fe6e75de21)

6. If you see the changes you had previously made in your GitHub – the job works as expected.





