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

### Gene presence
 - Query: which of your samples have this sequence

 
### Nearest neighbours
 - Query: here is a sketch of my sample - which of yours is closest? which are the 10 closest using mash distance?
 - Query: here is a set of SNP probes, and genotypes for my sample. please send me your closest 10, using distance measure X.
 
### distance definitions
 - types of mash
 - definitions of SNP distance, incl what to do for missing and for hets
 
 
 ## query API
 
### database_status()
 returns (date of last change, query types supported)
 
 ### sequence_presence_count(string, id_thresh)
  returns count of how many samples/datasets contain this sequence, up to some identity

 ### sequence_presence_count(string, id_thresh, taxid)
 if database does not support taxid filters, return false.
 else returns count of how many samples/datasets contain this sequence, up to some identity,
  and a boolean confirming these have all been filtered to be that species.
  and an enum specifying how taxid was assigned.
  
 ### sketch_neighbour(sketch value, sketch type, sketch database identifer, number)
 return <number> closest samples to sketch-value using sketch database with identifier in query.
 eg Refseq as of such-and-such date
  



 ### sequence_presence_ids(string, id_thresh)
  returns count and identifiers of samples within id_thresh of string
  
  
  
 
 
