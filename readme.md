**mitoRNA** is a Python2.7 wrapper designed to ease the target assembly of mitogenomes from RNA-Seq and a starting referenc(es). The tool uses an iterative approach, alternating *reference-mapping* and *de novo-assembly*, until the number of reads which map to the assembly reach a *plateau*.

![Image description](https://github.com/for-giobbe/mitoRNA/blob/master/pipeline.png)


---

Additional tools which are required for running mitoRNA are Bowtie2 and Trinity, which can easily be installed using ```conda```. An help page can be racalled using the command ```-h```.

Example of usage: 
```
mitoRNA.py -I reference.fasta -M paired -1 left.fastq -2 right.fastq -P 16 -T metazoa -O output
```

List of arguments:
```
Required Arguments:
  -h, --help    show this help message and exit
  -R FASTA      Fasta file with the reference mitochondrial genome
  -M MOD        reads type: paired - unpaired
  -1 FASTQ1     mate 1 containing the raw reads
  -2 FASTQ2     mate 2 containing the raw reads
  -U SINGLE     Fastq containing the raw reads
  -O OUT        Output directory

Optional Arguments:
  -P THREADS    Number of threads, (1)
  -C            Full clean up (delete all intermediate files)
  -N END        maximum number of iterations
 ```
 
 ---

For citation and additional information read the relative paper [Complete mitochondrial genomes from transcriptomes](https://www.nature.com/articles/s41598-019-51313-7) or get in touch with Giobbe at forni.giobbe@gmail.com.
