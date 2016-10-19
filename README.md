# Extraction pipeline

This project includes tools required to perform metadata analysis. Specifically, it uses Apache Tika to parse metadata from various files and then builds inverted index using solr.


## Quick Start Using Docker

1. Get and install docker for your operating system (if not already) https://www.docker.com/products/docker
2. Build a docker image. This can be done by    
<code>docker build . -f docker/Dockerfile -t imagecat2</code>  
3. Create a directory called 'testbed'. Create the following folder structure inside testbed: 
    testbed/HT_extractions/data_urllist
    testbed/HT_extractions/data_imagelist
    testbed/HT_extractions/data_extracted
    testbed/HT_extractions/data_logs
    testbed/HT_extractions/data_images
4. Place the python codes from https://github.com/asitang/Memex-Hbase.git into a code_folder
5. Place all part files in HT_extractions/data_urllist
6. Start the container
<code>docker run -it -d -v /path_to_testbed/:/mnt -v /path_to_code_folder:/code imagecat2</code>  
7. From inside the container run  
<code>cd /code</code>  
<code>python p_pipeline.py</code>  




## Developers




 
  



