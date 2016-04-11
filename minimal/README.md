# Minimal docker image 

**smallest** docker image possible


### Image creation

```
tar cv --files-from /dev/null | docker import - minimal
```

### Use the image

In Dockerfile add: 

```
FROM minimal
```


