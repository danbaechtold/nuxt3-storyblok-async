# nuxt3-storyblok-async

Demo for [storyblok-nuxt issue #155](https://github.com/storyblok/storyblok-nuxt/issues/155)


## Setup

1. Add your Storyblok Access Token to .env

2. Install the dependencies:

```bash
# pnpm
pnpm install
```


## Run Demo

Generate the application:

```bash
pnpm run generate
```

Locally preview production build:

```bash
pnpm run preview
```

## Example Pages:
With "useAsyncStoryblok", producing the error: 
```
http://localhost:3000/bad
```

With Workaround:
```
http://localhost:3000/good
```
