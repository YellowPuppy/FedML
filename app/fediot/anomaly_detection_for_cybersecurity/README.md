## Prepare Dataset
Prerequisite: install `unar` command line tool (https://theunarchiver.com/command-line).

At the server and client side, run the following script under data directory:
```
bash download.sh
```

## Training Script

At the client side, the client ID (a.k.a rank) starts from 1.
Please also modify config/fedml_config.yaml, changing the `client_id_list`, `client_num_per_round`, `worker_num` 
as the number of clients you plan to run.

For this application, the number of clients is up to 9 since there are 9 types of devices in N-BaIoT dataset.

At the server side, run the following script:
```
bash run_server.sh
```

For client 1, run the following script:
```
bash run_client.sh 1
```
For client 2, run the following script:
```
bash run_client.sh 2
```
Note: please run the server first.

## A Better User-experience with FedML MLOps (open.fedml.ai)
To reduce the difficulty and complexity of these CLI commands. We recommend you to use our MLOps (open.fedml.ai).
FedML MLOps provides:
- Install Client Agent and Login
- Inviting Collaborators and group management
- Project Management
- Experiment Tracking (visualizing training results)
- monitoring device status
- visualizing system performance (including profiling flow chart)
- distributed logging
- model serving