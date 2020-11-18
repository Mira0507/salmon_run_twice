## Q: Do two Salmon runs in a row give exactly the same counts? 

### 1. with --gcBias & --seqBias 

1st run: 

```bash

#!/bin/bash

samples=(Mock_72hpi_S{1..3} SARS-CoV-2_72hpi_S{7..9})

rawdir=../rawdata

prefix=gc-seq-quant1


for read in ${samples[*]} 
do
    salmon quant -i ../salmon_sa_index_hg19 -l A --gcBias --seqBias -r $rawdir/$read.fastq.gz -p 8 --validateMappings -o $prefix/${read}.quant
done

```

2nd run: 

```

```



### 2. with --gcBias 

### 3. with --seqBias

### 4. without --gcBias & --seqBias 


