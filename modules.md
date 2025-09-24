<img width="918" height="552" alt="image" src="https://github.com/user-attachments/assets/1567546f-925d-4667-9e8b-b11f7ca02fff" />


<img width="992" height="783" alt="image" src="https://github.com/user-attachments/assets/b30140a4-5ac8-43e4-996e-a933aed4db85" />


<img width="992" height="417" alt="image" src="https://github.com/user-attachments/assets/a24c063c-3144-4d30-b6b0-8648e4d46dd1" />


debug module in ansible
========================

The debug module in Ansible is a useful tool for outputting information during playbook execution. It helps you inspect variables, confirm task execution, and troubleshoot issues in your Ansible scripts.



<img width="1026" height="621" alt="image" src="https://github.com/user-attachments/assets/f8ce7705-5e73-4f5a-852c-735b13072260" />


<img width="940" height="602" alt="image" src="https://github.com/user-attachments/assets/98237b04-3ef1-4620-a1f1-a67247ac25cc" />


<img width="977" height="752" alt="image" src="https://github.com/user-attachments/assets/ea7bc9ed-8a5d-43f0-aaa9-2f5b662482c7" />


✅ Key takeaway for interviews:

I used debug to print variable values.

Found the root cause was wrong variable path/naming issue.

Fixed it and avoided a production misconfiguration.


<img width="992" height="603" alt="image" src="https://github.com/user-attachments/assets/1dbb58a9-3575-435f-9066-b95e426b5829" />


<img width="975" height="493" alt="image" src="https://github.com/user-attachments/assets/47115ea7-baf7-48e1-bdb3-d533924f3da0" />


<img width="970" height="647" alt="image" src="https://github.com/user-attachments/assets/257c73d6-c93a-4993-8808-9297b0fe7668" />



Handlers in ansible
====================

IQ] what is the difference between tasks and handlers?

--> Tasks are executed in the order they are defined in the playbook. All tasks will run every time the playbook is executed, unless certain conditions (like when statements) are specified.


--> Handlers are only executed when notified by a task. If a task makes a change (e.g., installing a package or modifying a file) and issues a notification to a handler, the handler will run after all tasks have been processed.

--> handlers are special kind of tasks, It will not executed by default, until other tasks are notify.


--> Handlers will execute at end of the play.


<img width="753" height="762" alt="image" src="https://github.com/user-attachments/assets/bbb066dc-e497-4ec8-ae0a-07c1f806c9a3" />



# ✅ Did you use handlers in your project?


👉 Yes, I used handlers in my project mainly for service restarts.

For example:

When I updated a configuration file (like nginx.conf or httpd.conf), I didn’t want the service to restart every time the playbook ran.

So, I used a handler, which is only triggered when the configuration file is actually changed.

Example: If template module updates nginx.conf, it notifies the handler → the handler runs → service restarts only if needed.

This avoided unnecessary restarts and helped in keeping deployments smooth.


# ✅ What is the difference between Task and Handler?


Task:

Runs every time the playbook is executed.
Example: Installing nginx or copying a file.

Handler:

Runs only when notified by a task (and only once, even if multiple tasks notify it).
Example: Restarting a service after a config change.


🔹 Interview-style Statement

👉 “In my projects, I used handlers to restart services only when configuration files were updated. The main difference is that tasks always run when called, while handlers only run when triggered. This makes handlers very useful for efficient service management.”


<img width="953" height="670" alt="image" src="https://github.com/user-attachments/assets/476e08c0-cae8-4aa9-bd5b-2e08949ee9b3" />


<img width="962" height="613" alt="image" src="https://github.com/user-attachments/assets/726728df-da13-4ce1-bf31-a5b57c4113b1" />



