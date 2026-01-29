# GitHub traffic

GitHub reports traffic to a repository in the Insights/Graphs section of a repository.
This includes the number of visits to the repository, the number of times it was
cloned each day, popular pages, and referring sites.
The number of visitors and the number of clones are only reported for two weeks (14 days).
This information is also available via the GitHub API.

## Installation

Install this project in a Python environment (`python -m venv venv`) using pip:

    pip install git+https://github.com/MTG/github-traffic.git

A script will be installed to `github_get_traffic/`

## Configuration

Create a directory to save the output of the script to.

Copy the configuration file, `github_traffic/config.ini`. You can put it in the same directory
that you created above.

Open GitHub settings, and go to the section *Personal access tokens*. Create a new
token. The only permission that this key needs is `public_repo`, to read statistics
for a public repository.

## Running

To activate the virtual environment (venv):

    .\venv\Scripts\Activate.ps1

Run the script, specifying the path to the config file and the output directory:

    github_get_traffic -c <location_of_config.ini_file> -o <output_directory>
   
e.g., 
   
    github_get_traffic -c gh_traffic/config.ini -o gh_traffic

This script can be run weekly via cron to maintain a complete record of historical data.

