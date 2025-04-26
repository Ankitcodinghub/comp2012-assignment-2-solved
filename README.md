# comp2012-assignment-2-solved
**TO GET THIS SOLUTION VISIT:** [COMP2012 Assignment 2 Solved](https://www.ankitcodinghub.com/product/comp2012-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;124246&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COMP2012 Assignment 2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
Digital Signature Process

The digram belows explains the digit signature process

In our example, the sender, Alice, creates a digital signature using a private key to encrypt the signature. At the same time, hash data is created and encrypted.

The recipient, Bob, uses the signer’s public key to decrypt the signature to verify that the document’s sender is indeed Alice and the message was not alter after it was signed.

In summary, the processes include:

. Generate keys

. Sign

. Verify

Schnorr Algorithm and Digital Signature Algorithm are two algorithms for the digital signature process. You can find the details for the 3 processes of the 2 algorithms in this PDF file: Digital Signatures protocol. It gives the details of how the keys should be generated, how the signing and verification are done.

Important Signature-related Classes

In this assignment, we implement toy versions of DSA digital signature and Schnorr digital signature.

There are 9 different classes given to you with the skeleton code:

The signed signature of a message is modelled under the Signature class, which has two derived classes: (in signatures.cpp/.h)

Abstract base class Signature

DSASignature

SchnorrSignature

These objects hold the actual signature.

As discussed before, a user needs a secret signing key and a public key in order to be able to sign and verify messages respectively.

Abstract base class SecretKey

DSASecretKey

SchnorrSecretKey

SecretKey class provides the Sign() function necessary to create a signature on a message.

Abstract base class PublicKey

DSAPublicKey

SchnorrPublicKey

PublicKey class provides the Verify() function necessary to verify a signature of a message.

Note that some functions in the abstract base classes should be virtual.

Number Class

In DSA and Schnorr, the public/secret keys and signatures consist of integers of many bits

(1024 or 256). They cannot be represented using common integer types such as int64 (signed integer type with width of exactly 64 bits). GMP Library offers arbitrary precision numbers, but is difficult to install on Windows. Therefore we use int64 to represent all numbers and cut down the bits of public/secret keys and signatures.

We implement all necessary operations and functions of number in the class Number, in number.h/number.cpp. These functions and parameters of p, q, g are static functions/variables. Please check self-study notes in course website on static functions if you are not familiar with its usage.

Number::Add(n1, n2): integer addition. Return a Number that holds the sum of n1 and n2.

Number::Sub(n1, n2): integer subtraction. Return a Number that holds the difference of n1 and n2.

Number::Neg(n): integer negation. Return a Number that holds the negation of n.

Number::Mul(n1, n2): integer multiplication. Be cautious about integer overflow. Return a Number that holds the product of n1 and n2.

Number::Mod(n, p): integer modulo. Returns a Number that holds the integer n mod p. Almost every operation in this assignment is modular operation. Please use this to get correct results and avoid integer overflow. If you don’t know what is integer overflow, please check integer overflow.

Number::MulMod(n1, n2, p): apply modulo operation after multiplication.

Number::Pow(base, exp, mod): Return a Number that holds the integer (base to the power of exp) modular mod. Notice that the exponent should be a non-negative number.

Number::Inv(n, mod): modulo inverse (mod should be a prime number). Return a Number that holds the unique integer n-1 such that n × n-1 = 1 mod mod.

Number::Rand(lower, upper): Return a Number that holds a random value in {lower, lower+1, …, upper-1}. This used to generate keys and create signatures.

Number::NSign(n): If n &gt; 0, return 1. If n=0, return 0. If n &lt; 0, return -1. Use this function to compare two Numbers.

Number::Hash()Return the first 16 bits of SHA256 cryptographic hash function applied on the input. The input can be std::string, or Number, or (Number, std::string). In the last case, Hash(Number, std::string), the input is the concatenation of the bits of Number and the bits of std::string.

In gmp_number.h/gmp_number.cpp, the Number class is implemented based on GMP library, thus providing complete DSA/Schnorr algorithms. You can install GMP yourself and change the codes/filenames to experiment with gmp number, but do not use GMP in your submission.

Users and Admins

You don’t need to read into user.h/user.cpp/admin.h/admin.cpp to complete the assignment. STL is used in class User and Admin, you are not required to write STL operations yourself. Knowing the usage of STL might help you understand the whole program. If might also help you debug. You can check the vector of STL in self-study notes on website. If you want to know more, you can search online for any tutorial or document.

Each User has a name, a pair of DSA public/secret keys and a pair of Schnorr public/secret keys. A User can create a signature for a message and send both the message and the signature to another User by calling SendMessage() function. The Admin delivers the message to the other User. The ReceiveMessage() function of the other User is called to verify the signature.

The Admin holds the public information of all users: username, pointer to User object, DSA/Schnorr public keys. The admin acts as both communication network and Certificate Authority (CA).

End of Description

We use hex (base 16) form of integers. If you don’t know hex integers and want more information, you can check Hexadecimal.

Notice that GenerateKey and Sign functions require random number. If you use Number::Rand function differently, your implementation might generate different keys and signatures. Please make sure that you get the exact same results as the expected output, by using Number::Rand only in Schnorr::Sign and Schnorr GenerateKey, similar to the provided implementation of DSA counterparts.

You should start with the given skeleton code.

We will be grading your code on a Linux machine. Filenames are case sensitive in Linux. You are not allowed to use STL, global variables, static variables, or any additional libraries.

You need to clean up your memory properly.

Remove your cin/cout debug output in your submission.

End of Compile and Debug

Download

Digital Signatures protocol

It gives the details of how the keys should be generated, how the signing and verification are done for the DSA and Schnorr Algorithm.

Skeleton Code for Mac/Linux – v2 or Skeleton Code for Windows – v2 The files and folders in the zipped file are:

Makefile – It is the makefile for compilation.

src – All the source files (.cpp) can be found in this folder. include – All the header files (.h) can be found in this folder.

bin – The executable will be stored in this folder and the object files will be stored in the sub-folder, obj.

End of Download

Memory Leak

End of Memory Leak

Grading

. If your program can be compiled, you will receive 10%. This is testcase 1 (given).

. If you correctly implement Schnorr GenerateKey, you will receive 10%. This is testcase 2 (given).

. If your program can output the destruction messages correctly when there is no message between users, you will receive 10%. There are two test cases, 1 given and 1 hidden, each counting 5%.

. If your program can output the destruction messages correctly without memory leakage when there is no message between users, you will receive 10%. There are two test cases, 1 given and 1 hidden, each counting 5%.

. If you correctly implement SchnorrSecretKey::Sign, you will receive 10%. There are five test cases, 2 given and 3 hidden, each counting 2%.

SchnorrPublicKey::Verify is called on these signatures. If your function can return the correct boolean results without runtime error, you will pass the test case. There are five test cases, 2 given and 3 hidden, each counting 2%.

. If you correctly implement DSAPublicKey::Verify, you will receive 10%. There are five test cases, 2 given and 3 hidden, each counting 2%.

. If your program can output the expected output shown on webpage, you will receive 10%. There are 2 testcases 80 and 81 (given). Testcase 81 checks memory leakage. . If your program can output correct results on hidden test case of multiple messages (similar to the provided case), you will receive 10%. This is testcase 9 (hidden).

. If your program can output correct results on hidden test case of multiple messages without memory leakage, you will receive 10%. This is testcase 10 (hidden).

As a hint, you can simulate the hidden test cases by writing test codes your self. For example, you can write codes to create an arbitrarily wrong signature and see whether your Verify can always return the correct results.

End of Grading

Canvas Submission

Create a single zip file that contains only the signature.h and signature.cpp files with the folder structure and name it pa2.zip.

src/signatures.cpp include/signatures.h

Submit the pa2.zip to ZINC. ZINC usage instructions can be found here.

The filenames have to be exactly the same. It must be a zip file, not rar, not 7z, not tar, not gz, etc. Inside the zip file, the cpp files need to have correct names. If your submissions cannot be uncompressed, they will not be graded.

Make sure your source files can be successfully compiled.If we cannot even compile your source file, your work will not be graded, and you will get zero mark for your PA2. Therefore, you should at least put in dummy implementations to the parts that you cannot finish so that there will be no compilation error.
