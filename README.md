# pug template inheritance in svelte

## problem

cannot use pug template inheritance in svelte, using svelte-preprocess

## test

```bash
git clone https://github.com/benblazak/_svelte_preprocess__pug_template_inheritance.git
cd _svelte_preprocess__pug_template_inheritance
npm install
npm run dev -- --open
```

- try the mixin link
  - this should work
- try the template link
  - this should fail with the error message
    > Declaration of template inheritance ("extends") should be the first thing in the file. There can only be one extends statement per file.

## ideas

i think the reason `extends ...` is not the first thing in the file is because the svelte mixins are prepended here: https://github.com/sveltejs/svelte-preprocess/blob/main/src/transformers/pug.ts#L68
