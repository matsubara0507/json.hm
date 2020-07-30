# json.hm

Implement JSON parser using [Hamler](https://www.hamler-lang.org/)

## Example

use Docker Image on [matsubara0507/docker-hamler](https://github.com/matsubara0507/docker-hamler)

```
$ docker run -it --rm -w /work -v `pwd`:/work matsubara0507/hamler:dev build
Compiling JSON
Compiling Main
$ docker run -it --rm -w /work -v `pwd`:/work matsubara0507/hamler:dev repl
Hamler REPL, version 0.2
Type :? for help

> import JSON as J
> import Data.Either (fromRight)
> J.decode "null"
{'Right',{'Null'}}
> J.decode "123"
{'Right',{'Number',123.0}}
> J.decode "\"abc\""
{'Right',{'String',"abc"}}
> show $ fromRight (J.decode "{\"abc\":[false, true, 1.23]}")
"{\"abc\" : [false, true, 1.23]}"
```
