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


E:\lib_project\test-nuxt-eslint\components\test-eslint.vue
   5:3   error    The template root requires exactly one element  vue/valid-template-root
  10:11  warning  Prop "type" should define at least its type     vue/require-prop-types

E:\lib_project\test-nuxt-eslint\pages\index.vue
  8:7  error  Expected '<component>' elements to have 'v-bind:is' attribute  vue/require-component-is

✖ 3 problems (2 errors, 1 warning)

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
