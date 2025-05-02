# YUPANA


<img width="448" alt="image" src="https://github.com/user-attachments/assets/38c01d8e-1d0d-43e4-ae39-9d9884747ee1" />


THE YUPANA APPROACH
Yupana is an online tool that: a) estimates the environmental impacts of a prototype, b) compares the impacts of different prototyping materials and techniques, c) provides information ab out the user’s choices, and d) gives sustainability suggestions to guide potential changes in the user’s initial decisions. The calculations are made per life phase of a prototype, and the details are as follows:

**The Four Phases of a Prototype Life Cycle**
The calculator focuses on two main environmental impacts that are present in the four phases of a prototype life cycle: energy consumption and CO2 emissions. Both environmental impacts are calculated using different parameters depending on the phase.

**Raw Material Processing phase:**
This phase includes the total processing energy (MJ) used to make the prototyping material. It comes from the embodied energy (ee), which is defined as energy to produce one kilogram of material including all processing inefficiencies [1]. We also consider the CO2 emissions generated in the process.
In equation (1), the total material manufacturing energy (Emm total) is calculated by multiplying the sum of prototyping material mass ( 𝑝𝑚), which includes final product and waste material from the number of iterations, and the sum of embodied energy per kg ( 𝑒𝑒) of it. In (2), the mass of the total raw material processing CO2 emissions (CO2mm total) is calculated by multiplying the sum of prototyping material mass ( ), and the sum of material processing CO2
emissions per kg of material (𝐶𝑂2𝑚𝑚).
Assumptions: The values used for the calculations are the embodied energy (ee) and CO2 emissions of materials (CO2mm) when they are primary manufactured and processed. This information is available from LCA-databases and software or literature sources such as Ashby [2].

**Transportation phase:**
This phase includes the total transportation energy (MJ) used to deliver the prototyping material to the fabrication site. It is calculated by an energy factor (efi) (MJ/metric ton * km) that represents the relationship between the type of transportation used and the amount of energy needed per km to transport 1 ton of material. The distance di (km) traveled per mode is considered. We also included the CO2 emissions generated in this phase, coming from a similar emissions factor (CO2fi) (kgCO2/kg) per travel mode.

In equation (3), the total transportation energy (Et total) is calculated by multiplying the sum of prototyping material mass ( 𝑝𝑚) with the sum of energy factor (efi) multiplied by the distance traveled di per mode. That result is divided
by 103 to transform the units from ton to kg. In equation (4), the total transportation CO2 emissions (CO2t total) are calculated by multiplying the sum of prototyping material ( 𝑝𝑚) with the the sum of CO2 factor (CO2fi) times distance
traveled di (km) per mode. That result is divided also by 103 to transform the units from ton to kg.
Assumptions: The energy factor values are from the following types of transportation: Short haul aircraft driven by kerosene, Ocean driven by shipping-diesel fuel, 32 metric ton truck driven by diesel fuel, 14 metric ton truck driven by diesel fuel, and light goods vehicle driven by diesel fuel. The user can pick the material’s traveling distance in between international (8000-9500 km), national (3500-4200 km) and local(300-370km). The calculator automatically picks the minimum or maximum value based on the user’s choice.

**Digital Fabrication phase:**
This phase includes the total digital fabrication energy (MJ) used to make a prototype, which is related to the prototyping time (seconds) and the amount of power (Watt) a machine uses. We also included the CO2 emissions associated with the electricity used to run the machines, which depends on the electricity generation (from fossil fuels, nuclear energy, or renewable energy sources).
In equation (6), the total digital fabrication energy (Edf total) is calculated by multiplying the digital fabrication power (Pdfi) in each mode, stand-by, idle, and 3D printing or laser cutting, with the respective time (ti) for stand-by, idle, and 3D printing or laser cutting. This is divided by 106 to transform the units from Watt seconds to MJ. Since we assume that the machine electricity is the only source for CO2 emissions in this life cycle phase, in equation (7), the total digital fabrication CO2 emissions (CO2df total) are calculated by multiplying the total digital fabrication energy (Edf total) from equation (6) with the electricity emissions factor CO2df (kgCO2/kWh) and dividing by 3.6 to transform the interim units from MJ to kWh.
Assumptions: The calculator’s data base has values of two 3D printers (MakerBot Replicator+ and Ultimaker 2 Extended), and three laser cutters (Trotec Speedy 400, Epilog Fusion Pro 32, and Universal PLS6.75). The minimum and maximum power values of the machines were taken from the manufacturer data sheets.

**End of Life phase:** 
This phase includes the total energy (MJ) a disposal facility uses to process the prototyping waste and transport energy. The waste can be recycled, incinerated, or disposed off in the landfill. We considered transportation energy as one of the parameters to include in this phase, as well as the CO2 emissions associated with the transportation distances the waste travels to reach those facilities.

In equation (10), the total end of life recycling energy (Erc total) is calculated by multiplying the sum of prototyping material waste mass (Í 𝑝𝑚𝑤) with the sum of energy used to recycle a material (Í𝐸r), which is the difference between the embodied energy recycling (MJ/kg) and the heat of combustion recycling value (MJ/kg). The result is added to the sum of energy used to transport the waste material (Í𝐸tw). In (11), the transportation of waste energy (Etw) is calculated multiplying the sum of prototyping material waste (Í𝑝𝑚𝑤), by the sum of energy factor (Í
𝑒 𝑓 ) which isthe result of multiplying the type of transportation energy factor by the distance the material waste traveled (km). That result is divided by 103 to transform the units from ton to kg. This equation equals the total end of life landfill energy (Elf total). In (12), the total recycling CO2 at the end of life (CO2rc total) is calculated by multiplying the sum of
prototyping material waste (Í𝑝𝑚𝑤), which includes wasted material and number of iterations, by the sum of CO2 generated recycling a material (Í𝐶𝑂2𝑟 ), which is the difference between the CO2 emission recycling (MJ/kg) and the CO2 combustion recycling values (MJ/kg). The result is added to the sum of CO2 emissions generated to transport the waste material (Í𝐶𝑂2𝑡𝑤). In (13), the transportation of waste generated CO2 emissions (CO2tw) and it is calculated multiplying the sum of prototyping material waste (Í𝑝𝑚𝑤), by the sum of CO2 factor (Í𝐶𝑂2 𝑓 ) which is the result of multiplying the type of transportation CO2 factor by the distance the material waste traveled (km). That result is divided by 103 to transform the units from ton to kg. This equation is equals to the total CO2 generated when the waste is landfilled (CO2lf total).
Assumptions: All waste is transported to a facility to later decide the end of life of it (recycling, incineration, landfill). The distance to a recycling or incineration facility goes from 29 to 305 km, and to the landfill is from 87 to 160 km. Even though the calculator shows a very small environmental impact when the waste is landfilled, that is only making reference to energy and CO2 emissions, but there are other qualitative impacts to take into account such as soil depletion, green houses emissions, land use, among others.






For more information please contact eldylazaro@gmail.com

