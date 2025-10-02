# UT Capitole Blacklists Sync

## Overview

This GitHub Actions workflow automatically downloads and releases domain blacklists from the University of Toulouse (UT) Capitole. 

## Workflow Details

The workflow performs the following steps:

1. **Download**: Retrieves the latest blacklists archive from UT Capitole
2. **Extract**: Unpacks the downloaded archive
3. **Process**:
   - Flattens domain lists from different categories
   - Creates three versions of each list:
     - Raw domain list
     - Domain list prefixed with `0.0.0.0` for blocking
     - Domain list prefixed with `172.16.10.10` for routing to specific IP
4. **Release**: Uploads processed lists as a GitHub release

## Source

Blacklists are sourced from: https://dsi.ut-capitole.fr/blacklists/

## License

Please refer to the original UT Capitole blacklists for licensing information.