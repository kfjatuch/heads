To build for the Librem 2nd generation (Librem 13 v2/v3 and Librem 15 v3/v4),
we need to have the following files in this folder:
* cpu_microcode_blob.bin  - CPU Microcode
* descriptor.bin - The Intel Flash Descriptor
* fspm.bin - FSP 2.0 Memory Init blob
* fsps.bin - FSP 2.0 Silicon Init blob
* me.bin - Intel Management Engine

To get the binaries, run the get_blobs.sh script which will download and
verify all of the files' hashes, then run me_cleaner on the descriptor.bin and me.bin.

You can now compile the image with:

```
make BOARD=librem13v2
```
