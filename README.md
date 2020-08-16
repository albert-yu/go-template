# go-template

Template repository for Go project

## Build

Pointing to the root directory, run:

```bash
make
```

The compiled executable can be found in the `build/` directory.
Then, to run it:

```bash
./build/coolapp
```

Here, `coolapp` is the value of the `APPNAME` variable in the Makefile.

## Test

```bash
make test
```

## Deploy

### Build for target platform

You can pass in environment variables to compile for a different platform. For example, on a Linux x86 (AWS typically) box:

```bash
env GOOS=linux GOARCH=386 make
```

### Copy to target

```bash
scp -i path/to/downloaded/ec2/pem path/to/build/serve ec2-user@ec2-54-211-180-247.compute-1.amazonaws.com:/home/ec2-user/targetdirectory
```
