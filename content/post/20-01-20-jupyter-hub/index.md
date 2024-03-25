---
title: "Deploying JupyterHub on the Cloud"
authors:
- kostas
date: 2020-01-20
---

I'm teaching a class on computational methods for environmental engineers this semester, and the language of choice is Python <!--more-->
as it is simple enough for potentially novice programmers and has a very rich ecosystem of existing libraries that make life easier for any environmental engineer/scientist. As I have taught the class once before, I emphasized reproducibility which meant that
we used Jupyter notebooks for most of the class. The other aspect of the class that I found tremendously useful was live coding. Thankfully, the [RISE extension](https://github.com/damianavila/RISE) combines Jupyter notebooks with slideshows (powered by [Reveal.js](https://revealjs.com/#/) presentation framework) and I ended up using it exclusively for preparing the lectures.

Although a good chunk of the class was spent with the students coding on their own with me going around answering questions, I decided to take it a step further by utilizing a [flipped classroom](https://en.wikipedia.org/wiki/Flipped%5Fclassroom) approach and combining it with paired/grouped learning. Essentially the students go over some lecture material prior to class, and we spend most of the lecture time explaining anything that the students had trouble but leave enough time for groups of students to solve a coding problem (relevant to the lecture material of course). The last part of the lecture is spent going over the answers of each student group and answering any questions. This presents a technology issue: it would be too much of a hassle to connect each student's laptop to the projector in order to show
their answers to the entire class. The answer would be to set up a server where the students can connect and solve the problem in Jupyter notebooks on the server. [Jupyter Hub](https://jupyter.org/hub) would be the solution, but I didn't want to have all the students connect to my laptop.

Here's where the [the Littlest JupyterHub (TLJH)](https://github.com/jupyterhub/the-littlest-jupyterhub) comes in, which is a distribution that helps you provide Jupyter Notebooks to 1-50 users on a single server (hosted on a cloud provider potentially). In this post, I will document how I set up TLJH on the Google Cloud.

The first step involves logging in to the [Google Cloud Console](https://console.cloud.google.com/) and creating a new VM instance. You can keep the default options except for:

-   Change the Boot Disk image from `Debian GNU/Linux 9 (Stretch)` to `Ubuntu 18.04 LTS`
-   Disable any service accounts (under `Identity and API access`)
-   Check the **Allow HTTP Traffic** and **Allow HTTPS Traffic** checkboxes under `Firewall`
-   Customize the `Startup script` under `Management, disks, networking, SSH keys`
    with the following

    ```sh
      #!/bin/bash
      curl https://raw.githubusercontent.com/jupyterhub/the-littlest-jupyterhub/master/bootstrap/bootstrap.py \
        | sudo python3 - \
          --admin <admin-user-name>
    ```

After creating the VM and waiting a few minutes for TLJH to be installed, grab
the external IP of your VM (without the ~ <https://> ~ part) and login to your new
server. If you click on the `Control Panel` and the `Admin` link, you can add
users (i.e. your students). Now we can have prepared Jupyter notebooks on the
cloud, that each student can work on and go over the problems/answers from a
single machine!
