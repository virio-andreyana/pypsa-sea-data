# pypsa-sea-data  
A ready-to-use package for modeling the Southeast Asia region with the latest version of pypsa-earth.

The content is based on the Master's Thesis [High Resolution Techno-Economic Analysis of Future Power Network Development in Southeast Asia](https://zenodo.org/records/14450500) by Virio Andreyana.

To run the premade scenarios:
1. Clone this repository next to your `pypsa-earth` repository.
2. Copy the contents of `pypsa-sea-data/configs` into `pypsa-earth/configs`.
3. Retrieve the necessary data bundle and cutouts by modifying the `enable` section in `config.sea.yaml`.
4. Place any config from the `scenarios-` folder into `pypsa-earth/configs/scenarios`.
5. Run the code using: `snakemake solve_all_networks`.

The content of `scenarios-pypsa-sea-v1` is an overnight foresight model of the Southeast Asia region with three optional **network topologies**:
- **exist**: Includes only existing interregional connections.
- **aims**: Includes all interregional connections proposed or discussed in the AIMS workpaper for the ASEAN power grid.
- **irena**: Includes all interregional connections modeled by IRENA's scenario.

And two **load options** for the year 2050:
- **1.5S-RE90**: Total electricity demand of 6413 TWh/a.
- **CNS**: Total electricity demand of 3528 TWh/a.

Future plans include premade scenarios for myopic foresight. Most of the coding development, however, is in the pypsa-earth repository.
