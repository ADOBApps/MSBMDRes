# Commands

## waterBoxer Hmat{{300,0,0}, {0,300,0}, {0,0,300}}
$ waterBoxer -x 300 -y 300 -z 300 -l 0 -m


## omd-solvator
This generate a unitary file with water and solute

$ omd-solvator -u NP15_5K_prevBox.omd -v freshWater.omd -n 887 -p 907924 -o NP15_5K_Box.omd

## solvator carves a solute void in OpenMD water box
$ solvator -i myWaterB.omd -p mySolute.pdb -o mySys.omd
_OR_
$ solvator -i myWaterB.omd -x mySolute.xyz -o mySys.omd

## Analysis files Remember add Rotule info
#
@    title "RMSD"
@    xaxis  label "Time (ns)"
@    yaxis  label "RMSD (nm)"
@TYPE xy
@ subtitle "Backbone after lsq fit to Backbone"