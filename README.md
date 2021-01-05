# libnet

Course project for Aalto University course TU-C9270. Visualizing networks of Python dependencies in Github projects.

### Setup
1. Create a file called ".env" in the root of the project
2. Get an OAuth2 token for your GitHub user (see https://docs.github.com/en/free-pro-team@latest/developers/apps/building-oauth-apps)
### Using
- You can run libnet simply with
```
python libnet.py
```
This builds a network of 10 library nodes and displays it with MatPlotLib and NetworkX
- You can specify the size of the network by giving it as a parameter
For example
```
python libnet.py 500
```
builds a network of 500 library nodes
- Libnet saves a snapshot of the current network for every 15 library nodes added and also after running the program to completion
- You can continue from the previous snapshot by giving "--continue" or "-c" as a parameter after the desired size of the network
```
python libnet.py 1000 --continue
```
After running the previous command this would continue from a size 500 network and build it until it has 1000 library nodes
