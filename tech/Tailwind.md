# Tailwind

## Points
- Tailwind is supposed to solve the CSS in JS problem
  - svelte does it better
- Tailwind is supposed to be less verbose
  - anything slightly complex is managed better by CSS / SCSS
  - RE: multiple `focus:`, `hover:`
- Tailwind provides out of the box good looking sites
  - so did bootstrap, doesn't make it a good tool


## Thoughts
- Tailwind UI idiot proofs UI design
- Tailwind and Svelte solve the same problem, svelte just solves it better


## Examples

### Would you rather write
```css
.selector:focus{
  color: red;
  font-size: 14px;
}
```

### Or write this
```
<div class="focus:color-red;">
```

## TODO
- [ ] write section on CSS in JS
- [ ] write section on verbosity
- [ ] write 
- [ ] read anti-tailwind articles