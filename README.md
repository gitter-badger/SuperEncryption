# SuperEncryption
SuperEncryption is lightweight and powerful library for encryption &amp; decryption digital content, support any file type from Movie, Audio to eBook, document etc.

## Key Features
- Support any file type (from movie, audio, ebook, document ...)
- High security with AES Encryption algorithm
- High performance encryption & decryption (tested encrypt & decrypt mp4 file 160 Mb in 5 seconds)
- Lightweight and powerful library built from scratch, so can use both in Server & Mobile client or re-write to other language.
- Optimized memory usage for encryption & decryption
- Encryption file size does not increase compare with original file size (Due to multiple block bytes have been compressed during encrypting)
 
 ## Library Dependency 
 - Requires Java Cryptography Extension enable http://www.oracle.com/technetwork/java/javase/downloads/jce-7-download-432124.html
 
## How to use
 - Just included jar library ```SuperEncryption-1.0.jar``` into your project. Please check in example code at https://github.com/JohnnyLe/SuperEncryption/tree/master/Example, It's very simple to use
 ```java
 public static void main(String[] args) throws IOException {
        // input file path to encrypt
        String pathFileInut="D:\\Project\\SuperEncryption\\Example\\testmp4.mp4";
        // output path for encrypted file
        String outputPath="D:\\Project\\SuperEncryption\\Example";
        
        // input file path to decode
        String pathFilDecode="D:\\Project\\SuperEncryption\\Example\\testmp4.mp4.encrypted";
        // Call encrypt file
        new Encrypter().docEncrypt(pathFileInut, outputPath);
        
        // Call decrypt file
        new Decrypter().docDecrypt(pathFilDecode, outputPath);

    }  
 ```
 
 - Using with command line 
  - Encrypt file (-i: Input file path, -o: output file path), or quick run with BAT file TestEncrypt.bat
```java
java -jar SuperEncryption-1.0.jar -encrypt -i D:\\Project\\SuperEncryption\\Example\\testmp4.mp4 -o D:\\Project\\SuperEncryption\\Example
```

  - Decrypt file (-i: Input file path, -o: output file path), or quick run with BAT file TestDecrypt.bat
```java
java -jar SuperEncryption-1.0.jar -decrypt -i D:\\Project\\SuperEncryption\\Example\\testmp4.mp4.encrypted -o D:\\Project\\SuperEncryption\\Example
```
 - File output format
  - Encrypted file extention: {file-name}.encrypted, for example ```testmp4.mp4.encrypted```

 - Contribute
  - For any question/ bug or feedback please feel free to open issue at https://github.com/JohnnyLe/SuperEncryption/issues 

 - Version Available 
  - Free version available in github just allow encrypt file up to 5 Mb and static encrypt key
  - Full version (please contact): Unlimited encryption file size, auto scale Blok bytes encryption, dynamic public & secret key support, dynamic encrypt layer support.
