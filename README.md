# gdist
API for genetic distance and presence queries

This for the moment is intended as a scratch space where we can
propose ideas for how to send queries back/forth between different
genome databases/datastores based on sequence queries and sketches. 
Once it gets coherent we can ask more widely
for advice.


## use cases

### SNP panels
 - Query: here is my panel of snps (defined by sequence probes), please query your database with these, and send me genotypes for all of your samples/datasets

## Gene presence
 - Query: which of your samples have this sequence
 
## Nearest neighbours
 - Query: here is a sketch of my sample - which of yours is closest? which are the 10 closest using mash distance?
 - Query: here is a set of SNP probes, and genotypes for my sample. please send me your closest 10, using distance measure X.
 
## distance definitions
 - types of mash
 - definitions of SNP distance, incl what to do for missing and for hets
 
 
 # query format
 
 
 
 
