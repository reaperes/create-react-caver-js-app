# Create react caver js app example

create-react-app 을 통해 react 프로젝트를 생성하면, caver-js 를 import 하는 순간 오류가 발생합니다. 
```
Creating an optimized production build...
Failed to compile.

Module not found: Error: Can't resolve 'util' in 'create-react-caver-js-app-example/node_modules/caver-js/packages/caver-klay/src'
BREAKING CHANGE: webpack < 5 used to include polyfills for node.js core modules by default.
This is no longer the case. Verify if you need this module and configure a polyfill for it.

If you want to include a polyfill, you need to:
        - add a fallback 'resolve.fallback: { "util": require.resolve("util/") }'
        - install 'util'
If you don't want to include a polyfill, you can use an empty module like this:
        resolve.fallback: { "util": false }
```

해당 오류에 대해서는 caver-js repository 에 가면 [해결 가이드](https://github.com/klaytn/caver-js#using-webpack--5)가 있습니다:
하지만, 이를 create-react-app 으로 만든 프로젝트에 쉽게 적용 하기는 어렵습니다.

이 프로젝트는 어떻게 오류를 해결할 수 있는지 해결 가이드를 제공합니다.
