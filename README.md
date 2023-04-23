# WatcheEffect

It is common for the watcher callback to use exactly the same reactive state as the source.

Composition API is used for the above.

## Example

In the code I have took an example of watchEffect being applied on the input field.

The \<input\> is 2-way binded using v-model and the watchEffect keeps a watch on the input field whether it is empty or not and based on that, the text is displayed below. 

## Project setup

```
npm install
```

## Compiles and hot-reloads for development

```
npm run serve
```
