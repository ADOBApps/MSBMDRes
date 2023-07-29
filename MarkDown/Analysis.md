# DynamicProps
1. RMSD:
 	`
 	DynamicProps --rcorr --sele1="select all" --sele2='select all' --input=system.dump --output=rmsd.xvg
 	_OR_
 	DynamicProps --rcorr --input=system.dump --sele1="select SOLUTE"  --output=rmsd.xvg
 	` 
	 	_IN_ Output_file.rcorr _OR_ rmsd.xvg _ADD_
@ title "Root-Mean Squared Displacement"
@ xaxis  label "Time (fs)"
@ yaxis  label "corrVal"
@ TYPE xy
@ subtitle "RMSD"

2. Radial_MSD:
 	`
 	DynamicProps --r_rcorr --sele1="select all" --sele2='select all' --input=system.dump --output=radial_msd.xvg
 	_OR_
 	DynamicProps --r_rcorr --input=system.dump --sele1="select SOLUTE"  --output=radial_msd.xvg
 	` 
	 	_IN_ Output_file.r_rcorr _OR_ radial_msd.xvg _ADD_
@ title "Radial Mean Squared Displacement"
@ xaxis  label "Time (fs)"
@ yaxis  label "Radial MSD (nm)"
@ TYPE xy
@ subtitle "MSD (radial projection)"

3. Directional msd for particles with unit vectors
 	`
 	DynamicProps --drcorr --sele1="select all" --sele2='select all' --input=system.dump --output=directional_msd.xvg
 	_OR_
 	DynamicProps --drcorr --input=system.dump --sele1="select SOLUTE"  --output=directional_msd.xvg
 	`
	 	_IN_ Output_file.rcorr _OR_ directional_msd.xvg _ADD_
@ title "Directional Mean Squared Displacement"
@ xaxis  label "Time (fs)"
@ yaxis  label "radius (nm)"
@ TYPE xy
@ subtitle "DirectionalRCorrFunc"
@ legend on
@ legend box on
@ legend loctype view
@ s0 legend "r2"
@ s1 legend "rparallel"
@ s2 legend "rperpendicular"


# StaticProps
{ statFileFormat = ""; }::Option:
TIME, TOTAL_ENERGY, POTENTIAL_ENERGY, KINETIC_ENERGY,
TEMPERATURE, PRESSURE, VOLUME, CONSERVED_QUANTITY, HULLVOLUME, GYRVOLUME,
TRANSLATIONAL_KINETIC, ROTATIONAL_KINETIC, LONG_RANGE_POTENTIAL,
SHORT_RANGE_POTENTIAL, VANDERWAALS_POTENTIAL, ELECTROSTATIC_POTENTIAL,
METALLIC_POTENTIAL, HYDROGEN_BONDING_POTENTIAL, RECIPROCAL_POTENTIAL,
SURFACE_POTENTIAL, BOND_POTENTIAL, BEND_POTENTIAL, DIHEDRAL_POTENTIAL, 
INVERSION_POTENTIAL, RAW_POTENTIAL, RESTRAINT_POTENTIAL, PRESSURE_TENSOR,
SYSTEM_DIPOLE, SYSTEM_QUADRUPOLE, HEATFLUX, ELECTRONIC_TEMPERATURE, COM,
COM_VELOCITY, ANGULAR_MOMENTUM, POTENTIAL_SELECTION

- Default
@ title "Statistic Props"
@ xaxis  label "Time (fs)"
@ yaxis  label "propVal"
@ TYPE xy
@ subtitle "StatProps"
@ legend on
@ legend box on
@ legend loctype view
@ s0 legend "Total Energy(kcal/mol)"
@ s1 legend "Potential Energy(kcal/mol)"
@ s2 legend "Kinetic Energy(kcal/mol)"
@ s3 legend "Temperature(K)"
@ s4 legend "Pressure(atm)"
@ s5 legend "Volume(A^3)"
@ s6 legend "Conserved Quantity(kcal/mol)"

- EnergyMinimization
@ title "Statistic Props"
@ xaxis  label "Time (fs)"
@ yaxis  label "propVal"
@ TYPE xy
@ subtitle "StatProps"
@ legend on
@ legend box on
@ legend loctype view
@ s0 legend "Potential Energy(kcal/mol)"

- All
@ title "Statistic Props"
@ xaxis  label "Time (fs)"
@ yaxis  label "propVal"
@ TYPE xy
@ subtitle "StatProps"
@ legend on
@ legend box on
@ legend loctype view
@ s0 legend "Total Energy(kcal/mol)"
@ s1 legend "Potential Energy(kcal/mol)"
@ s2 legend "Kinetic Energy(kcal/mol)"
@ s3 legend "Temperature(K)"
@ s4 legend "Pressure(atm)"
@ s5 legend "Volume(A^3)"
@ s6 legend "Conserved Quantity(kcal/mol)"
@ s7 legend "Hullvolume"
@ s8 legend "Gyrvolume"
@ s9 legend "Translational Kinetic"
@ s10 legend "Rotational Kinetic"
@ s11 legend "Long Range Potential"
@ s12 legend "Short Range Potential"
@ s13 legend "Vanderwaals Potential"
@ s14 legend "Electrostatic Potential"
@ s15 legend "Metallic Potential"
@ s16 legend "Hydrogen Bonding Potential"
@ s17 legend "Reciprocal Potential"
@ s18 legend "Surface Potential"
@ s19 legend "Bond Potential"
@ s20 legend "Bend Potential"
@ s21 legend "Dihedral Potential"
@ s22 legend "Inversion Potential"
@ s23 legend "Raw Potential"
@ s24 legend "Restraint Potential"
@ s25 legend "Pressure Tensor"
@ s26 legend "System Dipole"
@ s27 legend "System Quadrupole"
@ s28 legend "Heatflux"
@ s29 legend "Electronic Temperature"
@ s30 legend "Com"
@ s31 legend "Com Velocity"
@ s32 legend "Angular Momentum"
@ s33 legend "Potential Selection"
