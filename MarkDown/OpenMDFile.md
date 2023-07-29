<OpenMD>
  <MetaData>
    #include "water.inc"
    #include "NanoStruct.inc"

    component{
      type = "AuNP_887";
      nMol = 1;
    }

    component{
      type = "SPCE";
      nMol = 1;
    }

    minimizer{
      useMinimizer = false;  // Minimizer disable
      method = SD;           // Steepest descent
      maxIterations = 1000;
    }

    // ensemble = "NVT";                       // Equilibration 1
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
    runTime = 1e3;       // the total simulation run time
    seed = 985456376;    // Seed value for random number generator (improve reproducibility)

    tempSet = "true";
    thermalTime = 10;
    sampleTime = 100;
    statusTime = 2;

    // finalConfig = "sys_box_topol"; // name of output file box
    // finalConfig = "sys_minimized_topol"; // name of output file EnergyMinimization
    // finalConfig = "sys_NVT_topol"; // name of output file Equilibration 1
    // finalConfig = "sys_NPTi_topol"; // name of output file Equilibration 2

    // columns to print in the .stat file where each column is separated by a pipe (|) symbol.
    // (The default is the first eight of these columns in order.)
    // General (default)
    // statFileFormat ="TIME|TOTAL_ENERGY|POTENTIAL_ENERGY|KINETIC_ENERGY|TEMPERATURE|PRESSURE|VOLUME|CONSERVED_QUANTITY";
    // EnergyMinimization
    // statFileFormat = "TIME|POTENTIAL_ENERGY";


    useInitialExtendedSystemState = "false";
    usePeriodicBoundaryConditions = "false";
    useInitialTime = "false";
## Last run using OpenMD version: 2.6, revision: Release                                 
  </MetaData>
  <Snapshot>
    <FrameData>
      Time: 0
      Hmat: {{ 100, 0, 0 }, { 0, 100, 0 }, { 0, 0, 100 }}
      Thermostat: 0 , 0
      Barostat: {{ 0, 0, 0 }, { 0, 0, 0 }, { 0, 0, 0 }}
    </FrameData>
    <StuntDoubles>
      0 pq  0.0  0.0     0.0    1.0  0  0  0
      1 pq  -50  -47.5   -47.5   1   0  0  0
    </StuntDoubles>
  </Snapshot>
</OpenMD>
