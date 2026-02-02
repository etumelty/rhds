# rhds
# rhds
# rhds
git clone <[github URL](https://github.com/etumelty/rhds)>
cd rhds
mamba env create -f environment.yml
mamba activate rhds
Rscript install.r

# Setting up config.env
code config-template.env
# Since we know we'll need dedicated directories for data and results, we'll define these here but leave pseudo-paths as placeholders so that users will know that they need to replace these paths when working on their specific local environment:
datadir=/PATH/TO/DATA/DIR
resultsdir=/PATH/TO/RESULTS/DIR
docsdir=/PATH/TO/RESULTS/DIR
# Now that we have a config.template file to work from, we'll set up specific one for our environment. 
cp config-template.env config.env
# Replace the placeholder paths with the following.
datadir="/data/<username>/rhds/data"
resultsdir="/data/<username>/rhds/results"
docsdir="/data/<username>/rhds/results/docs"
# Add config.env to git.ignore
