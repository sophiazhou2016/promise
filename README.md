# promise
## Promise.resolve##
  a. Promise.resolve(1)
  b. Promise转化thenable函数
## Promise.reject ##
## Promise.then().then().catch() ##
## Promise.all() -- 所有请求都成功fullfilled或者其中一个呗rejected ##
  ### Promise.all([p1,p2,p3]).then((v1,v2,v3) => {}).catch(() => {}) ###
  1. then函数里面的this指向问题，需要用匿名函数
  1. v1, v2, v3 分别是p1, p2, p3 resolve返回的结果
  1. 出现的bug：then跟catch函数里面的都没有执行，原因是其中一个promise在resolve之前就return了，永远都不会resolve，也不会reject.
    其实通过断点还是可以调试出来的。因为之前没有用过，所以无处下手。环境保持，代码用本地的console去吧。
## Promise.race() ##