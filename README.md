# Aleo-Testnet-Beta-Guide
Prior testnets have shown that while consumer-grade hardware can technically participate as a prover, it is unlikely to be effective due to high level of competition.
Minimum 1000 credit required to be eligible.

![image](https://github.com/uangdrop/AleoTest/assets/128940865/8356a98b-2efe-494d-87e3-f877db5339f0)






------------------
# Requirement  
## Aleo Prover that is competitive, the machine will need more than these requirements.
![image](https://github.com/mztacat/Aleo-Testnet-Beta-Guide/assets/31314340/bb2a8efd-77d5-48ed-ab63-9f55e5f793ec)







## Updating System 
```
sudo apt update && sudo apt update -y
```
![Screenshot_17](https://github.com/uangdrop/AleoTest/assets/128940865/02999566-bbac-489b-a284-cf99b058976f)



### Install GIT

```
sudo apt install git
```
Reply with ```y``` and continue 


![image](https://github.com/uangdrop/AleoTest/assets/128940865/efa1aa00-2259-4b73-a581-d1d75a743f2b)

### Install Build tool
```
sudo apt install -y build-essential clang libc6-dev libcurl4 libssl-dev
```
### Install Screen
```
sudo apt install screen -y
```

## Install Rust 

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

```
Reply with ```1``` and Enter


### Set Environment PATH
```
. "$HOME/.cargo/env"
source ~/.bashrc   
```

### Update RUST & Check version 
```
rustup update
rustc --version
```
![image](https://github.com/uangdrop/AleoTest/assets/128940865/06bff890-264e-4b36-a793-013e1b3744b4)





## Clone SnarkOS Repository 
```
git clone --branch mainnet --single-branch https://github.com/AleoNet/snarkOS.git
cd snarkOS
git checkout tags/testnet-beta
```
![image](https://github.com/uangdrop/AleoTest/assets/128940865/b285acfe-9576-4aac-b3b2-bd1be42013da)




## Install dependencies 
```
./build_ubuntu.sh
```
![image](https://github.com/uangdrop/AleoTest/assets/128940865/8525df43-49ff-4d65-ae68-2e5ca2d7c0c7)

![image](https://github.com/uangdrop/AleoTest/assets/128940865/b72fc2e9-0620-4f9b-b490-af28aafc0f59)



## Install SnarkOS 
```
cargo install --locked --path .
```
![image](https://github.com/uangdrop/AleoTest/assets/128940865/830edae7-7195-40cb-a1bf-54b46c764b2f)





## Open required port 

```
sudo ufw allow 4130/tcp
sudo ufw allow 3030/tcp
sudo ufw allow ssh
sudo ufw enable
``` 

Reply with ```y``` and Enter
```
sudo ufw status
```

![Screenshot_24](https://github.com/uangdrop/AleoTest/assets/128940865/2ebf1a2d-9e13-4962-9e8d-a60d7155b67b)



## Run ALEO Prover 

## Generate ALEO Account
### Save account details 
```
snarkos account new 
```
![Screenshot_25](https://github.com/uangdrop/AleoTest/assets/128940865/617537c2-a526-416a-b503-51b70269df20)



### Open Screen 
```
screen -S client
```






## Run Prover 
### 
```
cd $HOME && cd snarkOS
./run-prover.sh --network 1
```

Paste Your private key 


![Screenshot_26](https://github.com/uangdrop/AleoTest/assets/128940865/ccab8ae0-d4f2-4916-90d0-4e615b432ca4)




GINI DONE!!!


![image](https://github.com/uangdrop/AleoTest/assets/128940865/949a733d-0983-46d8-953f-5bf0098635ed)























