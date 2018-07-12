# crypto_novel
## Novel ideas for cryptography and error detection

### In "XOR_crypto" we use XOR gate to make a simple yet effective cryptographic technique.
### In "XOR_error_detection" we use XOR gate to extract an XOR_checksum to get a highly accurate(99.99%) XOR_checksum.

 ## XOR_crypto
 ![asdfgt](https://user-images.githubusercontent.com/17335120/42646102-80aba118-861d-11e8-931b-c971b5e905a8.JPG)
 
Plain text = 1001011  
We will XOR consecutive elements of first row(1001011) to get second row(101110)  
Then we will XOR consecutive elements of second row(101110) to get element of third row(11001).  
We will follow this procedure until we get single element in a row. 
let's call this a "Converging XOR tree"

![crypto1](https://user-images.githubusercontent.com/17335120/42646788-908eb88e-861f-11e8-8072-65ea51767747.JPG)
Image 2  

Green line(1001011) is plain text and Blue line(1110100) is cipherText  
Now we will do the reverse procedure to get back our plain text.  
We will take Blue line(1110100) as input as shown below  

![crypto2](https://user-images.githubusercontent.com/17335120/42646882-cf0551ea-861f-11e8-8c70-c76240997b76.JPG)

And get out our Green(1001011) plain text by following the same procedure.
By playing with the output of Image 2 we can make algorithm more complex, But for now stick with the simpler version  

For coding implimentation see XOR_crypto_code file.  

## XOR_error_detection

This Novel idea can be a replacement to checksum algorithm

![err1](https://user-images.githubusercontent.com/17335120/42649299-f44f267c-8626-11e8-8d6b-9e45e923c8e7.JPG)

By doing the same consecutive XOR we get our tree.  
Here Blue line(1001011) is message whose "step XOR" is to be calculated  
Lets assume orange line(111) is our "step XOR".

### Accuracy
Let's assume our message lenght to be n bit 
We will make our "Converging XOR tree" and choose m<sup>th</sup> row from bottom to be our "step XOR". so,  
The accuracy will of our algotithm will be  
## 1 - 1/2<sup>m</sup> %  
i.e If 16<sup>th</sup> row from bottom is our "step XOR", then our algorithm's accuracy will be  
1 - 1/2<sup>16</sup> = <b>99.998%</b>

