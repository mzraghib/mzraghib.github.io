## Find the index of an element in a vector:



## Notes on Vectors:
1) Use 'reshape' function to initialize the shape of a multidimentional vector.
  e.g, if you do Vec.reshape(2) then you can access Vec[0] and Vec[1] directly to assign values

2) Use 'reserve'  function to reserve memory for a vector of a known size. 
This makes execution faster since the vector doesn't have to be resized as data is pushed into it.
