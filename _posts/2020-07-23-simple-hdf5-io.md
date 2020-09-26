---
layout: post
title: C++ header file only library for simple hdf5 file input/output
---


# [h5stream](https://github.com/srbhp/h5stream)
Header only library for HDF5 input/output


### Example

```
  // Create File
  h5stream file("sample.h5", "tr");

  // Create a vector
  std::vector<double> matrix { 1, 2, 3282, 932 };
  // Write to the file
  file.write<double>(matrix, "matrix"); // Call write_vector

  //Read data from the file
  auto xx = file.read<double>("matrix");
```


Source Code : [h5stream](https://github.com/srbhp/h5stream)

