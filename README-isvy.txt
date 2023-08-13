
This is a fork of JS-Beautify, to fix JavaScript --wrap-line-width malfuction (wrap line too soon) for nested arrow
functions, e.g. often used in Cypress tess, plus this README-isvy.txt file.

    JS-Beautify
        https://github.com/beautify-web/js-beautify.git


INSTALLATION

    $ sudo yarn global add https://github.com/Yikes2000/js-beautify.git --prefix /usr/local

    # This step is necessary to build js-beautify/js/lib:
    $ cd /usr/local/share/.config/yarn/global/node_modules/js-beautify ; sudo make js


FUTURE UPDATES

    $ cd /usr/local/share/.config/yarn/global/node_modules/js-beautify ; sudo make js


--

Without building js-beautify/js/lib, this error occurs:

    $ js-beautify --version
    
    node:internal/modules/cjs/loader:1031
      throw err;
      ^
    Error: Cannot find module '../lib/cli'
    Require stack:
    - /usr/local/share/.config/yarn/global/node_modules/js-beautify/js/bin/js-beautify.js
        at Function.Module._resolveFilename (node:internal/modules/cjs/loader:1028:15)
        at Function.Module._load (node:internal/modules/cjs/loader:873:27)
        at Module.require (node:internal/modules/cjs/loader:1100:19)
        at require (node:internal/modules/cjs/helpers:119:18)
        at Object.<anonymous> (/usr/local/share/.config/yarn/global/node_modules/js-beautify/js/bin/js-beautify.js:3:11)
        at Module._compile (node:internal/modules/cjs/loader:1198:14)
        at Object.Module._extensions..js (node:internal/modules/cjs/loader:1252:10)
        at Module.load (node:internal/modules/cjs/loader:1076:32)
        at Function.Module._load (node:internal/modules/cjs/loader:911:12)
        at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:81:12) {
      code: 'MODULE_NOT_FOUND',
      requireStack: [
        '/usr/local/share/.config/yarn/global/node_modules/js-beautify/js/bin/js-beautify.js'
      ]
    }
