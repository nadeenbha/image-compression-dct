
# Discrete Cosine Transform (DCT) Process

  

<p>As our use of and reliance on computers continues to grow, so too does our need for
efficient ways of storing large amounts of data. For example, someone with a web page or
online catalog — that uses dozens or perhaps hundreds of images — will more than likely need
to use some form of image compression to store those images. This is because the amount of
space required to hold unadulterated images can be prohibitively large in terms of cost.
Fortunately, there are several methods of image compression available today. These fall into
two general categories: lossless and lossy image compression. The JPEG process is a widely
used form of lossy image compression that centers around the Discrete Cosine Transform.
The DCT works by separating images into parts of differing frequencies. During a step
called quantization, where part of compression actually occurs, the less important
frequencies are discarded, hence the use of the term ”lossy.” Then, only the most important
frequencies that remain are used retrieve the image in the decompression process. As a
resut, reconstructed images contain some distortion; but as we shall soon see, these levels of
distortion can be adjusted during the compression stage. The JPEG method is used for both
color and black-and-white images, but the focus of this article will be on compression of the
latter.</p>

## Process

The following is a general overview of the JPEG process. Later, we will take the reader
through a detailed tour of JPEG’s method so that a more comprehensive understanding of the
process may be acquired.
  
1. The image is broken into 8X8 blocks of pixels.
2. Working from left to right, top to bottom, the DCT is applied to each block.
3. Each block is compressed through quantization.
4. The array of compressed blocks that constitute the image is stored in a drastically reduced
amount of space.
5. When desired, the image is reconstructed through decompression, a process that uses the

Inverse Discrete Cosine Transform (IDCT).

<b>Credits: </b>

  

1. Refferrence source : https://www.math.cuhk.edu.hk/~lmlui/dct.pdf
2. zigzag.py has been taken from : https://github.com/amzhang1/simple-JPEG-compression