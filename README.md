# Rust + WASM workshop #01, Paralelní Polis, 13.02.2019
 
 ## Instalační instrukce
 Před workshopem si nainstalujte následující aplikace a balíčky, abychom se na workshopu mohli věnovat už jen případnému dolaďování a dříve se dostat k tomu zajímavějšímu.
 K popisu a vysvětlení funkcí a souvislostí jednotlivých součástí se dostaneme v rámci workshopu.
  
 ### Rust  
 https://www.rust-lang.org/tools/install  
 Případně instrukce pro Windows:  
 https://github.com/rust-lang/rustup.rs/blob/master/README.md#working-with-rust-on-windows
  
 ### WebAssembly a další
 
 #### wasm-pack
 https://rustwasm.github.io/wasm-pack/installer/
  
 #### cargo-generate
 cargo install cargo-generate  
 (Více: https://github.com/ashleygwilliams/cargo-generate)
 
 #### npm
 https://www.npmjs.com/get-npm
 
 ### wasm-pack šablona
 A nakonec si zkuste stáhnout a pohrát si s šablonou Rust + WASM projektu:  
 cargo generate --git https://github.com/rustwasm/wasm-pack-template
  
 
 ### Další zdroje
 Instalační kroky byly vydestilovány z: https://rustwasm.github.io/book/game-of-life/setup.html, kde naleznete podrobnější instrukce a vysvětlení.

### Error: Unexpected section: 0xc6
Ve `www/package.json` zamknout závislosti na starší verze:

```
  "devDependencies": {
    "hello-wasm-pack": "0.1.0",
    "webpack": "4.16.3",
    "webpack-cli": "3.1.0",
    "webpack-dev-server": "3.1.5",
    "copy-webpack-plugin": "4.5.2"
  }
```

Potom znovu `npm i` a `npm link ...`
