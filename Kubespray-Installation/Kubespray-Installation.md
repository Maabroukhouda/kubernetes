# Kubespray Installation
## 1. Clone the Repository from GitLab
Clone the Kubespray repository from the GitLab server:

```
 git clone https://gitlab.proxym-group.net/it/infra-automation-hub/automation-modules/kubespray.git
```

**Authentication:**

Username: Houda.mabrouk
Password: Use a GitLab token with read access (Personal Access Token recommended)

```
Cloning into 'kubespray'...
Username for 'https://gitlab.proxym-group.net': Houda.mabrouk
Password for 'https://Houda.mabrouk@gitlab.proxym-group.net':
``` 

## 2.Switch to the Target Branch
Checkout the bcrg-uat branch for UAT environment deployment:
```
git checkout bcrg-uat
```

 ## 3.  Install System Dependencies
Install required Python packages and virtual environment tools:
```
sudo apt update
sudo apt install python3-pip python3-venv
```
## 4. Create Python Virtual Environment
Create a dedicated directory and virtual environment for Kubespray:
```
mkdir kubespray-venv
```
Initialize the virtual environment:
```
python3 -m venv kubespray-venv/
```

## 5. Activate Virtual Environment
Activate the virtual environment:
```
 source kubespray-venv/bin/activate
```
![image](/uplodes/kube1.png)

## 6. Install Python Dependencies
Navigate to the Kubespray directory and install required Python packages:
```
cd kubespray
pip install -U -r requirements.txt
```
## 7. Install Ansible Collections
Install the required Ansible collection for common operations:
```
ansible-galaxy collection install m4eba.common
```
