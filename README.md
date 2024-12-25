# Network3 Node Ubuntu Setup
![image](https://github.com/user-attachments/assets/c6a4568b-340e-4cef-8bc0-62d6f873fe95)

## Deployment

#### Step 1: Update & Install Curl
```sh
sudo apt update && sudo apt install curl
```

#### Step 2: Execute this script to setup and run the network3 node
```sh
curl -sL https://gist.githubusercontent.com/rinkashimee/98fedf4f048e6ba4ed70eaf7fc18ea83/raw/449eea514436ba3c970026a821e4c0019048dc0b/network3.sh | bash
```
##### Results:
![image](https://github.com/user-attachments/assets/562ca1e4-04da-4766-80c6-1dcd0d17549c)

#### Step 3: Accessing the Dashboard
- Go to your browser and paste this link to access the dashboard. Make sure to change `xx.xx.xx.xx` to your **VPS IP**.
```sh
https://account.network3.ai/main?o=xx.xx.xx.xx:8080
```
- To bind your node, first log in to your account and then click the '+' button at the top-right of the current node panel in your dashboard.

  ![image](https://github.com/user-attachments/assets/9e78196c-4fc5-4054-963f-82041fbb606c)

- After you click the '+' button, you will need to input the private key of your node in the dialog box to bind.

  ![image](https://github.com/user-attachments/assets/02c2ca52-aa56-45c2-9426-7bcd2d00f523)

- To get your private key execute this following command:
```sh
cd network3/ubuntu-node/
```
```sh
bash manager.sh key
```
 ![image](https://github.com/user-attachments/assets/acef8549-35fb-46ff-b86e-2971814fd657)

- Congratulations! You have successfully bind your node.

 ![image](https://github.com/user-attachments/assets/3d51c347-fb0b-4357-94b9-1f0c8ce4f0d4)

## Command

- Run your network3 node.
```sh
cd network3/ubuntu-node/
```
```sh
bash manager.sh up
```
- Stop your network3 node.
```sh
cd network3/ubuntu-node/
```
```sh
bash manager.sh down
```
- Get your node private key.
```sh
cd network3/ubuntu-node/
```
```sh
bash manager.sh key
```

## NOTICE: 
What needs to be explained here is that this `xx.xx.xx.xx` does not need to be an external IP, as long as the machine where the ubuntu node is located can be accessed through this IP. Of course port 8080 needs to be open to allow access from other machines.
