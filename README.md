# Messing with Svelte


## Notes

https://github.com/sveltejs/prettier-plugin-svelte
https://github.com/tailwindlabs/prettier-plugin-tailwindcss#compatibility-with-other-prettier-plugins



```
// .prettierrc
{
    // ..
    "plugins": ["prettier-plugin-svelte"],
    "pluginSearchDirs": ["."], // should be removed in v3
    "overrides": [{ "files": "*.svelte", "options": { "parser": "svelte" } }]
}
```