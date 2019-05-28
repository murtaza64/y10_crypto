# Caesar Cipher
## Goal 1

Your objective is to decipher the following text:

    kxqeb pfl dqiyf rlk fli giyesujj yj qefkxui sqjkcu

No, it's not Polish or Czech, it's an English sentence that's been encrypted using a Caesar cipher with key 16.

The Caesar cipher works by representing each character from a to z as a number from 0 to 25. 
Each character in the cipher is replaced with the character obtained by adding the value of the key to its value, wrapping around to the beginning if it gets bigger than 25.

For example, with `key = 3` we get `a → e` and `y → b`. The formula for encryption is `d = (c + k) % 26` where `d` is the index from 0 to 25 of the character after encrypting while `c` is the index of the character to be encrypted.

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

    Ydy tjp zqzm czvm ocz omvbzyt ja Yvmoc Kgvbpzdn Ocz Rdnz? D ocjpbco ijo. Do’n ijo v nojmt ocz Ezyd rjpgy ozgg tjp. Do’n v Ndoc gzbziy. Yvmoc Kgvbpzdn rvn v Yvmf Gjmy ja ocz Ndoc, nj kjrzmapg viy nj rdnz cz xjpgy pnz ocz Ajmxz oj diagpzixz ocz hdydxcgjmdvin oj xmzvoz gdaz… Cz cvy npxc v fijrgzybz ja ocz yvmf ndyz ocvo cz xjpgy zqzi fzzk ocz jizn cz xvmzy vwjpo amjh ytdib. Ocz yvmf ndyz ja ocz Ajmxz dn v kvocrvt oj hvit vwdgdodzn njhz xjindyzm oj wz piivopmvg. Cz wzxvhz nj kjrzmapg… ocz jigt ocdib cz rvn vamvdy ja rvn gjndib cdn kjrzm, rcdxc zqziopvggt, ja xjpmnz, cz ydy. Piajmopivozgt, cz ovpbco cdn vkkmziodxz zqzmtocdib cz fizr, oczi cdn vkkmziodxz fdggzy cdh di cdn ngzzk. Dmjidx. Cz xjpgy nvqz joczmn amjh yzvoc, wpo ijo cdhnzga.

If you run into problems, consider the following:

* How should uppercase letters be handled?
* How should punctuation be handled?

## Goal 3

Write a caesar encyption script, which will be very similar to the decryption script. When you finish, send your friends messages to decrypt!

## Extension

[Frequency analysis](https://learncryptography.com/attack-vectors/frequency-analysis) is a method used to break the Caesar cipher efficiently. It uses the fact that certain letters appear more in the English language to predict the key. [Here](http://www.oxfordmathcenter.com/drupal7/node/353) is data about the frequency of letters
in the English language. Use this information to write a function that takes in a string (ciphertext) and prints out all possible plaintexts in order of highest probability.

Example output:

    Ciphertext: khoor zruog

    Key: 10
    Probability: 12.7%
    Plaintext: axeeh phkew
    
    Key: 21
    Probability: 9.1%
    Plaintext: pmttw ewztl
    
    ...(continue for all possible keys)...
