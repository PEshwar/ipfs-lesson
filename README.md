## IPFS setup and test instructions

### Download IPFS tar here
```
https://dist.ipfs.io/#go-ipfs
```

### Untar file and install locally

```
tar xvfz <tar file name>

cd go-ipfs

./install.sh

```

### Check if installed correctly and list commands

```
ipfs help
```

### Initialize IPFS repository. This will create a key-pair for your node and a repository with some ipfs objects

```
ipfs init

```

### Type the command that is shown as output from previous step

```
/ipfs/QmS4ustL54uo8FzR9455qaxZwuMiUhyvMcX9Ba8nUH4uVv/readme
```

### Add files to ipfs

```
echo "Some text!" > IPFSfile
ipfs add IPFSfile

```

### See which files are on your system

```
ipfs pin ls
```
#### This should list all files and also show the file you created

## Interact with Swarm
### start IPFS network daemon

```
ipfs daemon
```

### Check details of your connectoin from another terminal window

```
ipfs id
``` 

### To configure CORS:

####Stop IPFS daemon with ctrl-c
```
ipfs config -- json API.HTTPHeaders.Access-Control-Allow-Methods ‘[“PUT”, “GET”, “POST”, “OPTIONS”]’
ipfs config — json API.HTTPHeaders.Access-Control-Allow-Origin ‘[“*”]’
ipfs daemon
```


### Get list of peers
```
ipfs swarm peers
```

### Inspect peers 

```
ipfs id <insert hash>
```
  
### IPFS daemon sets up a localhost which allows you to interact with IPFS through browser. Default port is 8080

```
localhost:8080/ipfs/<hash of file>
```

### There is also a web-ui

```
127.0.0.1:5001/webui
```


