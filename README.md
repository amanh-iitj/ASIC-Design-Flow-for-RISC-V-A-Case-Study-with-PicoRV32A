# ASIC-Design-Flow-for-RISC-V-A-Case-Study-with-PicoRV32A


# Section 1 tasks:-

- Run 'picorv32a' design synthesis using OpenLANE flow and generate necessary outputs.
- Calculate the flop ratio.

## Design preparation and initiate Openlane

![Screenshot from 2024-05-27 11-22-45](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/2a09579c-da4a-454e-ba36-687e6205442d)

![Screenshot from 2024-05-27 11-36-33](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/7791eab0-3070-40b1-80ec-0db1f6b58c3b)

## Design Specifications of picorv32a

![Screenshot from 2024-05-27 11-36-33](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/0f80d2a1-a80c-4da5-acc3-2f3ed194675f)

## Run synthesis

![Screenshot from 2024-05-27 11-49-54](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/08d5d42a-02c9-4cd9-a59e-eb339d7b5183)

![Screenshot from 2024-05-27 11-33-36](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/4244c9f4-b5f7-41de-998c-1e42c92ffa92)

## STA report

![Screenshot from 2024-05-27 12-07-34](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/29f78cc5-e4b1-42df-904a-f74f4394cb04)

![Screenshot from 2024-05-27 12-07-23](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/ed05b8ab-e73c-4d19-a53f-ca832e285dfb)


## Characterise synthesis results

![Screenshot from 2024-05-27 11-56-56](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/0254fda9-1161-483b-b871-a1cb52046215)

![Screenshot from 2024-05-27 12-00-24](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/d026cd35-784e-4ff1-b87d-cdc85df364bf)

![Screenshot from 2024-05-27 11-56-24](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/ccba3fff-cb04-420a-aeac-45d718eb45ef)

- We know, Flop ratio = Number of counter D-FF / Number of total cells
- Flop ratio = 1613 / 14876 = 0.1084
- Flop ratio % = 10.84


# Section 2 tasks:-

- Run 'picorv32a' design floorplan using OpenLANE flow and generate necessary outputs.
- Calculate the die area in microns from the values in floorplan def.
- Load generated floorplan def in magic tool and explore the floorplan.
- Run 'picorv32a' design congestion aware placement using OpenLANE flow and generate necessary outputs.
- Load generated placement def in magic tool and explore the placement.

## Review floorplan files

![Screenshot from 2024-05-27 23-46-56](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/c59fdb93-0cbf-44ae-b896-826f561cd3b9)

![Screenshot from 2024-05-28 13-08-24](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/a95f2778-7c55-47e3-ae64-cdcf1180dbe0)

![Screenshot from 2024-05-28 13-04-43](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/4e482775-64fe-428e-9ada-8f0679f00c54)

![Screenshot from 2024-05-27 23-17-42](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/66901b96-a237-4945-ab9e-e30147dd83cc)

![Screenshot from 2024-05-28 13-09-01](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/36676065-7ffb-4279-9401-9ffcb3c7fa6a)

- From the picorv32a.def file, it is seen that width of chip is 660.685 micrometer and height of the chip is 671.405 micrometer. 

## Floorplan layout in Magic

![Screenshot from 2024-05-27 23-25-50](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/478e02bd-eb6b-481e-bf59-8aae5e312942)

![Screenshot from 2024-05-27 23-49-19](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/0abb122a-b883-4b4c-8740-54ddbb8c0b89)

![Screenshot from 2024-05-27 23-48-03](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/b0fa5dd1-6ed3-44b4-aea4-0510cf11bcc4)

## Congestion aware placement using RePlAce

![Screenshot from 2024-05-28 12-56-13](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/623ebb9c-5e23-4e63-967a-989ce691f96a)

![Screenshot from 2024-05-28 12-56-56](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/7c0f8e9f-fe9b-49dc-b81b-25086fe7a8f0)

![Screenshot from 2024-05-28 12-57-09](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/72a4c600-d204-4e1d-a126-edca3311a777)


# Section 3 tasks:-
- Clone custom inverter standard cell design from github repository: Standard cell design and characterization using OpenLANE flow.
- Load the custom inverter layout in magic and explore.
- Spice extraction of inverter in magic.
- Editing the spice model file for analysis through simulation.
- Post-layout ngspice simulations.
- Find problem in the DRC section of the old magic tech file for the skywater process and fix them.

## IO placer revision

![Screenshot from 2024-05-29 12-51-00](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/c7375c51-2ddf-4e12-ae99-0885459a583d)

## Clone custom inverter standard cell design from github repository and load the custom inverter layout in magic

![Screenshot from 2024-05-30 20-49-17](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/04f3c746-b4b1-4875-83f2-9d87724e956e)

![Screenshot from 2024-05-30 21-03-12](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/0ce66388-c892-4ae1-888a-59bd250aa6a1)

## pshort.lib

![Screenshot from 2024-05-30 21-31-14](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/7a738cad-6ddf-428b-81db-bf406ffb7bcf)
 
## Spice extraction of inverter in magic

![Screenshot from 2024-05-30 21-49-26](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/aaf736fe-d2f6-4919-9a52-87e34a50969d)

## ngspice simulation

![Screenshot from 2024-05-30 22-36-57](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/c289787e-09f0-4541-91ef-7b95b5f81f9e)

![Screenshot from 2024-05-30 22-37-32](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/cba97ec5-8d7b-4b11-a5ae-395d65da6706)

## Characterize inverter using sky130 model files

![Screenshot from 2024-05-30 23-17-07 (1)](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/cabd2728-892e-4a86-8b84-b9bda9fe9d30)

- Rise time
  (2.246 - 2.182)e-09 = 64psec
- Fall time
  (4.095 - 4.051)e-09 = 44psec
- Propagation delay
  (2.210 - 2.150)e-09 = 60psec
- Cell fall delay
  (4.077 - 4.050)e-09 = 27psec

## Content of .magicrc file 

![Screenshot from 2024-05-31 21-14-58 (1)](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/46003628-2c24-42df-9846-e101c3d0f06c)

![Screenshot from 2024-05-31 21-15-58](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/166a53d6-4f22-4983-a124-baaa233c9b23)

## Lab introduction to Magic tool options and DRC rules

![Screenshot from 2024-05-31 21-18-52](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/5522ac97-6959-47d9-bd76-2450af2bc100)

![Screenshot from 2024-05-31 21-20-05](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/e01fae5f-672c-4567-9541-9d0d97a99a12)

![Screenshot from 2024-05-31 21-52-42](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/97fb507b-9269-47df-b7be-c72e99f75d91)

![Screenshot from 2024-05-31 21-50-41](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/1ef5bb28-5b41-4b23-8c34-7a9cfb5c9fef)

## Lab exercise to fix poly.9 error in Sky130 tech-file

![Screenshot from 2024-05-31 21-58-47](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/6e658e83-1f2f-4250-8fc3-70a6def6c516)

![Screenshot from 2024-05-31 22-26-33](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/73f81d1c-758f-48e0-84eb-f6140ec369df)

![Screenshot from 2024-05-31 22-27-39](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/fd8750e7-9a39-4b7f-8643-064f6b92d2be)

## Lab challenge exercise to describe DRC error as geometrical construct

![Screenshot from 2024-05-31 22-50-03](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/33b67270-2e52-43f4-954b-3e23f8408b6d)

![Screenshot from 2024-05-31 22-52-06](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/ba095386-42e4-4c21-a3ce-d9f77fc37311)

![image](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/7a65e767-b5bd-437f-96cf-5a0df4bd2267)

## Lab challenge to find missing or incorrect rules and fix them

![Screenshot from 2024-05-31 23-01-20](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/9f47206e-ca91-4ad2-937d-853fed427a5c)


# Section 4 tasks:-
- Fix up small DRC errors and verify the design is ready to be inserted into our flow.
- Save the finalized layout with custom name and open it.
- Generate lef from the layout.
- Copy the newly generated lef and associated required lib files to 'picorv32a' design 'src' directory.
- Edit 'config.tcl' to change lib file and add the new extra lef into the openlane flow.
- Run openlane flow synthesis with newly inserted custom inverter cell.
- Remove/reduce the newly introduced violations with the introduction of custom inverter cell by modifying design parameters.
- Once synthesis has accepted our custom inverter we can now run floorplan and placement and verify the cell is accepted in PnR flow.
- Do Post-Synthesis timing analysis with OpenSTA tool.
- Make timing ECO fixes to remove all violations.
- Replace the old netlist with the new netlist generated after timing ECO fix and implement the floorplan, placement and cts.
- Post-CTS OpenROAD timing analysis.

## Lab steps to convert grid info to track info

![Screenshot from 2024-06-01 12-02-57](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/50e30f5c-76ff-42c6-a1fd-18e824eb48ac)

![Screenshot from 2024-06-01 12-10-27](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/ee6c97ec-419c-4a02-a14d-70e702418562)

![Screenshot from 2024-06-01 12-14-53](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/9823df8d-4ff8-4afd-92e9-ec8a1817c282)

## Lab steps to convert magic layout to standard cell LEF

![Screenshot from 2024-06-01 12-20-18](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/7835700b-c117-459a-b085-03e138654911)

![Screenshot from 2024-06-01 12-24-20](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/8f4aa1ee-6567-4bbd-80da-c92d14373c26)

## Introduction to timing libs and steps to include new cell in synthesis

![Screenshot from 2024-06-01 12-29-43](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/d762f8e0-7f50-431d-aa31-d6e5f4265774)

![Screenshot from 2024-06-01 12-29-46](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/eaf334ba-e193-4a0b-83b3-dadb1d2ae92a)

## sky130_vsdinv.lef

![Screenshot from 2024-06-01 12-24-54](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/ae14fb32-d37c-4aee-800a-5f0f4caca752)

## Different library files

![Screenshot from 2024-06-01 12-32-45](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/c7b0a99a-c3e2-41ea-a9d6-b0b1b0cebe75)

![Screenshot from 2024-06-01 12-35-03](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/64368cfd-b05f-4be7-8a1a-c3ef4fcd279a)

![Screenshot from 2024-06-01 12-35-16](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/05490d6d-83b1-4336-b35b-f55e1dbe697b)

## config.tcl file 

![Screenshot 2024-06-04 200637](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/070442ae-b6fe-484a-b17a-25c17641cef6)


## OPENLANE execution
- Commands:

  ./flow.tcl -interactive

  package require openlane 0.9

  prep -design picorv32a

  set lefs [glob $::env(DESIGN_DIR)/src/*.lef]      

  add_lefs -src $lefs

  run_synthesis

![Screenshot from 2024-06-01 12-47-47](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/a4d373bc-f107-43de-90a1-39d79f1fe432)

![Screenshot from 2024-06-01 12-49-15](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/b849cd23-b5bd-476f-8179-fe3a5066531a)

## README.md file

![Screenshot from 2024-06-01 13-22-17](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/9ff9fa35-28a1-48db-8cb7-b5effc6a568e)

## Re-synthesis for reduced slack

![Screenshot from 2024-06-01 13-31-33](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/000204d8-c04b-47f8-97c8-3146b0afe303)

![Screenshot from 2024-06-01 13-54-49](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/94bcdc4f-b3a5-453e-8b4a-8905af118495)

## Floorplan and Placement
- Commands:

  init_floorplan

  place_io
  
  tap_decap_or

![Screenshot from 2024-06-02 22-20-24](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/3ff976cc-3907-4323-8746-748b75a63d04)

![Screenshot from 2024-06-02 22-20-47](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/cf94cb0a-b7c3-4ab8-bdfd-a99a885e36ea)

![Screenshot from 2024-06-02 22-20-54](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/21518fa3-7be0-4d05-bf73-535746f3cae0)

![Screenshot from 2024-06-02 22-22-04](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/fd6fea61-ac9f-4582-9899-2086acd47d63)


## Placement succesfully generated

![Screenshot from 2024-06-01 19-42-24](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/3acb9c97-0993-4d35-99e7-733d3e65e936)

## Running expand window in tckon

![Screenshot from 2024-06-02 22-26-33](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/476c95a3-c322-4d88-979a-b55f485fc845)

![Screenshot from 2024-06-02 22-28-27](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/82f7f77e-a53c-493b-9dd9-51d3b56e4888)

![Screenshot from 2024-06-02 22-28-41](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/877a1a13-806a-4066-8b6a-fb0444c905f4)

## Post-Synthesis timing analysis with OpenSTA tool

- Commands:

  #Change directory to openlane

  cd Desktop/work/tools/openlane_working_dir/openlane

  #Command to invoke OpenSTA tool with script

  sta pre_sta.conf

![Screenshot from 2024-06-03 12-42-04](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/12f4e2e1-0403-4ad4-846a-69a8b702baa4)

## pre_sta.conf file

![Screenshot from 2024-06-02 14-14-14](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/03415ebe-a0b6-4c29-bccc-8da786de0ace)

## my_base.sdc file

![Screenshot from 2024-06-02 14-12-21 (1)](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/4a6d82b2-4bd7-4143-a06e-055cdd6760b5)

## Make timing ECO fixes to remove all violations

- Commands:

  #Reports all the connections to a net

  report_net -connections _12771_

  #Checking command syntax

  help replace_cell

  #Replacing cell

  replace_cell _15446_ sky130_fd_sc_hd__o21bai_4

  #Generating custom timing report

  report_checks -fields {net cap slew input_pins} -digits 4

![Screenshot from 2024-06-03 12-43-48](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/754dfbb1-5fa3-4433-8016-b46082e54241)

![Screenshot from 2024-06-03 12-44-58](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/64bb5e8d-a8bf-49a4-9f45-573b4dbdbc94)

![Screenshot from 2024-06-03 12-43-09](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/9f3dd500-c0f9-4257-8aae-896e19784054)

![Screenshot from 2024-06-03 12-45-36](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/6cc7f5a7-0f71-4615-83e0-2ed8c4c75f65)

- Slack is reduced from -5.59 to -5.5031

## Cell getting replaced

![Screenshot from 2024-06-03 12-45-57](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/f77c402d-9495-4d04-9507-f4a45d613d57)

## Replace the old netlist with the new netlist generated after timing ECO fix and implement the floorplan, placement and cts

![Screenshot from 2024-06-03 12-55-59](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/6b471a90-54ba-407d-ab3b-d47ac391a9aa)

## Write verilog file

![Screenshot from 2024-06-03 12-55-42](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/f03e18ef-39de-4a75-b3a6-4b9cd022bf12)

## Verified that the netlist is overwritten

![Screenshot from 2024-06-03 12-59-28](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/b080051b-1f55-4b07-a700-935c249905e8)

## Load the design and run necessary stages

![Screenshot from 2024-06-03 13-02-41](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/83d3f957-6fa4-43f0-a976-fae0269cdbd2)

![Screenshot from 2024-06-03 13-03-39](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/53f5fd24-a5ca-495c-92e2-9c175f141501)

![Screenshot from 2024-06-03 13-05-52](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/484fc7a3-33eb-4bd0-93af-a27bddf5857d)

## cts.tcl

![Screenshot from 2024-06-03 13-08-34](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/9dd6dd49-f091-46c8-b102-bd7c8d56dade)

![Screenshot from 2024-06-03 13-08-46](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/b9dd3575-85f4-428b-a013-79f1e58a8984)

## or_cts.tcl

![Screenshot from 2024-06-03 13-11-10](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/e37b99d2-0f47-4f94-9342-a859e87f99bf)

![Screenshot from 2024-06-03 13-11-21](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/e65da2c2-6d75-45c4-a18b-afc1097997d9)

## Post-CTS OpenROAD timing analysis

![Screenshot from 2024-06-03 17-33-08 (1)](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/c1d94c30-5049-4b4e-b58a-1fa51ac93565)

![Screenshot from 2024-06-03 17-36-51 (1)](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/8142a276-b6c6-4e25-91e0-f1e50ae534da)

![Screenshot from 2024-06-03 17-37-13 (2)](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/60c1d463-29ce-4bd3-8d33-ea8abb3d7e1a)

![Screenshot from 2024-06-03 17-37-24](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/9f58836c-5ed5-41d7-a24c-f87ec22b9d0c)

![Screenshot from 2024-06-03 17-37-33](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/ed2646c8-2692-4476-9aee-3d70f5a63ec9)

![Screenshot from 2024-06-03 17-37-56](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/af8b2b4d-d4b6-45f7-bac3-277d32a21c79)

## Post-CTS OpenROAD timing analysis 

![Screenshot from 2024-06-03 17-40-06](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/ec13eac7-fd90-434b-b294-ff4e74ba4573)

![Screenshot from 2024-06-03 17-41-08](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/8262dd92-4d32-45f9-80c5-dce6266d6537)

![Screenshot from 2024-06-03 17-44-13](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/a401fe2e-f51e-411f-8c7e-7f9718d0539d)

![Screenshot from 2024-06-03 17-44-39](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/27f97015-bad3-47bc-bcfd-edcad0d439c8)

![Screenshot from 2024-06-03 17-44-44](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/f83b0fc4-3fee-4a7f-b490-6a35e8432f6d)

![Screenshot from 2024-06-03 17-45-09](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/e9d56740-36b7-4f12-92c5-3207622e7b76)

![Screenshot from 2024-06-03 17-45-58](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/a5ed38e2-471e-4c61-8f02-671b95a235d6)



# Section 5 tasks:-
- Perform generation of Power Distribution Network (PDN) and explore the PDN layout.
- Perfrom detailed routing using TritonRoute.
- Post-Route parasitic extraction using SPEF extractor.
- Post-Route OpenSTA timing analysis with the extracted parasitics of the route.

## Perform generation of Power Distribution Network (PDN)

![Screenshot from 2024-06-03 21-19-05](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/cb897a62-c727-488d-b4d8-7e552dd4e45e)

## Load PDN def in magic in another terminal

- Commands:

  #Change directory to path containing generated PDN def

  cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/03-06_15-41/tmp/floorplan/

  #Command to load the PDN def in magic tool

  magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read 14-pdn.def &

![Screenshot from 2024-06-03 21-21-12](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/d50a5dc7-a23e-463b-90a3-39b81205b363)

![Screenshot from 2024-06-03 21-22-05](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/b06fdd80-badd-4463-b62f-df62fe9f89ba)

![Screenshot from 2024-06-03 21-22-10](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/e6834d4d-6ce0-47a9-8295-91368f45c71b)

![Screenshot from 2024-06-03 22-02-29](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/ad819144-09d4-47f6-90d6-2a24ff64e764)

## Perform detailed routing using TritonRoute and explore the routed layout

![Screenshot from 2024-06-03 21-23-45](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/539d3fc5-0af9-42d4-9768-0b703f2cd63d)

![Screenshot from 2024-06-03 21-40-34](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/6677bd01-b23c-4718-a6ca-45b93fb67a7b)

## Load routed def in magic

- Commands:

  #Change directory to path containing routed def

  cd Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/03-06_15-41/results/routing/

  #Command to load the routed def in magic tool

  magic -T /home/vsduser/Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.def &

![Screenshot from 2024-06-03 22-12-24](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/e8115836-1a93-48a5-a51d-366586fe0d1d)

![Screenshot from 2024-06-03 22-06-48](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/75572598-922e-4cc9-a663-ef3138e1bafb)

![Screenshot from 2024-06-03 22-08-34](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/e9f32f8c-cb8d-448b-98a0-53b8c1795c7b)

![Screenshot from 2024-06-03 22-02-35](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/661ebc00-c21f-4b35-9af1-f9ad34d69eaf)

![Screenshot from 2024-06-03 22-03-06](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/917855c5-f3a8-44dc-a387-0c98f3fd62c3)

## fastroute.guide file

![Screenshot from 2024-06-03 22-05-23](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/2367c823-dd63-4de6-b6b5-6f2dc18f569a)

![Screenshot from 2024-06-03 22-05-27](https://github.com/amanh-iitj/SOC-Design-and-Planning/assets/155350256/d314b083-4124-48a7-bd38-1eb86027721a)

## Post-Route parasitic extraction

- Parasitics command is already run and spef is extracted
- In runs folder, where routing outputs are dumped and we'll find the SPEF there. 

- Commands:

  #Command extract spef

  python3 main.py /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/03-06_15-41/tmp/merged.lef 
  /home/vsduser/Desktop/work/tools/openlane_working_dir/openlane/designs/picorv32a/runs/03-06_15-41/results/routing/picorv32a.def
