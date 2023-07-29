  <MetaData>
    #include "water.inc"
    #include "NanoStruct.inc"

    component{
      type = "AuNP_887";
      nMol = 1;
    }

    minimizer{
      useMinimizer = false;  // Minimizer disable
      method = CG;
      maxIterations = 1000;
    }

    // ensemble = "NVT";                                  // Equilibration 1
    // ensemble = "LangevinHull";                      // Equilibration 2
    // ensemble = "NPTi";                      // Equilibration 2
    // ensemble = "NVE";
    forceField = "MnM";
    electrostaticSummationMethod = "shifted_force";
    electrostaticScreeningMethod = "damped";
    cutoffRadius = 9;
    switchingRadius = 9;
    dampingAlpha = 0.18;

    tempSet = "true";
    thermalTime = 10;
    sampleTime = 100;
    statusTime = 2;

    targetTemp = 300;     // K
    targetPressure = 1.0; // atm

    tauThermostat = 1e3; // constant temp
    tauBarostat = 1e4;

    dt = 1.0;            // the time step for integration
    runTime = 1e5;       // the total simulation run time
    seed = 985456376;    // Seed value for random number generator (improve reproducibility)

    tempSet = "true";
    thermalTime = 10;
    sampleTime = 100;
    statusTime = 2;

    // finalConfig = "sys_box_topol"; // name of output file box
    // finalConfig = "sys_minimized_topol"; // name of output file minimization
    // finalConfig = "sys_NVT_topol"; // name of output file Equilibration 1
    // finalConfig = "sys_NPTi_topol"; // name of output file Equilibration 2

    useInitialExtendedSystemState = "false";
    usePeriodicBoundaryConditions = "false";
    useInitialTime = "false";

## Last run using OpenMD version: 2.6, revision: Release                                 
  </MetaData>