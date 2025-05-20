**Getting Familiar with open source EDA tools**

- **Sky_L1_openLANE Directory structure in detail**

The openlane_working_dir contains pdks,openlane. We are using skywater sky130A as it is compatible with opensource EDAs. Sky130A contains libs.ref and libs.tech which is technology and tool specific respectiverly.
![directory](https://github.com/user-attachments/assets/283380a6-47a5-4fbe-9dd2-3143228c16dc)

- **Sky_L2 Design Preparation Step**

using `docker` command in openlane for design preparation and then using  
`prep -design picorv32a`
![docker_ss](https://github.com/user-attachments/assets/40c58089-4978-4ee5-a98d-f6defbeed5bb)

- **Sky_L3 Review file after design prep and run synthesis**

A run directory is created which has results(contains synthesis, floor planning,etc), reports(timing analysis), logs, tmp, config.tcl shows default parameters taken by run
![run_directory](https://github.com/user-attachments/assets/98ed03c4-c941-40f4-b511-1c0acd4d89f3)
Inisde tmp directory Merged.lef is created.
![kuch](https://github.com/user-attachments/assets/93e16d93-0591-425a-b1ea-222d0fd3e9db)
layer and via level information using command `less merged.lef`
![idk](https://github.com/user-attachments/assets/7eeb5505-6602-4d8b-8ebf-a2bda8c3b3e1)

- **Sky_L4-OpenLANE Project Git Link Description**
- **Sky_L5 Steps to characterize synthesis results**
  After running the command `run_syntheis`, flop ratio is calculated by taking total no of flops / total no of cells = 1613 / 14876 = 0.1084 i.e 10.84%
  ![ratio_flop](https://github.com/user-attachments/assets/297b1b57-cbbc-4e53-a775-ca8ed02596f8)
  Inside the run folder we will see what are the changes made. There is a syntheised netlist after synthesis before it was empty.
  ![syn_netlist](https://github.com/user-attachments/assets/0377e243-34d8-4705-b98f-e52c483c898c)
  All the reports generated
  ![report_timing](https://github.com/user-attachments/assets/5560504b-f629-4e09-b3c9-3a46f9fd10e8)




