# 03 Authentication
Sometimes we want to secure our application, but not every application has
authentication mangement included or your just want a simple way to secure an application
behind with a simple username and password.

## How To
Try to open the dashboard via http://localhost/dashboard/
You have to enter the credentials `admin` and `admin123456`

The username and password in the docker-compose file 
are in the format username:bcrypt(password)
You have to hash your password and enter the hash.

### Generate a password hash
To quickly hash a password, you can go to [cyberchef](https://cyberchef.org/#recipe=Bcrypt(10)Find_/_Replace(%7B'option':'Simple%20string','string':'$'%7D,'$$$$',true,false,false,false)&input=YWRtaW4xMjM0NTY),
the input is your password and the output the hashed version.

You can only use the local tool htpasswd and use 

```shell
echo $(htpasswd -nB admin) | sed -e s/\\$/\\$\\$/g
```

> [!IMPORTANT]
> Because the way docker resolves text, every `$` needs to be escaped
> with another dollar sign.
> These two examples already double the dollar signs but in the end, 
> the password must look something like `$$2a$$10$$.....`

> [!TIP]
> Note that because of a process called salting 
> the same input can lead to different hashed password.


## Tasks
* Change to username to `potato`
* Change the password to `123456`
* Copy the whoami service from example 02 and add the same authentication middleware to it
* Be ashamed that you really used `123456` as a password. Use a secure password from your password manager