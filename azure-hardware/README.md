## Azure SEV-SNP hardware reference values
On Azure, the SEV-SNP hardware measurement is the launch measurement of the paravisor (openHCL). 
The paravisor boots first; therefore, the launch measurement measures the paravisor and not the guest OS.
For more information about the paravisor, see [here](https://techcommunity.microsoft.com/blog/windowsosplatform/openhcl-the-new-open-source-paravisor/4273172).

### Experiment: measuring the hardware quote
Three different images produced the same exact hardware quote except for PCRs and init_data (data provided by the hypervisor at launch). The images that were used are RHEL, Fedora, and FCOS.

### Conclusion
As long as the paravisor stays the same, the measurement will not change and the hardware quote will be valid.

#### Measurements:
`AMD-SEV-SNP-v5.hq` - The hardware quote for DCasv5 and DCadsv5-series CPU, which is the AMD EPYC (Milan) model.

