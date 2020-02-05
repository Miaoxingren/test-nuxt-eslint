# test-nuxt-eslint

Test repo for eslint issue.

## Replication instructions

1. npm i
2. npm run lint

### Current outcome:

```
$ npm run lint

> test-nuxt-eslint@1.0.0 lint E:\lib_project\test-nuxt-eslint
> eslint --ext .js,.vue --ignore-path .gitignore .


TypeError: Cannot read property 'range' of null
Occurred while linting e:\lib_project\test-nuxt-eslint\pages\index.vue:35
    at SourceCode.getTokenBefore (e:\lib_project\test-nuxt-eslint\node_modules\eslint\lib\source-code\token-store\index.js:298:18)
    at checkSpacingBefore (e:\lib_project\test-nuxt-eslint\node_modules\eslint\lib\rules\template-curly-spacing.js:60:42)
    at TemplateElement (e:\lib_project\test-nuxt-eslint\node_modules\eslint\lib\rules\template-curly-spacing.js:119:17)
    at listeners.(anonymous function).forEach.listener (e:\lib_project\test-nuxt-eslint\node_modules\eslint\lib\linter\safe-emitter.js:45:58)
    at Array.forEach (<anonymous>)
    at Object.emit (e:\lib_project\test-nuxt-eslint\node_modules\eslint\lib\linter\safe-emitter.js:45:38)
    at NodeEventGenerator.applySelector (e:\lib_project\test-nuxt-eslint\node_modules\eslint\lib\linter\node-event-generator.js:254:26)
    at NodeEventGenerator.applySelectors (e:\lib_project\test-nuxt-eslint\node_modules\eslint\lib\linter\node-event-generator.js:283:22)
    at NodeEventGenerator.enterNode (e:\lib_project\test-nuxt-eslint\node_modules\eslint\lib\linter\node-event-generator.js:297:14)
    at CodePathAnalyzer.enterNode (e:\lib_project\test-nuxt-eslint\node_modules\eslint\lib\linter\code-path-analysis\code-path-analyzer.js:634:23)s

```

### Expect outcome:

No errors.

## Temporary solution

1. npm i eslint-plugin-nuxt@0.4.3 -D
2. npm run lint

### Current outcome:

No errors.

```
$ npm run lint

> test-nuxt-eslint@1.0.0 lint E:\lib_project\test-nuxt-eslint
> eslint --ext .js,.vue --ignore-path .gitignore .

```
