**Getting Familiar with open source EDA tools**

**Sky_L1_openLANE Directory structure in detail**

The openlane_working_dir contains pdks,openlane. We are using skywater sky130A as it is compatible with opensource EDAs. Sky130A contains libs.ref and libs.tech which is technology and tool specific respectiverly.
![directory](https://github.com/user-attachments/assets/283380a6-47a5-4fbe-9dd2-3143228c16dc)

**Sky_L1_openLANE Design Preparation Step**

We are suing docker in open lane for design preparation using command 
`prep -design picorv32a`
![docker_ss](https://github.com/user-attachments/assets/40c58089-4978-4ee5-a98d-f6defbeed5bb)
A run directory is created
![run_directory](https://github.com/user-attachments/assets/98ed03c4-c941-40f4-b511-1c0acd4d89f3)


