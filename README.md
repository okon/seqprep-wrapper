SeqPrep wrapper
========

## 1. About  
Forked from alhsu/AmpliVar. 
Using the first step of AmpliVar wrapper for merging reads, because SeqPrep is already pre-compiled for MacOS (and can be difficult to get working otherwise).

Full AmpliVar package can be found [here](https://github.com/alhsu/AmpliVar). For AmpliVar cite: 
Hsu, Arthur L., et al. "AmpliVar: Mutation Detection in High‐Throughput Sequence from Amplicon‐Based Libraries." Human mutation 36.4 (2015): 411-418.

## 2. Requirements  
+ **System Requirements**     
 * Linux operating system with BASH shell (pre-compiled binaries for Mac OSX 10.8 and Centos 6)  
 * 4G RAM (8G recommended)
 * Python 2 (2.6+)  

+ **Software Dependencies** (provided in the AmpliVar package):  
 * [SeqPrep](https://github.com/jstjohn/SeqPrep)      
 * [GNU Parallel](http://www.gnu.org/software/parallel/)

## 3. Installation     
  The source package also contains pre-compiled binaries needed to run AmpliVar under Mac OSX or Linux environments. 
  The binaries are compiled on Centos 6 and OSX 10.8.5. Please refer to the original sites for source code and/or 
  executable binary if the provided binaries do not work.  
  
  Using self-build or existing binaries is possible and can be achieved by either editing the section labelled 
  **"EDIT HERE TO USE SELF-BUILD BINARIES"** in the  wrapper script - *seqprep_wrapper.sh* to point path to 
  binaries to new location, or by using the **-e** switch, which gives preference to binaries in system path (and 
  still uses packaged binaries where one cannot be located).   
  
  To install this SeqPrep wrapper, download the repo:   
  ```    git clone https://github.com/okon/seqprep-wrapper.git    ```  



## 4. Usage and Program Options    
+ **File naming and formats**   
	 * Paired FASTQ files in the input directory must have the suffix of "_R1.fastq.gz" or "_R2.fastq.gz".  


+ **Wrapper options**   
     **WARNING:** *When used on Mac OS, only the short options are supported.*   
     
     A list of options can be displayed using ```seqprep_wrapper.sh -h```   
     
     ```   
     GENERAL OPTIONS   
     [-i|--input <INPUT_DIR>]          Path to directory containing the FASTQ files. REQUIRED (when checkpoint is not specified)  
     [-o|--output <ANALYSIS_DIR>]      Path to directory to output results of analysis. REQUIRED   
     [-t|--threads <THREADS>]          Number of parallel threads. Default=2  
     [-d|--adapters <ADAPTERS>]        Adapters used in the assay NEXTERA or TRUSEQ. REQUIRED (if -a and -b are not set)  
     [-a|--adapter_fwd <ADAPTER_FWD>]         Forward adapter sequence  
     [-b|--adapter_rev <ADAPTER_REV>]         Reverse adapter sequence  
     [-f|--filter <KEY>]               Process only files containing KEY. Default=all files.  
     [-e|--system-exe]                 Use executables in system PATH where available, instead of packaged executables  
     [-h|--help]                       Print this help message  
     [-v|--version]                    Print Version  
    
     ```     



## 5. References
 * O. Tange (2011): GNU Parallel - The Command-Line Power Tool, ;login: The USENIX Magazine, February 2011:42-47.



