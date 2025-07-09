# biome-zed-require-config-file

This is a reproduction repository for [this biome-zed issue](https://github.com/biomejs/biome-zed/issues/126).

```sh
bun install
zed .
```

Edit the `index.ts` file, by removing the `type` keyword in the import.
Saving the file will add back the `type` keyword, even though nothing should happen since we don't have a biome.json file, and the settings requires the file to be present.

Setting `source.fixAll.biome` to false fixes it.
