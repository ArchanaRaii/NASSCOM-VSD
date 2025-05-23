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


**Sky130 Day 2 - Good floorplan vs bad floorplan and introduction to library cells**

**SKY130_D2_SK1 - Chip Floor planning considerations**

- **SKY_L6 - Steps to run floorplan using openlane**
  
The floor plan switches located in openlane/configurations/README.md
![fp_variables](https://github.com/user-attachments/assets/620cd407-b897-4ce7-ad21-cd82f3638169)
Default parameters set for floorplan
![set_variables](https://github.com/user-attachments/assets/1ce1aaae-8089-450d-90ee-2699521b7f33)
Finally running command `run_floorplan`.
![view_def](https://github.com/user-attachments/assets/b549d895-1a0b-4ef3-885e-845c1a3fbab3)
Using the following data we can calculate the area if DIE
![file_def](https://github.com/user-attachments/assets/e6887a3e-63e4-4f9b-9ab8-54d09e55cff5)

To see actual layout after floorplan is done using magic:
![layout](https://github.com/user-attachments/assets/25947269-1039-41a6-9806-cb5b8d306072)

**SKY130_D2_SK2 - Library Binding and Placement**
- **SKY_L5 - Congestion aware placement using RePlAce**
Doing placement by running command run_placement
Following image is post placement design ensuring the standard cells are in standartial rows.
![palcement_ss](https://github.com/user-attachments/assets/341c1b7e-eb7d-46de-8f34-70b8f23f1d76)

**Sky130 Day 3 - Design library cell using Magic Layout and ngspice characterization**
**SKY130_D3_SK1 - Labs for CMOS inverter ngspice simulations**
- **SKY_L5 - Lab steps to git clone vsdstdcelldesign**
![spice](https://github.com/user-attachments/assets/33d00592-ff40-45bc-8036-bdf72d27c553)

**SKY130_D3_SK2 - Inception of Layout and CMOS fabrication process**
- **SKY_L8 - Lab introduction to Sky130 basic layers layout and LEF using inverter**
![spice1](https://github.com/user-attachments/assets/3b5031ec-4a78-4f14-b09d-5812efbe7496)

**SKY130_D3_SK3 - Sky130 Tech File Labs**
- **SKY_L1 - Lab steps to create final SPICE deck using Sky130 tech**
![spicee_1](https://github.com/user-attachments/assets/947c8cde-c40a-4d57-a90c-d6acef911aae)

- **SKY_L5 - Lab introduction to Magic and steps to load Sky130 tech-rules**
![mag_ss](https://github.com/user-attachments/assets/8923ac84-3ec0-48a5-87b4-1c00d0e8cb4e)
![ss_cifseeVIA2](https://github.com/user-attachments/assets/b39aa1de-04aa-43f4-bf9c-e450c66da5e5)

- **SKY_L6 - Lab exercise to fix poly.9 error in Sky130 tech-file**
![ok](https://github.com/user-attachments/assets/4ce8007d-0132-4de0-9a8d-58b95948cb9d)
![corrected_drc](https://github.com/user-attachments/assets/6f2a2408-0aac-4aae-a0ea-72a41d824c2c)















