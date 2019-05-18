# Caesar Cipher
## Goal 1

Your objective is to decipher the following text:

    kxqeb pfl dqiyf rlk fli giyesujj yj qefkxui sqjkcu

No, it's not Polish or Czech, it's an English sentence that's been encrypted using a Caesar cipher with key 16.

The Caesar cipher works by representing each character from a to z as a number from 0 to 25. 
Each character in the cipher is replaced with the character obtained by adding the value of the key to its value, wrapping around to the beginning if it gets bigger than 25.

For example, with `key = 3` we get `a → e` and `y → b`. The formula for encryption is `d = (c + k) % 25` where `d` is the index from 0 to 25 of the character after encrypting while `c` is the index of the character to be encrypted.

The text before ciphering is called plaintext and encrypted text is called ciphertext.

Your objective is to write a python script that can successfully decode the above message. You may use the following starter code:

    def decrypt(ciphertext, key)
        # TODO
        return # TODO

    ciphertext  = input('text to decipher: ')
    key = int(input('key: '))
    print(decrypt(ciphertext, key))

Useful functions:

* `ord` returns the ascii value of the inputted character

  `ord('b') == 98`
* `chr` converts an ascii value to a character

  `chr(100) == 'd'`

Good luck!

## Goal 2

Decrypt the following text which has been encrypted with caesar cipher key 21:

    Yey ukq aran davn pda pnvcayu kb Yvnpd Lhvcqaeo Pda Seoa? E pdkqcdp jkp. Ep’o jkp v opknu pda Faye skqhy pahh ukq. Ep’o v Oepd hacajy. Yvnpd Lhvcqaeo svo v Yvng Hkny kb pda Oepd, ok lksanbqh vjy ok seoa da xkqhy qoa pda Bknxa pk ejbhqajxa pda ieyexdhknevjo pk xnavpa heba… Da dvy oqxd v gjkshayca kb pda yvng oeya pdvp da xkqhy araj gaal pda kjao da xvnay vwkqp bnki yuejc. Pda yvng oeya kb pda Bknxa eo v lvpdsvu pk ivju vwehepeao okia xkjoeyan pk wa qjjvpqnvh. Da waxvia ok lksanbqh… pda kjhu pdejc da svo vbnvey kb svo hkoejc deo lksan, sdexd arajpqvhhu, kb xkqnoa, da yey. Qjbknpqjvpahu, da pvqcdp deo vllnajpexa aranupdejc da gjas, pdaj deo vllnajpexa gehhay dei ej deo ohaal. Enkjex. Da xkqhy ovra kpdano bnki yavpd, wqp jkp deioahb.

If you run into problems, consider the following:

* How should uppercase letters be handled?
* How should punctuation be handled?

## Goal 3

Write a caesar encyption script, which will be very similar to the decryption script. When you finish, send your friends messages to decrypt!