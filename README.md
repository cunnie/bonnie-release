# bonnie-release

Bonnie++ BOSH Release

Sample instructions assuming using BOSH Lite
```
sudo route add -net 10.244.0.0/16
bosh -e lite upload-release releases/bonnie++/
bosh -e lite -d bonnie++ deploy manifests/example.yml
# to display IOPS/read (MiB/s)/write (MiB/s)
bosh -e lite -d bonnie++ run-errand bonnie++ |
  grep '^[0-9.]' | awk -F, -f misc/stats.awk
```
