## Run template

like aliases/makefiles, but way simpler. Keep a file of template scripts to run on the shell and call them by name

rtconfig.toml

```
rocker = "docker run --rm -it osmosisfoundation/rocker /bin/sh"
gcm = [
    "git add .",
    "git commit -m {{message}}
]
```

```sh
rt rocker
rt rocker --config="../rtconfig.toml"
rt gcm "my commit message"
```
