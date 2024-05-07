ECB = 	PADDING YES
CBC =   PADDING YES
CFB =   PADDING NO
OFB =   PADDING NO

main text bit = 20

openssl enc -aes-128-ecb -e -in text.txt -out textECBencrypted.bin -K 101010101010010101abcdeffedcbacc
ghex textECBencrypted.bin &
cnceypt bit  = 32
openssl enc -aes-128-ecb -d -in textECBencrypted.bin -out textECBdecrypted.txt -K 101010101010010101abcdeffedcbacc
this one is larger after endryption meaning it has padding

openssl enc -aes-128-cbc -e -in text.txt -out textCBCencrypted.bin -K 101010101010010101abcdeffedcbacc -iv 12344321567887659090909012345678
ghex textCBCencrypted.bin &
encrpt bit = 32
openssl enc -aes-128-cbc -d -in textCBCencrypted.bin -out textCBCdecrypted.txt -K 101010101010010101abcdeffedcbacc -iv 12344321567887659090909012345678
this one is larger after endryption meaning it has padding

openssl enc -aria-128-cfb8 -e -in text.txt -out textCFBencrypted.bin -K 101010101010010101abcdeffedcbacc -iv 12344321567887659090909012345678
ghex textCFBencrypted.bin &
encrypt bit = 20
openssl enc -aria-128-cfb8 -d -in textCFBencrypted.bin -out textCFBdecrypted.txt -K 101010101010010101abcdeffedcbacc -iv 12344321567887659090909012345678
this one is same sized after endryption meaning it do not have padding (stream)

openssl enc -aria-128-ofb -e -in text.txt -out textOFBencrypted.bin -K 101010101010010101abcdeffedcbacc -iv 12344321567887659090909012345678
ghex textOFBencrypted.bin &
openssl enc -aria-128-ofb -d -in textOFBencrypted.bin -out textOFBdecrypted.txt -K 101010101010010101abcdeffedcbacc -iv 12344321567887659090909012345678
this one is same sized after endryption meaning it do not have padding (stream)
