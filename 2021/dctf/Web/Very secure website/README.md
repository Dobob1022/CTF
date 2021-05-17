## Very secure website

##### Score : 200

### Challenge

Some students have built their most secure website ever. Can you spot their mistake?

http://dctf1-chall-very-secure-site.westeurope.azurecontainer.io/

---

### Description

This Challenge is web challenge. 

When you connect to the web, You can see the login form. But this webpage provied the source code.

when you see the source code. there is some hint on there.

```php
<?php
  if (isset($_GET['username']) and isset($_GET['password'])) {
    if (hash("tiger128,4", $_GET['username']) != "51c3f5f5d8a8830bc5d8b7ebcb5717df") {
      echo "Invalid username";
    }
    else if (hash("tiger128,4", $_GET['password']) == "0e132798983807237937411964085731") {
      $flag = fopen("flag.txt", "r") or die("Cannot open file");
      echo fread($flag, filesize("flag.txt"));
      fclose($flag);
    }
    else {
      echo "Try harder";
    }
  }
  else {
    echo "Invalid parameters";
  }
?>
```

There is username form. it's encoded with "tiger128,4"hash. If try to decode, the result will be 

"51c3f5f5d8a8830bc5d8b7ebcb5717df" => "admin"

So, we find the username == admin.

Let's find to get password.

password hash is "0e132798983807237937411964085731"

but when you decode this hash, there is no information about this hash. So we tried to use "Magic Hash"

The magic hash is vulnerability on PHP. You can get more information on this site
https://www.whitehatsec.com/blog/magic-hashes/

So we use magic number/string, hash algo is tiger128,4, The magic number is

"479763000"

to use this magic number, you can bypass the login form.

Then you will get the Flag.

The flag is "dctf{It's_magic._I_ain't_gotta_explain_shit.}"
