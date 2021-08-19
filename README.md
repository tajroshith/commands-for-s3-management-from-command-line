## Configure AWS-CLI

```sh
#aws configure
AWS Access Key ID : Provide Access Key
AWS Secret Access Key : Provide Secret Access Key
Default region name : Provide Region
Default output format : json
```

## To list

```sh
#aws s3 ls
2021-08-17 14:35:55 taj-a1.awsdemo.com
2021-08-17 14:26:59 taj-a2.awsdemo.com
2021-08-10 22:27:55 wordpress-web-el
```

## To make a bucket
```sh
#aws s3 mb s3://taj-a3.awsdemo.com
make_bucket: taj-a3.awsdemo.com
```

## To remove/delete a bucket
```sh
#aws s3 rb s3://taj-a2.awsdemo.com
remove_bucket: taj-a2.awsdemo.com
```

## To list contents of a bucket
```sh
#aws s3 ls s3://taj-a3.awsdemo.com
2021-08-17 14:41:19    4017575 cenerade.png

```
## To copy a local file into bucket 
```sh
#aws s3 cp tokyo.png s3://taj-a3.awsdemo.com
upload: .\tokyo.png to s3://taj-a3.awsdemo.com/tokyo.png

```
## To copy multiple files in a local folder to the bucket
```sh
#aws s3 cp Videos s3://taj-a3.awsdemo.com/ --recursive
upload: Videos\desktop.ini to s3://taj-a3.awsdemo.com/desktop.ini
upload: Videos\Captures\desktop.ini to s3://taj-a3.awsdemo.com/Captures/desktop.ini

```

## To sync multiple buckets
```sh
#aws s3 sync s3://taj-a3.awsdemo.com s3://taj-a1.awsdemo.com
copy: s3://taj-a3.awsdemo.com/tokyo.png to s3://taj-a1.awsdemo.com/tokyo.png
copy: s3://taj-a3.awsdemo.com/Captures/desktop.ini to s3://taj-a1.awsdemo.com/Captures/desktop.ini
copy: s3://taj-a3.awsdemo.com/desktop.ini to s3://taj-a1.awsdemo.com/desktop.ini
copy: s3://taj-a3.awsdemo.com/cenerade.png to s3://taj-a1.awsdemo.com/cenerade.png

```
## To remove/delete an object in a bucket

```sh
#aws s3 rm s3://taj-a1.awsdemo.com/tokyo.png
delete: s3://taj-a1.awsdemo.com/tokyo.png

```

## To remove/delete all contents in non-empty bucket

```sh

#aws s3 rm s3://taj-a1.awsdemo.com --recursive
delete: s3://taj-a1.awsdemo.com/flowers.jpg
delete: s3://taj-a1.awsdemo.com/goal.jpg
delete: s3://taj-a1.awsdemo.com/orbit.png
delete: s3://taj-a1.awsdemo.com/mysterious.jpg
delete: s3://taj-a1.awsdemo.com/pixar.png

```
