# ossclient
 ossclient is a utility for manipulating contents stored in aliyun oss.

## usage

```ossclient -f cfg.yaml --overwrite SRC_FILE FOO/BAR/DST_FILE_NAME```

The -f cfg flag is mandatory, which stores your account credential. ossclient is not able to upload file without these information. The content of cfg.yaml file is:
```
client_id: lkjsdf234                            # access_id
client_secret: sdfsflsafj323                    #access_secret
oss_bucket: dvtest102-oss1                      #oss bucket name, must already exist
oss_endpoint: oss-cn-shanghai.aliyuncs.com      #oss endpoint

```

ossclient will refuse to upload file if the  if the dst file already exists, unless --overwrite flag is given.
