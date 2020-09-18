# Overview and update
Version one of the mechanical design is based on a simple mechanical system single column system controlled by a 12V motor. Details of this are given below. Oxygen Concentrations > 90% have been achieved with this design. We are currently working on 1) A double column design to achieve a more continuous flow; 2) A completely pneumatic controlled design (which does not rely on any external power source); 3) lowering the energy consumption using a completely different approach to make this more suitable for off-grid locations; 4) designs of a compressor which can be fabricated locally with minimal equipment.

# Overview
The first version of our design uses a single column, making a very simple design. We use PSA drying to pre-dry the air before it enters the zeolite bed for oxygen concentration. Because one of our aims is to make this suitable for off-grid locations we have chosen to use a Li-X zeolite due to the significant enhancement of the N2/O2 adsorption selectivity compared to 13X zeolite. This means we can achieve lower energy consumption for compared to traditional 13X zeolite with the same volume of bed and operating operating pressure (e.g. see https://www.tandfonline.com/doi/abs/10.1080/01496399208018880).

# Materials
We have chosen to use common peumatic componets for this version of the design. We are continously seeking to simplify and make this more appropriate for off-grid locations. Please do feedback to us on any aspect of this/build one yourself and contibute back to the project through a pull request.

The follow is a list of materials required to build:
- 1x 3 Way 2 position valve (1/4 inch inlets and outlets) hand button operated.
- 2 x one-way valves (currently using fuel valves)
- 1x Regulator
- 2m FDA approved PVC reinforced tubing 8mm
- 2 or 3 inch ABS pipe with end-caps (for the zeolite columns)
- 1 x oxygen flowmeter (rotameter) 0-10 l/min
- Blow-tie valve (adjustable in-line pressure relief valve)
- 9 x 1/4 inch Male BSP, 8mm barbed tail fittings (used on the end of the columns to connect to the 8mm PVC tube)
- 9 x hose clips
- 1x 1/4 inch Pneumatic silencer
- 1 x orifice restrictors (these can be 3D printed/or fabricated with plastic rod) more details coming soon! Currently we use a variable restrictor here and tune to achieve a high oxygen purity.
- For controlling the cycling, in this first version we have used a 12V 16RPM high torque geared motor with a CAM and speed controller in order to easily try different speeds. We have new version that does not require any elecrical power and does not rely on a speed controller - soon to be released here.

# Schematic of set-up
Here's a rough sketch of the setup. (We'll be updating with a better diagram soon!):

<p align="center">
    <img src="/docs/_media/schematic_openO2.jpg" />
     <img src="https://github.com/EnAccess/OpenO2/blob/master/docs/_media/schematic_openO2.jpg" />
    
</p>

# How it works
The system cycles through the following steps:
1) Pressurisation - until there is sufficient pressure to allow oxygen to flow .through the blow-tie valve (set just below 2 bar).
2) Oxygen generation (Adsorption stage)- oxygen fills the surge tank.
3) Depressurization.
4) Regeneration - oxygen flows back from the surge tank through the orifice (in order to control the rate of flow back) to purge the bed.