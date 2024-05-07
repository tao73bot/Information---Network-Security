openssl enc -aes-128-ecb -e -in sample.bmp -out encryptedImage.bmp -K 101010101010010101abcdeffedcbacc
ghex sample.bmp &
goto byte 54
copy
ghex encryptedImage.bmp &
find and replace
see image in viewer
openssl enc -aes-128-ecb -d -in encryptedImage.bmp -out decryptedImage.bmp -K 101010101010010101abcdeffedcbacc
ghex decryptedImage.bmp
find and replace
see image.

openssl enc -aes-128-cbc -e -in sample.bmp -out encryptedImageCBC.bmp -K 101010101010010101abcdeffedcbacc -iv 12344321567887659090909012345678
ghex sample.bmp &
goto byte 54
copy
ghex encryptedImageCBC.bmp &
find and replace
see image in viewer
openssl enc -aes-128-cbc -d -in encryptedImageCBC.bmp -out decryptedImageCBC.bmp -K 101010101010010101abcdeffedcbacc -iv 12344321567887659090909012345678
ghex decryptedImageCBC.bmp &
find and replace
see image.
