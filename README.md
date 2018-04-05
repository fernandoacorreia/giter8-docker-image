# giter8 docker image

[Giter8](https://github.com/n8han/giter8) command-line tool wrapped as a Docker image.


## Usage

```
docker run --rm -v $PWD:/g8out fernandoacorreia/g8 fernandoacorreia/basic-scala-project --name=my-project
```

This will generate a new project based on the [`fernandoacorreia/basic-scala-project`](https://github.com/fernandoacorreia/basic-scala-project) template and place it in `my-project` under the current directory.

Or you can set the project properties interactivelly:

```
docker run --rm -it -v $PWD:/g8out test fernandoacorreia/basic-scala-project.g8
```


## File ownership

The files will be initially owned by the `root` user (UID 0). After creating them, change the ownership to your user.

For instance, on a Linux system with `sudo`:

```
sudo chown -R $USER: *
```
