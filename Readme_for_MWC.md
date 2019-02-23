1) Clone the repo. on both the k8s cluster master (where kubectl is available).
2) cd gcp-live-k8s-visualizer
3) Run the following command after changing the HOST IP on both the clusters:
    nohup kubectl proxy --www=. --address='10.255.136.148' --accept-hosts='^10.255.136.148$,^[::1]$': &
4) Open index.html on any one of the clusters and update IPs below "<!-- CHANGE THE IP IN data ATTRIBUTE BELOW-->" one by one.
4) Load the following url after updating IP of the master chosen in step (4).
    http://10.255.136.148:8001/static
