# Aurelia

This is a bundled version of the [Aurelia framework components](https://github.com/aurelia).

## installation

```
jspm install github:distros/aurelia
```

## Method 1

Add it as a script tag after system.js.

```markup
<script src="jspm_packages/system.js"></script>
<script src="jspm_packages/github/distros/aurelia/aurelia.js"></script>
<script src="config.js"></script>
<script>
System.import('aurelia-bootstrapper');
</script>

```

## Method 2

Add it as a auto injected bundle.

paste the entire array below into the config.js

```
System.config({
  "transpiler": "babel",
  "babelOptions": {
    "stage": 0,
  },
  "paths": {
    "*": "dist/*.js",
    "github:*": "jspm_packages/github/*.js",
    "npm:*": "jspm_packages/npm/*.js"
  },
  "bundles":{
      "aurelia": {
            ... PASTE HERE ...
      }
  }
});
```

Your app will now use the bundled aurelia components so your app will boot up faster.
The app can still be developed without bundling the application files or dependencies.

## Bundling application files

use this to bundle the application files while excluding the ones already included in the aurelia bundle:

```
jspm bundle */** - aurelia app.bundle.js --inject
```

##

Here is an overview of what is included in this bundle.
This is what should be pasted into the config.js when using it as an injected bundle.

    "aurelia": [
      "npm:core-js@0.9.5/modules/$.fw",
      "npm:core-js@0.9.5/modules/$.dom-create",
      "npm:core-js@0.9.5/modules/$.uid",
      "npm:core-js@0.9.5/modules/$.def",
      "npm:core-js@0.9.5/modules/$.invoke",
      "npm:core-js@0.9.5/modules/$.assert",
      "npm:core-js@0.9.5/modules/$.array-includes",
      "npm:core-js@0.9.5/modules/$.replacer",
      "npm:core-js@0.9.5/modules/$.throws",
      "npm:core-js@0.9.5/modules/$.keyof",
      "npm:core-js@0.9.5/modules/$.enum-keys",
      "npm:core-js@0.9.5/modules/$.assign",
      "npm:core-js@0.9.5/modules/es6.object.is",
      "npm:core-js@0.9.5/modules/$.set-proto",
      "npm:core-js@0.9.5/modules/es6.object.to-string",
      "npm:core-js@0.9.5/modules/es6.object.statics-accept-primitives",
      "npm:core-js@0.9.5/modules/es6.function.name",
      "npm:core-js@0.9.5/modules/es6.function.has-instance",
      "npm:core-js@0.9.5/modules/es6.number.constructor",
      "npm:core-js@0.9.5/modules/es6.number.statics",
      "npm:core-js@0.9.5/modules/es6.math",
      "npm:core-js@0.9.5/modules/es6.string.from-code-point",
      "npm:core-js@0.9.5/modules/es6.string.raw",
      "npm:core-js@0.9.5/modules/$.string-at",
      "npm:core-js@0.9.5/modules/$.iter",
      "npm:core-js@0.9.5/modules/$.iter-define",
      "npm:core-js@0.9.5/modules/es6.string.code-point-at",
      "npm:core-js@0.9.5/modules/es6.string.ends-with",
      "npm:core-js@0.9.5/modules/es6.string.includes",
      "npm:core-js@0.9.5/modules/es6.string.repeat",
      "npm:core-js@0.9.5/modules/es6.string.starts-with",
      "npm:core-js@0.9.5/modules/$.iter-call",
      "npm:core-js@0.9.5/modules/$.iter-detect",
      "npm:core-js@0.9.5/modules/es6.array.of",
      "npm:core-js@0.9.5/modules/$.unscope",
      "npm:core-js@0.9.5/modules/$.species",
      "npm:core-js@0.9.5/modules/es6.array.copy-within",
      "npm:core-js@0.9.5/modules/es6.array.fill",
      "npm:core-js@0.9.5/modules/es6.array.find",
      "npm:core-js@0.9.5/modules/es6.array.find-index",
      "npm:core-js@0.9.5/modules/es6.regexp",
      "npm:core-js@0.9.5/modules/$.for-of",
      "npm:process@0.10.1/browser",
      "npm:core-js@0.9.5/modules/$.collection-strong",
      "npm:core-js@0.9.5/modules/$.collection",
      "npm:core-js@0.9.5/modules/es6.set",
      "npm:core-js@0.9.5/modules/$.collection-weak",
      "npm:core-js@0.9.5/modules/es6.weak-set",
      "npm:core-js@0.9.5/modules/$.own-keys",
      "npm:core-js@0.9.5/modules/es7.array.includes",
      "npm:core-js@0.9.5/modules/es7.string.at",
      "npm:core-js@0.9.5/modules/es7.regexp.escape",
      "npm:core-js@0.9.5/modules/es7.object.get-own-property-descriptors",
      "npm:core-js@0.9.5/modules/es7.object.to-array",
      "npm:core-js@0.9.5/modules/$.collection-to-json",
      "npm:core-js@0.9.5/modules/es7.set.to-json",
      "npm:core-js@0.9.5/modules/js.array.statics",
      "npm:core-js@0.9.5/modules/$.partial",
      "npm:core-js@0.9.5/modules/web.immediate",
      "npm:core-js@0.9.5/modules/web.dom.iterable",
      "npm:core-js@0.9.5/modules/core.dict",
      "npm:core-js@0.9.5/modules/core.iter-helpers",
      "npm:core-js@0.9.5/modules/core.$for",
      "npm:core-js@0.9.5/modules/core.delay",
      "npm:core-js@0.9.5/modules/core.function.part",
      "npm:core-js@0.9.5/modules/core.object",
      "npm:core-js@0.9.5/modules/core.array.turn",
      "npm:core-js@0.9.5/modules/core.number.iterator",
      "npm:core-js@0.9.5/modules/core.number.math",
      "npm:core-js@0.9.5/modules/core.string.escape-html",
      "npm:core-js@0.9.5/modules/core.date",
      "npm:core-js@0.9.5/modules/core.global",
      "npm:core-js@0.9.5/modules/core.log",
      "github:aurelia/metadata@0.5.0/reflect-metadata",
      "github:aurelia/metadata@0.5.0/decorator-applicator",
      "github:aurelia/path@0.6.0/index",
      "github:aurelia/loader@0.6.0/loader",
      "npm:core-js@0.9.5/modules/$",
      "npm:core-js@0.9.5/modules/$.wks",
      "npm:core-js@0.9.5/modules/$.ctx",
      "npm:core-js@0.9.5/modules/es6.symbol",
      "npm:core-js@0.9.5/modules/es6.object.assign",
      "npm:core-js@0.9.5/modules/es6.object.set-prototype-of",
      "npm:core-js@0.9.5/modules/es6.string.iterator",
      "npm:core-js@0.9.5/modules/es6.array.from",
      "npm:core-js@0.9.5/modules/es6.array.iterator",
      "npm:core-js@0.9.5/modules/es6.array.species",
      "npm:process@0.10.1",
      "npm:core-js@0.9.5/modules/es6.map",
      "npm:core-js@0.9.5/modules/es6.weak-map",
      "npm:core-js@0.9.5/modules/es6.reflect",
      "npm:core-js@0.9.5/modules/es7.map.to-json",
      "npm:core-js@0.9.5/modules/web.timers",
      "github:aurelia/metadata@0.5.0/metadata",
      "github:aurelia/metadata@0.5.0/decorators",
      "github:aurelia/path@0.6.0",
      "npm:core-js@0.9.5/modules/$.cof",
      "npm:core-js@0.9.5/modules/$.array-methods",
      "github:jspm/nodelibs-process@0.1.1/index",
      "github:aurelia/loader@0.6.0/template-registry-entry",
      "npm:core-js@0.9.5/modules/es5",
      "github:jspm/nodelibs-process@0.1.1",
      "github:aurelia/loader@0.6.0/index",
      "npm:core-js@0.9.5/modules/$.task",
      "github:aurelia/loader@0.6.0",
      "npm:core-js@0.9.5/modules/es6.promise",
      "npm:core-js@0.9.5/shim",
      "npm:core-js@0.9.5/index",
      "npm:core-js@0.9.5",
      "github:aurelia/metadata@0.5.0/origin",
      "github:aurelia/metadata@0.5.0/index",
      "github:aurelia/metadata@0.5.0",
      "github:aurelia/loader-default@0.7.0/index",
      "github:aurelia/loader-default@0.7.0",
      "github:aurelia/binding@0.6.0/value-converter",
      "github:aurelia/binding@0.6.0/event-manager",
      "github:aurelia/task-queue@0.4.0/index",
      "github:aurelia/binding@0.6.0/environment",
      "github:aurelia/binding@0.6.0/array-change-records",
      "github:aurelia/binding@0.6.0/map-change-records",
      "github:aurelia/binding@0.6.0/map-observation",
      "github:aurelia/binding@0.6.0/dirty-checking",
      "github:aurelia/binding@0.6.0/property-observation",
      "github:aurelia/binding@0.6.0/element-observation",
      "github:aurelia/dependency-injection@0.7.0/metadata",
      "github:aurelia/logging@0.4.0/index",
      "github:aurelia/binding@0.6.0/computed-observation",
      "github:aurelia/binding@0.6.0/binding-modes",
      "github:aurelia/binding@0.6.0/lexer",
      "github:aurelia/binding@0.6.0/path-observer",
      "github:aurelia/binding@0.6.0/composite-observer",
      "github:aurelia/binding@0.6.0/access-keyed-observer",
      "github:aurelia/binding@0.6.0/binding-expression",
      "github:aurelia/binding@0.6.0/listener-expression",
      "github:aurelia/binding@0.6.0/name-expression",
      "github:aurelia/binding@0.6.0/call-expression",
      "github:aurelia/task-queue@0.4.0",
      "github:aurelia/binding@0.6.0/collection-observation",
      "github:aurelia/logging@0.4.0",
      "github:aurelia/binding@0.6.0/ast",
      "github:aurelia/binding@0.6.0/array-observation",
      "github:aurelia/dependency-injection@0.7.0/container",
      "github:aurelia/binding@0.6.0/parser",
      "github:aurelia/dependency-injection@0.7.0/index",
      "github:aurelia/dependency-injection@0.7.0",
      "github:aurelia/binding@0.6.0/observer-locator",
      "github:aurelia/binding@0.6.0/index",
      "github:aurelia/binding@0.6.0",
      "github:aurelia/templating@0.11.0/resource-registry",
      "github:aurelia/templating@0.11.0/view",
      "github:aurelia/templating@0.11.0/content-selector",
      "github:aurelia/templating@0.11.0/animator",
      "github:aurelia/templating@0.11.0/binding-language",
      "github:aurelia/templating@0.11.0/util",
      "github:aurelia/templating@0.11.0/bindable-property",
      "github:aurelia/templating@0.11.0/behavior-instance",
      "github:aurelia/templating@0.11.0/children",
      "github:aurelia/templating@0.11.0/element-config",
      "github:aurelia/templating@0.11.0/composition-engine",
      "github:aurelia/templating@0.11.0/decorators",
      "github:aurelia/templating-binding@0.11.0/syntax-interpreter",
      "github:aurelia/templating@0.11.0/view-slot",
      "github:aurelia/templating@0.11.0/module-analyzer",
      "github:aurelia/templating-binding@0.11.0/binding-language",
      "github:aurelia/templating@0.11.0/view-strategy",
      "github:aurelia/templating@0.11.0/view-factory",
      "github:aurelia/templating@0.11.0/view-compiler",
      "github:aurelia/templating@0.11.0/view-engine",
      "github:aurelia/templating@0.11.0/html-behavior",
      "github:aurelia/templating@0.11.0/index",
      "github:aurelia/templating@0.11.0",
      "github:aurelia/templating-binding@0.11.0/index",
      "github:aurelia/templating-binding@0.11.0",
      "github:aurelia/templating-resources@0.11.0/if",
      "github:aurelia/templating-resources@0.11.0/with",
      "github:aurelia/templating-resources@0.11.0/repeat",
      "github:aurelia/templating-resources@0.11.0/show",
      "github:aurelia/templating-resources@0.11.0/global-behavior",
      "github:aurelia/templating-resources@0.11.0/sanitize-html",
      "github:aurelia/templating-resources@0.11.0/compose",
      "github:aurelia/templating-resources@0.11.0/index",
      "github:aurelia/templating-resources@0.11.0",
      "github:aurelia/route-recognizer@0.4.0/state",
      "github:aurelia/route-recognizer@0.4.0/segments",
      "github:aurelia/router@0.8.0/navigation-commands",
      "github:aurelia/router@0.8.0/navigation-instruction",
      "github:aurelia/router@0.8.0/util",
      "github:aurelia/history@0.4.0/index",
      "github:aurelia/router@0.8.0/pipeline",
      "github:aurelia/router@0.8.0/route-loading",
      "github:aurelia/router@0.8.0/activation",
      "github:aurelia/event-aggregator@0.4.0/index",
      "github:aurelia/templating-router@0.12.0/router-view",
      "github:aurelia/templating-router@0.12.0/route-href",
      "github:aurelia/route-recognizer@0.4.0/index",
      "github:aurelia/router@0.8.0/navigation-plan",
      "github:aurelia/history@0.4.0",
      "github:aurelia/router@0.8.0/pipeline-provider",
      "github:aurelia/event-aggregator@0.4.0",
      "github:aurelia/route-recognizer@0.4.0",
      "github:aurelia/router@0.8.0/navigation-context",
      "github:aurelia/router@0.8.0/app-router",
      "github:aurelia/router@0.8.0/route-filters",
      "github:aurelia/router@0.8.0/router-configuration",
      "github:aurelia/router@0.8.0/router",
      "github:aurelia/templating-router@0.12.0/route-loader",
      "github:aurelia/router@0.8.0/index",
      "github:aurelia/router@0.8.0",
      "github:aurelia/templating-router@0.12.0/index",
      "github:aurelia/templating-router@0.12.0",
      "github:aurelia/history-browser@0.4.0/index",
      "github:aurelia/history-browser@0.4.0",
      "github:aurelia/animator-css@0.2.0/animator",
      "github:aurelia/animator-css@0.2.0/index",
      "github:aurelia/animator-css@0.2.0",
      "github:aurelia/framework@0.11.0/plugins",
      "github:aurelia/framework@0.11.0/aurelia",
      "github:aurelia/framework@0.11.0/index",
      "github:aurelia/framework@0.11.0",
      "github:aurelia/http-client@0.8.0/headers",
      "github:aurelia/http-client@0.8.0/http-response-message",
      "github:aurelia/http-client@0.8.0/transformers",
      "github:aurelia/http-client@0.8.0/jsonp-request-message",
      "github:aurelia/http-client@0.8.0/request-message-processor",
      "github:aurelia/http-client@0.8.0/http-request-message",
      "github:aurelia/http-client@0.8.0/request-builder",
      "github:aurelia/http-client@0.8.0/http-client",
      "github:aurelia/http-client@0.8.0/index",
      "github:aurelia/http-client@0.8.0",
      "github:aurelia/logging-console@0.4.0/index",
      "github:aurelia/logging-console@0.4.0",
      "github:aurelia/bootstrapper@0.12.0/index",
      "github:aurelia/bootstrapper@0.12.0"
    ]
    
