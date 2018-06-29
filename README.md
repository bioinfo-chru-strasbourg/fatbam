######################################
# FATBAM [0.9.9b-31/05/2018]
# FATBAM clipping & coverage on amplicons
# Antony Le Bechec @ IRC © GNU-GPL
#######################################

################
# Requirements #
################
# Reference genome (e.g. hg19.fa)
# PICARD >=1.95
# SAMTOOLS >=1.2
# BEDTOOLS >=2.17
# JAVA >=1.8


#################
# Usage example #
#################

# Clipping
./FATBAM.clipping.sh --bam=examples/sample.aligned.unclipped.bam --output=examples/sample.aligned.clipped.bam --manifest=examples/sample.manifest -v;
# Coverage
./FATBAM.coverage.sh --bam=examples/sample.aligned.clipped.bam --output=examples/sample.aligned.clipped.bam.coverage --manifest=examples/sample.manifest -v;
column -t examples/sample.aligned.clipped.bam.coverage;



#######################################
# FATBAMClipping [0.9.3b-11/05/2018]
# FATBAM clipping
# Antony Le Bechec @ IRC © GNU-GPL
#######################################
# RELEASE NOTES:
# 0.9b-30/05/2016: Script creation
# 0.9.1b-01/06/2016: Deletion of temporary files
# 0.9.2b-02/06/2016: Few bugs corrected
# 0.9.3b-11/05/2018: Temporary files in a temporary folder. Few bugs fixed.

# USAGE: FATBAM.clipping.sh --bam=<BAM> --manifest=<MANIFEST> --output=<OUTPUT> [options...]
# -b/--bam              Aligned SAM/BAM file (mandatory)
# -m/--manifest         MANIFEST file (mandatory)
# -c/--chr              Filter reads on chromosome (defaut all reads)
# -a/--clipping_options Clipping options
# -o/--output           Clipped Aligned BAM file (defaut *clipped.bam)
# -e/--env              ENVironment file
# -r/--ref              REFerence genome
# -p/--picardlib        PICARD Library (disabled if ENV)
# -s/--samtools         SAMTOOLS (disabled if ENV)
# -l/--bedtools         BEDTOOLS (disabled if ENV)
# -t/--tmp              Temporary folder option (default /tmp)
# -u/--threads          number of threads for multithreading and samtools option (default 1)
# -z/--compress         compress level samtools option, from 0 to 9 (default 0)
# -x/--multithreading   Multithreading option (default false, need make installed)
# -v/--verbose          VERBOSE option
# -d/--debug            DEBUG option
# -n/--release          RELEASE option
# -h/--help             HELP option
#


#######################################
# FATBAMCoverage [0.9.3b-31/05/2017]
# FATBAM coverage calculation on amplicons
# Antony Le Bechec @ IRC © GNU-GPL
#######################################
# RELEASE NOTES:
# 0.9b-02/06/2016: Script creation
# 0.9.1b-28/03/2017: Bug fixed on output if no primers defined
# 0.9.2b-11/05/2017: Temporary files in a temporary folder. Bug fixed.
# 0.9.3b-31/05/2017: Multithreading. Bug fixed.

# USAGE: FATBAM.coverage.sh --bam=<BAM> --manifest=<MANIFEST> --output=<OUTPUT> [options...]
# -b/--bam              Aligned and clipped BAM file (mandatory)
# -m/--manifest         MANIFEST file (mandatory)
# -s/--unclipped        Indicates if the BAM file is NOT clipped (yet) (default: 0/FALSE, means that the BAM IS clipped)
# -c/--chr              Filter reads on chromosome (defaut all reads)
# -o/--output           Coverage file from Aligned BAM file depending on Manifest (defaut BAM.coverage)
# -e/--env              ENVironment file
# -r/--ref              REFerence genome
# -p/--picardlib        PICARD Library (disabled if ENV)
# -i/--picard           PICARD JAR (disabled if ENV)
# -s/--samtools         SAMTOOLS (disabled if ENV)
# -l/--bedtools         BEDTOOLS (disabled if ENV)
# -j/--java             JAVA (disabled if ENV, default 'java')
# -t/--tmp              Temporary folder option (default /tmp)
# -u/--threads          number of threads for multithreading and samttols option (default 1)
# -x/--multithreading   Use multithreading (default FALSE)
# -v/--verbose          VERBOSE option
# -d/--debug            DEBUG option
# -n/--release          RELEASE option
# -h/--help             HELP option




