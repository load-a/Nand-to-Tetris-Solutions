# Hack CPU Assembler

## What is this?
This is an assembler for the Hack CPU, as presented in the book **the Elements of Computing Systems: Building a Modern Computer from First Principles** (second edition) by Noam Nisan and Shimon Schocken. It takes a `.asm` file path and assembles a `.hack` binary file from it.

## Why?
My primary motivations are these: first, while you can find other assemblers like this that other people have made, few of them were done in Ruby. Second, Ruby's expressive syntax and my new knowledge of clean coding principles may make this version of the project easier to understand for people that find themselves stuck.

## How to get started
You can simply download the source files from here. The required ones are `main.rb`, `constants.rb`, `assembly_file.rb`. In your terminal, execute `main.rb`: pass in a single file path for your source code and enter the command. The program will assemble your file and write a `.hack` plaintext file based on the path it received as input. 

So `$ main.rb example.asm` will generate `example.hack` in the same file.

You can verify the assembler's accuracy by comparing its output to the a file generated by the official assembler. Included in this folder is a small file for doing just that. You'll have to provide both binaries yourself but once you have them you can enter something like this:

`$ ruby compare.rb test_file.hack verification_file.hack`

It will output "true" if the two files are exactly the same. Be sure to check for any trailing whitespace. If one file ends with a newline and the other doesn't the result will be false.