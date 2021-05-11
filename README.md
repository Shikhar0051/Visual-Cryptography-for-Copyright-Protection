# Digital Watermark for Copyright Protection of Digital Images
## Introduction
The aim of this case study is to demonstrate a digital watermarking scheme using visual cryptography for copyright protection of a digital image. A binary image, called watermark, is split into two shares via a 2-out-of-2 visual secret sharing scheme. Then, one of the shares called the master share is extracted from the host image using a fixed pseudo-random points, and the other share also known as ownership share, made by relating the master share and the watermark, is held by the owner which is also given to an authorized 3rd party copyright verifier. Based on the security property of visual cryptography, the two shares on their own cannot leak any information about the watermark. The experimental results show that even after the image was modified, the invisible watermark was successfully extracted from it.
## Theory
Visual Cryptography may be a special encryption technique to cover information in images in such a way that it is decrypted by the human vision if the proper key image is employed. The technique was proposed by Naor and Shamir in 1994. Visual Cryptography uses two transparent images. One image contains random pixels and also the other image contains the key information. it's impossible to retrieve the key information from one in every one of the pictures. Either transparent images or layers are required to reveal the data. the best thanks to implementing Visual Cryptography is to print the 2 layers onto a transparent sheet. <br>
There is a simple algorithm for visual cryptography that creates 2 encrypted images from an original unencrypted image. The algorithm is as follows:
1. Create an image of random pixels the same size and shape as the original image. Random1.
2. Create a second image whose pixels are the exclusiveor (XOR) of the first image and the original image.<br>
       &nbsp;&nbsp;&nbsp; Random2 = Random1 XOR Original.
<br>This image will "look random".
3. The two apparently random images can now be combined with XOR to re-create the original image.<br>
       &nbsp;&nbsp;&nbsp; Random1 XOR Random2 = Original
      
## How to run
There is no special requirements for this project. The flow of the project will be as given below:
1. 'python owernership_share_generator.py' will generate the Ownership share for our image and watermark.
2. 'python master_share_generator.py' will generate all the Master shares for each of the sample stolen and modified images.
3. 'python watermark_generator.py' will extract watermarks using the Ownership share with each of the master shares.
4. 'python template_match_res.py' will give the accuracy of extracted watermark.
