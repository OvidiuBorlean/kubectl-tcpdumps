# kubectl plugin for tcpdumps


## Running tcpdumps inside a Kubernetes Node with this kubectl plugin. 

## Prerequisites

- tcpdump binary already installed on the Node.
- Outbound connectivity for downloading the azcopy binary from Microsoft side. This is used for uploading the capture file to a Storage Account
- SAS - Environment variable with "Blob SAS Url" with write permissions

## Usage:
'''
kubectl-tcpdumps nodeName capTime
'''
Where nodeName is the Node where the capture will be executed and capTime is total time of capturing expressed in seconds

If no upload to Azure Storage Blod is desired, the DaemonSet will mount a HostPath Directory (/tmp). After finishing operation the capture files can be downloaded directly from the Pod with the following command:

'''
#kubectl cp default/tcpdumps-xxxx:/tmp/$nodeName ./$nodeName.pcap
'''






