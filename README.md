## BUILD

cd chaos &&

mkdir build &&

cd build &&
 
cmake -DCMAKE_BUILD_TYPE=[Debug,optimized] .. &&

make

./stream_test - measures time to encrypt 1GiB of 1s

## MISC

generator state is the current point of the rossler attractor with constants
A=0.4263, B=2, C=4 

gen32 returns a mix of each point's mantissa 

156 bits of entropy(?tbd) -> 3 64 bit seeds, using only 52 bits of each

stream tested with the testu01 library. multiple runs of BigCrush, Rabbit (100MB
500MB 1GB) FIPS_140_2, have not reported any p values outside accepted ranges 
so far
