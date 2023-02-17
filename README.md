# magic-byte-illustration   <br />

 <br />
If you're curious about how [magic bytes work](https://en.wikipedia.org/wiki/List_of_file_signatures), this tutorial can help!  
 <br />

We'll change file signatures and observe how it changes the output of the MacOS [file command](https://ss64.com/osx/file.html). (Limitation: this tutorial is for MacOS users.)
 <br />
 <br />
Steps:
 <br />
 <br />
## 1. `git clone https://github.com/Cerchie/magic-byte-illustration.git && cd magic-byte-illustration`
 <br />
  <br />
## 2. Now view PK.zip in your text editor. It will look something like:
 <br />
 <br />
<img width="800" alt="first few lines are PK����;" src="https://user-images.githubusercontent.com/54046179/219688465-e5dbe27a-45b9-4030-9f92-3b7651a81ac2.png">
 <br />
    <br />
## 3. PK is the file signature for the zip file format. You can verify that by running `file PK.zip`. 
 <br />
  <br />
## 4. Let's change the file signature so that `file` reads this file as a PDF! 
 <br />
   <br />
`git checkout change-signature-to-pdf`
 <br />
  <br />
When you view the file in your text editor, you can see that the signature has changed:
 <br />
  <br />

<img width="526" alt="first few lines read %PDF-���" src="https://user-images.githubusercontent.com/54046179/219690910-caa1158e-8dd8-458a-9646-60f62c8bef01.png">

 <br />
  <br />
## 5. Run `file PK.zip` to confirm. Note that while the _extension_ is still ".zip", the file signature is for a PDF, so it's read as a PDF. Pretty cool huh? 
