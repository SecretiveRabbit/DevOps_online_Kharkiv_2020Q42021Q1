Jenkins Task  
Create some templates using lection materials about Jenkins according your final task. More detailed: choose the content part for your final task (simple web page, web application, etc) and programming language (java, js, python, etc), and type of delivery/deployment mechanism.  

We need to install java 8 first before installing jenkins. We can do it in sych a way:

| <img src = "screenshots/1.png"> |
|:--:|
| Picture 1 - Checking java on our server. |

Of course we cheked the service java service after installation to make sure it works.  
After that we enter the browser on our host machine to the address 192.168.1.11:8080. Here 192.168.1.11 is the address of our virtual machine and 8080 is the port of jenkins application. We'll need to sign up to jenkins by typing some information about us, including e-mail but it won't be used in practice.
Also we'll need to install jenkins on uur VM. The installator will offer to install the most popular plugiins or to do it in our own, but we'll choose the first way. Extra plugins won't take lots of place and we'll probobly need them and future and we'll save our time on installation.
After that we can create our first job. 

This is Jenkins GUI:
| <img src = "screenshots/14.png"> |
|:--:|
| Picture 2 - Jenkins GUI. |

This is how the process of creating job happens:

| <img src = "screenshots/15.png"> |
|:--:|
| Picture 3 - The procedure of creating jobs. |

| <img src = "screenshots/16.png"> |
|:--:|
| Picture 4 - The procedure of creating jobs. |

After the creationg our first job we can launch it. Launched jobs are performed in builds. Builds are such files that indicate the status of performing job. With the help of these files we can check if the job worked correctly. We can check it in Console Output.

If the buiid was configured, the last line in the console would be "Finished: SUCCESS". Otherwise you'll see the kinds of mistakes in the console.

| <img src = "screenshots/3.png"> |
|:--:|
| Picture 5 - Successful build. |

| <img src = "screenshots/4.png"> |
|:--:|
| Picture 6 - Unsuccessful build. |

We can also watch the status of the job in the main screen at the left bottom of the screen:

| <img src = "screenshots/5.png"> |
|:--:|
| Picture 7 - History of builds. |

This is the structure of the file. It'll need us in further settings. 

| <img src = "screenshots/6.png"> |
|:--:|
| Picture 8 - Structure of Jenkins directory. |

The matter is that jobs can be performed accrdoing to timetable. The frequency and size of builds influence speed of filling space of our storage. To avoid overfilling we'll set the maximum number of build record in the configurations of the job:

| <img src = "screenshots/7.png"> |
|:--:|
| Picture 9 - Checking logfile. |

After some builds we check the number of stored builds in the folder /jenkins/job/builds/ 

| <img src = "screenshots/8.png"> |
|:--:|
| Picture 10 - Setting maximum number of stored buils to five. |

As we see, the number of builds resticted to six. It's strange because we set the max number 5. Moreover, the first build of the job always exists. It seems that the first job is an exception from the rule.

Now we'll create job with deploying the code from GitHub to our another server.
The first thing we need to do is to create the second server and configurate it, namely, install java and jenkins, share ssh key with the server:

The second thing is to create a repository on git, add credentials and set SCM options in job configuration.

| <img src = "screenshots/10.png"> |
|:--:|
| Picture 11 - Configuring VM where we'll deploy our job. |

| <img src = "screenshots/18.png"> |
|:--:|
| Picture 12 - Creating SSH key to the server on GitHub. |

| <img src = "screenshots/9.png"> |
|:--:|
| Picture 13 - Checking if the job worked correctly. |

As the result, web-page will contain in the following data:

| <img src = "screenshots/17.png"> |
|:--:|
| Picture 14 - Checking site. |

Now we set the job such that it will use our nodes. We added some labels to the nodes and adjusted the job such that it'll use node2. The result we can see on the screenshot below:

| <img src = "screenshots/11.png"> |
|:--:|
| Picture 15 - Ckecking if the job can be performed by node. |

Jenkins can be controlled not only by GUI, but also by CLI. There are special coomands for Linux and Windows systems that let us perform various tasks. Here we checked the user on the Jenkins-server using bash and powershell. Also we set global variables to simplify the procedure of logging to the jenkins:

| <img src = "screenshots/12.png"> |
|:--:|
| Picture 16 - Using Jenkins CLI in bash. |

| <img src = "screenshots/13.png"> |
|:--:|
| Picture 17 - Using Jenkins CLI in PowerShell. |

Let's try out some commands. For instance, let's enable and disable plugin, build any job.

| <img src = "screenshots/20.png"> |
|:--:|
| Picture 18 - Using Jenkins CLI in PowerShell. |

| <img src = "screenshots/21.png"> |
|:--:|
| Picture 19 - Using Jenkins CLI in PowerShell. |

We'd like to notice that it's always good to restart Jenkins after enabling or disabling plugins. It'll help us avoid errors.

The whole list of commands in Jenkins CLI we can see in documentations and the page on the Jenkins GUI:

| <img src = "screenshots/19.png"> |
|:--:|
| Picture 20 - List of Jenkins commands. |
