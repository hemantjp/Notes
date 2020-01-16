Regarding tar: just look at the "qwerty" keyboard. 
There are letters "zxcvf" next to each other.
You need either "tar czvf file.tar.gz files" or "tar xzvf file.tar.gz".


        x - extract files
        c - create archive
        t - list files
        v - verbose (list files as it processes them)
        j - use bz2 compression
        z - use gz compression
        f - read or write files to disk

Examples

Uncompress a tar.gz file: tar zxf tarball.tar.gz

Uncompress a tar.bz2 file: tar jxf tarball.tar.bz2

Create a tar.gz file: tar zcvf tarvall.tar.gz mydir/*
