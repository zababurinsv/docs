# markdown

* FS.writeFile(​ "file.txt"​ , ​ "some contents"​ );
* FS.createDataFile("/data"​ ,"file.txt","abcdef", true,true);
* FS.rename(​"/data/file.txt"​,"/data/renamed.txt"​);
* FS.readFile("/data/file.txt",{ encoding: "utf8" });
* FS.unlink("/data/file.txt");