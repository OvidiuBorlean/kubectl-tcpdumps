# kubectl plugin for tcpdumps


## Running tcpdumps inside a Kubernetes Node with this kubectl plugin. 

## Prerequisites

- tcpdump binary already installed on the Node.
- Outbound connectivity for downloading the azcopy binary from Microsoft side. This is used for uploading the capture file to a Storage Account
- SAS - Environment variable with "Blob SAS Url" with write permissions

## Usage:

kubectl-plugin <nodeName> <capTime>

Where nodeName is the Node where the capture will be executed and capTime is total time of capturing expressed in seconds








