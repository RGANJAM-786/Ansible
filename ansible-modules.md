<img width="898" height="810" alt="image" src="https://github.com/user-attachments/assets/b9e39471-36c2-41a1-9235-11abb29e2980" />


<img width="907" height="712" alt="image" src="https://github.com/user-attachments/assets/b9df9cae-4d98-4956-8e2d-6ac2f406bd41" />


<img width="907" height="752" alt="image" src="https://github.com/user-attachments/assets/6629f704-8644-4531-9b41-66d63dd7d565" />


<img width="960" height="773" alt="image" src="https://github.com/user-attachments/assets/6b6093e1-3469-481a-96aa-4448b8655e6b" />


<img width="902" height="731" alt="image" src="https://github.com/user-attachments/assets/ae70b767-9101-4363-aa07-d62e3f4203bd" />


<img width="921" height="815" alt="image" src="https://github.com/user-attachments/assets/dc926428-434a-4125-a9a4-b1192609d66a" />


✅ Quick Summary for Interviews


yum/apt → Install packages

service/systemd → Start/enable services

copy/template → Deploy config files

user/authorized_key → Manage users & SSH keys

file → Manage file permissions and directories

git → Deploy code from repositories

shell/command → Run commands

get_url/unarchive → Download and extract files

docker_container/docker_image → Manage containers



<img width="1067" height="802" alt="image" src="https://github.com/user-attachments/assets/9f12d80d-d451-4a51-ba9a-80f100f1835c" />



# ✅ Answer: Ansible Modules I Used in My Project


“In my project, I worked with several Ansible modules depending on the task:

apt / yum / dnf modules → Used for installing packages like Docker, Kubernetes tools, or Nginx on Linux servers.

Example: apt: name=docker.io state=present

copy and template modules → Used to push configuration files to servers.

Example: copying a Kubernetes kubeconfig file or templating Nginx config with variables.

service module → To start, stop, and restart services (like restarting Nginx after config change).

git module → To pull code directly from repositories when setting up applications.

shell / command modules → To execute commands (but I used them only when no specific module was available).

docker_container and docker_image modules → Used in automation for containerized deployments.

k8s module → To interact directly with Kubernetes clusters (creating deployments, services, etc.).

user and file modules → To create system users, manage permissions, and handle directories.

.

👉 Example from my project:

When setting up a new Kubernetes worker node, I used the apt module to install Docker, copy module to push the kubelet configs, and service module to start the kubelet.

For application deployment, I used the git module to pull the code, docker_image to build the image, and docker_container to run the app inside a container.


🔹 Scenario-Based Interview Questions on Ansible Modules

Q: You need to install Docker on 50 servers. How will you do it using Ansible?

A: I’ll use the apt module (for Ubuntu/Debian) or yum/dnf module (for RHEL/CentOS). Instead of manually logging into each server, Ansible will run the same playbook on all servers in parallel.

<img width="871" height="272" alt="image" src="https://github.com/user-attachments/assets/ff627e52-9f53-4f79-88a7-4d0ef3a0ccbf" />


Q: Your application needs a config file with environment-specific values (Dev, Staging, Prod). How will you manage this in Ansible?

A: I’ll use the template module with Jinja2 templates. This way, the same template file will adapt values based on variables defined in inventory or vars files.


Q: You deployed a new Nginx configuration file. How will you ensure Nginx restarts only when the config changes?

A: I’ll use the copy or template module with a notify handler that triggers the service module only when the file changes. This prevents unnecessary restarts.


Q: If you want to run a Git pull to fetch the latest application code, which module will you use?

A: I’ll use the git module. This is better than command: git pull because it’s idempotent (only updates when changes exist).

<img width="1003" height="692" alt="image" src="https://github.com/user-attachments/assets/4c407490-9cfa-4448-8d41-1f7743c1801f" />


<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/98b96517-28ff-4290-88dd-75edd5161fce" />


<img width="1050" height="591" alt="image" src="https://github.com/user-attachments/assets/cc78a111-e378-497e-b845-535d47763755" />


<img width="888" height="311" alt="image" src="https://github.com/user-attachments/assets/b7bac4d7-e477-414f-b635-0b507125cf01" />


<img width="905" height="557" alt="image" src="https://github.com/user-attachments/assets/e362efa0-a6a0-41ac-a10a-3d62fd8d9ea8" />


<img width="1085" height="526" alt="image" src="https://github.com/user-attachments/assets/8433b3e2-e832-454f-a069-987d71f4131d" />



✅ In short:


For server setup → apt, yum


For configs → template, copy, file


For apps → git, docker_container


For K8s → k8s


For services → service


<img width="962" height="468" alt="image" src="https://github.com/user-attachments/assets/16a808f6-1801-482e-87ca-a4282c88099a" />


<img width="917" height="366" alt="image" src="https://github.com/user-attachments/assets/f1be3cc8-12d1-444e-ad0b-e7e7ecce8382" />


<img width="1076" height="458" alt="image" src="https://github.com/user-attachments/assets/729ae732-2f24-484a-a239-391ab9117855" />


<img width="982" height="651" alt="image" src="https://github.com/user-attachments/assets/5158e106-d967-40a3-bbd0-0857822f4d52" />


<img width="1082" height="637" alt="image" src="https://github.com/user-attachments/assets/4b6ae618-6d92-4414-8f48-ecd435258b74" />


