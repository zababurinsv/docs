# markdown

* FS.readFile("/data/file.txt",{ encoding: "utf8" });
* FS.writeFile(​ "file.txt"​ , ​ "some contents"​ );
* FS.createDataFile("/data"​ ,"file.txt","abcdef", true,true);
* FS.rename(​"/data/file.txt"​,"/data/renamed.txt"​);
* FS.unlink("/data/file.txt");

## function

* const fsSave = () => this.FS.syncfs(false, err => console.warn(err));
* const fsLoad = () => this.FS.syncfs(true , err => console.warn(err));