# bonnie-release

Bonnie++ BOSH Release

Sample instructions assuming using BOSH Lite
```
sudo route add -net 10.244.0.0/16
bosh -e lite upload-release releases/bonnie++/
bosh -e lite -d bonnie++ deploy manifests/example.yml
bosh -e lite -d bonnie++ run-errand bonnie++
bosh -e lite -d bonnie++ ssh
```
