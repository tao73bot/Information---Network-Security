openssl enc -aes-128-ecb -e -in bigText.txt -out bigTextECBencrypted.bin -K 101010101010010101abcdeffedcbacc
ghex bigTextECBencrypted.bin &
go to 30th bit
change the HEX value
openssl enc -aes-128-ecb -d -in bigTextECBencrypted.bin -out bigTextECBdecrypted.txt -K 101010101010010101abcdeffedcbacc
check the file

openssl enc -aes-128-cbc -e -in bigText.txt -out bigTextCBCencrypted.bin -K 101010101010010101abcdeffedcbacc -iv 12344321567887659090909012345678
ghex bigTextCBCencrypted.bin &
go to 30th bit
change the HEX value
openssl enc -aes-128-cbc -d -in bigTextCBCencrypted.bin -out bigTextCBCdecrypted.txt -K 101010101010010101abcdeffedcbacc -iv 12344321567887659090909012345678
check the file


openssl enc -aes-128-cfb -e -in bigText.txt -out bigTextCFBencrypted.bin -K 101010101010010101abcdeffedcbacc -iv 12344321567887659090909012345678
ghex bigTextCFBencrypted.bin &
go to 30th bit
change the HEX value
openssl enc -aes-128-cfb -d -in bigTextCFBencrypted.bin -out bigTextCFBdecrypted.txt -K 101010101010010101abcdeffedcbacc -iv 12344321567887659090909012345678
check the file


openssl enc -aes-128-ofb -e -in bigText.txt -out bigTextOFBencrypted.bin -K 101010101010010101abcdeffedcbacc -iv 12344321567887659090909012345678
ghex bigTextOFBencrypted.bin &
go to 30th bit
change the HEX value
openssl enc -aes-128-cfb -d -in bigTextOFBencrypted.bin -out bigTextOFBdecrypted.txt -K 101010101010010101abcdeffedcbacc -iv 12344321567887659090909012345678
check the file
