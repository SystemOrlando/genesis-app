# Avisos de componentes de terceros

GÉNESIS es software propietario (ver [LICENSE](LICENSE)). Está hecho con componentes de código abierto y recursos de terceros,
cada uno bajo su propia licencia, que se respetan y prevalecen para ese componente (sección 4 de la licencia de GÉNESIS).
Este archivo lo escribe `genesis-desktop/tools/avisos-terceros.py` a partir de las dependencias reales; no lo edites a mano.

Ninguno de estos componentes está bajo una licencia de copyleft fuerte (GPL, AGPL) dentro del programa. Cinco paquetes de Rust
(`cssparser`, `cssparser-macros`, `dtoa-short`, `option-ext`, `selectors`) usan MPL-2.0, una licencia de copyleft por archivo:
se usan sin modificarlos y su código fuente está en crates.io y en sus repositorios. En Linux, GÉNESIS usa WebKitGTK y GTK
(LGPL), instalados en el sistema y enlazados de forma dinámica; no se incluyen en el instalador.

## Programas que GÉNESIS no incluye

GÉNESIS puede instalar o abrir estos programas, que se bajan de sus sitios oficiales bajo sus propias licencias y **no viajan**
dentro del instalador: OpenCode, Claude Code, Codex CLI, Gemini CLI, LocalAI (y los modelos que se elijan, cada uno con la
licencia de su autor), Piper y sus voces, Docker y WSL. Las marcas pertenecen a sus dueños y se nombran solo para decir con
qué funciona GÉNESIS; no hay vínculo ni respaldo de esas empresas.

## Recursos incluidos que no son paquetes

- **Skills de base** (`genesis-desktop/src-tauri/skills-base/`): instrucciones de terceros bajo Apache-2.0 u otras licencias
  de código abierto; cada una conserva su `LICENSE.txt`, y el detalle está en
  [`AVISOS-DE-LICENCIA.md`](genesis-desktop/src-tauri/skills-base/AVISOS-DE-LICENCIA.md).
- **Navegador del agente**: Playwright MCP 0.0.84 y Playwright 1.65.0-alpha-2026-10-30 (Microsoft, Apache-2.0), incluidos
  **sin modificar** dentro del programa ([`genesis-desktop/src-tauri/navegador/`](genesis-desktop/src-tauri/navegador/LEEME.md)).
  Sus `LICENSE`, `NOTICE` y `ThirdPartyNotices.txt` viajan con ellos y se descomprimen en la PC junto al código. Usan el
  navegador que ya hay en el equipo (Microsoft Edge, Google Chrome o Chromium), que no se incluye.
- **Caja del modo código**: QuickJS-ng (MIT; Fabrice Bellard, Charlie Gordon y los colaboradores de QuickJS-ng), compilado
  dentro del programa por el paquete `rquickjs` (MIT, en la lista de Rust de abajo). Corre el código que el agente escribe para
  los conectores, sin red ni acceso a archivos.
- **OCR y traductor local** ([`genesis-desktop/public/motores/`](genesis-desktop/public/motores/LEEME.md)), incluidos **sin
  modificar** con sus licencias en `public/motores/licencias/`: tesseract.js 7.0.0 y tesseract.js-core 7.0.0 (Tesseract en
  WebAssembly, Apache-2.0), los modelos tessdata_fast de inglés, español y portugués (Apache-2.0), pdf.js 6.4.299 (Mozilla,
  Apache-2.0) y bergamot-translator 0.4.9 (el motor de Firefox Translations, MPL-2.0; su código fuente está en
  github.com/browsermt/bergamot-translator). Los modelos de traducción de Mozilla (MPL-2.0) no van en el instalador: la app
  los baja cuando el operador lo pide.
- **Diccionario de inglés** (`public/motores/diccionario/en.txt`): palabras de los niveles 10 a 70 de SCOWL (Copyright
  2000-2016 Kevin Atkinson y otros; licencia permisiva, en `public/motores/licencias/SCOWL-Copyright.txt`). Sirve para
  detectar palabras que el traductor local inventa.
- **Tipografías**: Rethink Sans y Azeret Mono (SIL Open Font License 1.1), por los paquetes `@fontsource-variable/*` de abajo.
- **Iconos y logotipos**: Phosphor y Lobe Icons (MIT), Simple Icons (CC0-1.0) y los logos de los paquetes `@iconify-json/*`.
  Los logotipos de servicios son marcas de sus dueños y aparecen solo para identificar el conector.

## JavaScript (dentro de la interfaz)
MIT: 6, MIT OR Apache-2.0: 4, OFL-1.1: 2, CC0-1.0: 1, Apache-2.0 OR MIT: 1

| Paquete | Versión | Licencia |
|---|---|---|
| @fontsource-variable/azeret-mono | 5.3.0 | OFL-1.1 |
| @fontsource-variable/rethink-sans | 5.3.0 | OFL-1.1 |
| @iconify-json/logos | 1.2.18 | CC0-1.0 |
| @iconify/types | 2.0.0 | MIT |
| @lobehub/icons-static-svg | 1.101.0 | MIT |
| @tauri-apps/api | 2.12.4 | Apache-2.0 OR MIT |
| @tauri-apps/plugin-dialog | 2.8.4 | MIT OR Apache-2.0 |
| @tauri-apps/plugin-fs | 2.7.1 | MIT OR Apache-2.0 |
| @tauri-apps/plugin-global-shortcut | 2.4.1 | MIT OR Apache-2.0 |
| @tauri-apps/plugin-opener | 2.7.2 | MIT OR Apache-2.0 |
| react | 19.3.1 | MIT |
| react-dom | 19.3.1 | MIT |
| scheduler | 0.28.0 | MIT |
| three | 0.170.0 | MIT |

## Rust (dentro del programa, Windows y Linux)
MIT OR Apache-2.0: 210, MIT: 120, Apache-2.0 OR MIT: 52, Unicode-3.0: 18, MIT/Apache-2.0: 10, Unlicense OR MIT: 8, MPL-2.0: 5, MIT OR Apache-2.0 OR Zlib: 4

| Paquete | Versión | Licencia |
|---|---|---|
| adler2 | 2.0.1 | 0BSD OR MIT OR Apache-2.0 |
| adobe-cmap-parser | 0.4.1 | MIT |
| aes | 0.8.4 | MIT OR Apache-2.0 |
| aho-corasick | 1.1.5 | Unlicense OR MIT |
| alloc-no-stdlib | 3.0.0 | BSD-3-Clause |
| alloc-stdlib | 0.3.0 | BSD-3-Clause |
| allocator-api2 | 0.2.21 | MIT OR Apache-2.0 |
| anyhow | 1.0.104 | MIT OR Apache-2.0 |
| async-broadcast | 0.7.2 | MIT OR Apache-2.0 |
| async-channel | 2.5.0 | Apache-2.0 OR MIT |
| async-executor | 1.14.0 | Apache-2.0 OR MIT |
| async-io | 2.6.0 | Apache-2.0 OR MIT |
| async-lock | 3.4.2 | Apache-2.0 OR MIT |
| async-process | 2.5.0 | Apache-2.0 OR MIT |
| async-recursion | 1.2.0 | MIT OR Apache-2.0 |
| async-signal | 0.2.14 | Apache-2.0 OR MIT |
| async-task | 4.7.1 | Apache-2.0 OR MIT |
| async-trait | 0.1.92 | MIT OR Apache-2.0 |
| atk | 0.18.2 | MIT |
| atk-sys | 0.18.2 | MIT |
| atomic-waker | 1.1.2 | Apache-2.0 OR MIT |
| autocfg | 1.5.1 | Apache-2.0 OR MIT |
| base64 | 0.22.1 | MIT OR Apache-2.0 |
| base64 | 0.23.1 | MIT OR Apache-2.0 |
| bit-set | 0.8.0 | Apache-2.0 OR MIT |
| bit-vec | 0.8.0 | Apache-2.0 OR MIT |
| bitflags | 2.13.2 | MIT OR Apache-2.0 |
| bitflags | 1.3.2 | MIT/Apache-2.0 |
| block-buffer | 0.10.4 | MIT OR Apache-2.0 |
| block-padding | 0.3.3 | MIT OR Apache-2.0 |
| blocking | 1.7.0 | Apache-2.0 OR MIT |
| brotli | 9.1.1 | BSD-3-Clause AND MIT |
| brotli-decompressor | 6.2.0 | BSD-3-Clause/MIT |
| bs58 | 0.5.1 | MIT/Apache-2.0 |
| bumpalo | 3.20.3 | MIT OR Apache-2.0 |
| byteorder | 1.5.0 | Unlicense OR MIT |
| bytes | 1.12.1 | MIT |
| cairo-rs | 0.18.5 | MIT |
| cairo-sys-rs | 0.18.2 | MIT |
| camino | 1.2.6 | MIT OR Apache-2.0 |
| cargo-platform | 0.1.9 | MIT OR Apache-2.0 |
| cargo_metadata | 0.19.2 | MIT |
| cargo_toml | 1.0.1 | Apache-2.0 OR MIT |
| cbc | 0.1.2 | MIT OR Apache-2.0 |
| cc | 1.10.0 | MIT OR Apache-2.0 |
| cfb | 0.14.0 | MIT |
| cff-parser | 0.2.0 | MIT OR Apache-2.0 |
| cfg-expr | 0.15.8 | MIT OR Apache-2.0 |
| cfg-if | 1.0.5 | MIT OR Apache-2.0 |
| cfg_aliases | 0.2.2 | MIT |
| chacha20 | 0.10.2 | MIT OR Apache-2.0 |
| chrono | 0.4.45 | MIT OR Apache-2.0 |
| cipher | 0.4.4 | MIT OR Apache-2.0 |
| concurrent-queue | 2.5.0 | Apache-2.0 OR MIT |
| constant_time_eq | 0.6.1 | CC0-1.0 OR MIT-0 OR Apache-2.0 |
| cookie | 0.18.2 | MIT OR Apache-2.0 |
| core_detect | 1.0.0 | MIT/Apache-2.0 |
| cpufeatures | 0.3.1 | MIT OR Apache-2.0 |
| cpufeatures | 0.2.17 | MIT OR Apache-2.0 |
| crc32fast | 1.5.3 | MIT OR Apache-2.0 |
| crossbeam-channel | 0.5.17 | MIT OR Apache-2.0 |
| crossbeam-utils | 0.8.23 | MIT OR Apache-2.0 |
| crypto-common | 0.1.7 | MIT OR Apache-2.0 |
| cssparser | 0.37.0 | MPL-2.0 |
| cssparser-macros | 0.7.1 | MPL-2.0 |
| ctor | 1.0.13 | Apache-2.0 OR MIT |
| darling | 0.24.1 | MIT |
| darling_core | 0.24.1 | MIT |
| darling_macro | 0.24.1 | MIT |
| dbus | 0.9.12 | Apache-2.0/MIT |
| dbus-secret-service | 4.1.0 | MIT OR Apache-2.0 |
| defmt | 1.2.0 | MIT OR Apache-2.0 |
| defmt-macros | 1.2.0 | MIT OR Apache-2.0 |
| defmt-parser | 1.1.0 | MIT OR Apache-2.0 |
| deranged | 0.5.9 | MIT OR Apache-2.0 |
| derive_more | 2.1.1 | MIT |
| derive_more-impl | 2.1.1 | MIT |
| digest | 0.10.7 | MIT OR Apache-2.0 |
| dirs | 7.0.0 | MIT OR Apache-2.0 |
| dirs-sys | 0.5.0 | MIT OR Apache-2.0 |
| displaydoc | 0.2.7 | MIT OR Apache-2.0 |
| dlopen2 | 0.8.2 | MIT |
| dlopen2_derive | 0.4.3 | MIT |
| dom_query | 0.28.0 | MIT |
| dotenvy | 0.15.7 | MIT |
| dpi | 0.1.2 | Apache-2.0 AND MIT |
| dtoa | 1.0.11 | MIT OR Apache-2.0 |
| dtoa-short | 0.3.5 | MPL-2.0 |
| dunce | 1.0.5 | CC0-1.0 OR MIT-0 OR Apache-2.0 |
| dyn-clone | 1.0.20 | MIT OR Apache-2.0 |
| ecb | 0.1.2 | MIT |
| embed-resource | 3.0.12 | MIT |
| encoding_rs | 0.8.44 | (Apache-2.0 OR MIT) AND BSD-3-Clause |
| endi | 1.1.1 | MIT |
| enumflags2 | 0.7.12 | MIT OR Apache-2.0 |
| enumflags2_derive | 0.7.12 | MIT OR Apache-2.0 |
| equivalent | 1.0.3 | Apache-2.0 OR MIT |
| erased-serde | 0.4.11 | MIT OR Apache-2.0 |
| errno | 0.3.14 | MIT OR Apache-2.0 |
| euclid | 0.20.14 | MIT / Apache-2.0 |
| event-listener | 5.4.2 | Apache-2.0 OR MIT |
| event-listener-strategy | 0.5.4 | Apache-2.0 OR MIT |
| fastrand | 2.5.0 | Apache-2.0 OR MIT |
| fdeflate | 0.3.7 | MIT OR Apache-2.0 |
| field-offset | 0.3.6 | MIT OR Apache-2.0 |
| filetime | 0.2.29 | MIT/Apache-2.0 |
| find-msvc-tools | 0.1.15 | MIT OR Apache-2.0 |
| flate2 | 1.1.10 | MIT OR Apache-2.0 |
| fnv | 1.0.7 | Apache-2.0 / MIT |
| foldhash | 0.2.0 | Zlib |
| form_urlencoded | 1.2.2 | MIT OR Apache-2.0 |
| futures-channel | 0.3.34 | MIT OR Apache-2.0 |
| futures-core | 0.3.34 | MIT OR Apache-2.0 |
| futures-executor | 0.3.34 | MIT OR Apache-2.0 |
| futures-io | 0.3.34 | MIT OR Apache-2.0 |
| futures-lite | 2.6.1 | Apache-2.0 OR MIT |
| futures-macro | 0.3.34 | MIT OR Apache-2.0 |
| futures-sink | 0.3.34 | MIT OR Apache-2.0 |
| futures-task | 0.3.34 | MIT OR Apache-2.0 |
| futures-util | 0.3.34 | MIT OR Apache-2.0 |
| gdk | 0.18.2 | MIT |
| gdk-pixbuf | 0.18.5 | MIT |
| gdk-pixbuf-sys | 0.18.0 | MIT |
| gdk-sys | 0.18.2 | MIT |
| gdkwayland-sys | 0.18.2 | MIT |
| gdkx11 | 0.18.2 | MIT |
| gdkx11-sys | 0.18.2 | MIT |
| generic-array | 0.14.7 | MIT |
| gethostname | 1.1.0 | Apache-2.0 |
| getrandom | 0.2.17 | MIT OR Apache-2.0 |
| getrandom | 0.4.3 | MIT OR Apache-2.0 |
| getrandom | 0.3.4 | MIT OR Apache-2.0 |
| gio | 0.18.4 | MIT |
| gio-sys | 0.18.1 | MIT |
| glib | 0.18.5 | MIT |
| glib-macros | 0.18.5 | MIT |
| glib-sys | 0.18.1 | MIT |
| glob | 0.3.4 | MIT OR Apache-2.0 |
| global-hotkey | 0.8.0 | Apache-2.0 OR MIT |
| gobject-sys | 0.18.0 | MIT |
| gtk | 0.18.2 | MIT |
| gtk-sys | 0.18.2 | MIT |
| gtk3-macros | 0.18.2 | MIT |
| h2 | 0.4.20 | MIT |
| hashbrown | 0.17.1 | MIT OR Apache-2.0 |
| hashbrown | 0.12.3 | MIT OR Apache-2.0 |
| heck | 0.5.0 | MIT OR Apache-2.0 |
| heck | 0.4.1 | MIT OR Apache-2.0 |
| hex | 0.4.3 | MIT OR Apache-2.0 |
| html5ever | 0.39.0 | MIT OR Apache-2.0 |
| http | 1.5.0 | MIT OR Apache-2.0 |
| http-body | 1.1.0 | MIT |
| http-body-util | 0.1.5 | MIT |
| httparse | 1.10.1 | MIT OR Apache-2.0 |
| hyper | 1.12.0 | MIT |
| hyper-rustls | 0.27.10 | Apache-2.0 OR ISC OR MIT |
| hyper-util | 0.1.21 | MIT |
| iana-time-zone | 0.1.65 | MIT OR Apache-2.0 |
| ico | 0.6.0 | MIT |
| icu_collections | 2.4.0 | Unicode-3.0 |
| icu_locale_core | 2.4.0 | Unicode-3.0 |
| icu_normalizer | 2.4.0 | Unicode-3.0 |
| icu_normalizer_data | 2.4.0 | Unicode-3.0 |
| icu_properties | 2.4.0 | Unicode-3.0 |
| icu_properties_data | 2.4.0 | Unicode-3.0 |
| icu_provider | 2.4.0 | Unicode-3.0 |
| ident_case | 1.0.1 | MIT/Apache-2.0 |
| idna | 1.1.0 | MIT OR Apache-2.0 |
| idna_adapter | 1.2.2 | Apache-2.0 OR MIT |
| indexmap | 1.9.3 | Apache-2.0 OR MIT |
| indexmap | 2.14.2 | Apache-2.0 OR MIT |
| infer | 0.22.0 | MIT |
| inout | 0.1.4 | MIT OR Apache-2.0 |
| ipnet | 2.12.2 | MIT OR Apache-2.0 |
| is-docker | 0.2.0 | MIT |
| is-wsl | 0.4.0 | MIT |
| itoa | 1.0.18 | MIT OR Apache-2.0 |
| javascriptcore-rs | 1.1.2 | MIT |
| javascriptcore-rs-sys | 1.1.1 | MIT |
| jiff | 0.2.38 | Unlicense OR MIT |
| jiff-core | 0.1.1 | Unlicense OR MIT |
| jiff-tzdb | 0.1.9 | Unlicense OR MIT |
| jiff-tzdb-platform | 0.1.3 | Unlicense OR MIT |
| json-patch | 4.2.0 | MIT/Apache-2.0 |
| jsonptr | 0.7.1 | MIT OR Apache-2.0 |
| keyboard-types | 0.7.0 | MIT OR Apache-2.0 |
| keyboard-types | 0.8.3 | MIT OR Apache-2.0 |
| keyring | 3.6.3 | MIT OR Apache-2.0 |
| libappindicator | 0.9.0 | Apache-2.0 OR MIT |
| libappindicator-sys | 0.9.0 | Apache-2.0 OR MIT |
| libc | 0.2.191 | MIT OR Apache-2.0 |
| libdbus-sys | 0.2.7 | Apache-2.0/MIT |
| libloading | 0.7.4 | ISC |
| linux-raw-sys | 0.12.1 | Apache-2.0 WITH LLVM-exception OR Apache-2.0 OR MIT |
| litemap | 0.8.3 | Unicode-3.0 |
| lock_api | 0.4.14 | MIT OR Apache-2.0 |
| log | 0.4.35 | MIT OR Apache-2.0 |
| lopdf | 0.42.0 | MIT |
| lru-slab | 0.1.3 | MIT OR Apache-2.0 OR Zlib |
| markup5ever | 0.39.0 | MIT OR Apache-2.0 |
| md-5 | 0.10.6 | MIT OR Apache-2.0 |
| memchr | 2.8.3 | Unlicense OR MIT |
| memoffset | 0.9.1 | MIT |
| mime | 0.3.17 | MIT OR Apache-2.0 |
| minisign-verify | 0.3.0 | MIT |
| miniz_oxide | 0.9.1 | MIT OR Zlib OR Apache-2.0 |
| miniz_oxide | 0.8.9 | MIT OR Zlib OR Apache-2.0 |
| mio | 1.2.4 | MIT |
| muda | 0.20.0 | Apache-2.0 OR MIT |
| multiversion_no_op | 1.0.0 | Apache-2.0 OR MIT |
| new_debug_unreachable | 1.0.6 | MIT |
| nom | 8.0.0 | MIT |
| num-conv | 0.2.2 | MIT OR Apache-2.0 |
| num-traits | 0.2.19 | MIT OR Apache-2.0 |
| once_cell | 1.21.4 | MIT OR Apache-2.0 |
| open | 5.4.5 | MIT |
| openssl-probe | 0.2.2 | MIT OR Apache-2.0 |
| option-ext | 0.2.0 | MPL-2.0 |
| ordered-stream | 0.2.0 | MIT OR Apache-2.0 |
| pango | 0.18.3 | MIT |
| pango-sys | 0.18.0 | MIT |
| parking | 2.2.1 | Apache-2.0 OR MIT |
| parking_lot | 0.12.5 | MIT OR Apache-2.0 |
| parking_lot_core | 0.9.12 | MIT OR Apache-2.0 |
| pdf-extract | 0.12.1 | MIT |
| percent-encoding | 2.3.2 | MIT OR Apache-2.0 |
| phf | 0.13.1 | MIT |
| phf_codegen | 0.13.1 | MIT |
| phf_generator | 0.13.1 | MIT |
| phf_macros | 0.13.1 | MIT |
| phf_shared | 0.13.1 | MIT |
| pin-project-lite | 0.2.17 | Apache-2.0 OR MIT |
| piper | 0.2.5 | MIT OR Apache-2.0 |
| pkg-config | 0.3.34 | MIT OR Apache-2.0 |
| plist | 1.10.3 | MIT |
| png | 0.18.1 | MIT OR Apache-2.0 |
| polling | 3.11.0 | Apache-2.0 OR MIT |
| pom | 1.1.0 | MIT |
| postscript | 0.14.1 | Apache-2.0/MIT |
| potential_utf | 0.1.6 | Unicode-3.0 |
| powerfmt | 0.2.1 | MIT OR Apache-2.0 |
| ppv-lite86 | 0.2.21 | MIT OR Apache-2.0 |
| precomputed-hash | 0.1.1 | MIT |
| proc-macro-crate | 2.0.2 | MIT OR Apache-2.0 |
| proc-macro-crate | 3.5.0 | MIT OR Apache-2.0 |
| proc-macro-crate | 1.3.1 | MIT OR Apache-2.0 |
| proc-macro-error | 1.0.4 | MIT OR Apache-2.0 |
| proc-macro-error-attr | 1.0.4 | MIT OR Apache-2.0 |
| proc-macro2 | 1.0.107 | MIT OR Apache-2.0 |
| quick-xml | 0.42.0 | MIT |
| quinn | 0.11.12 | MIT OR Apache-2.0 |
| quinn-proto | 0.11.19 | MIT OR Apache-2.0 |
| quinn-udp | 0.5.16 | MIT OR Apache-2.0 |
| quote | 1.0.47 | MIT OR Apache-2.0 |
| rand | 0.8.8 | MIT OR Apache-2.0 |
| rand | 0.10.3 | MIT OR Apache-2.0 |
| rand_chacha | 0.3.1 | MIT OR Apache-2.0 |
| rand_core | 0.10.1 | MIT OR Apache-2.0 |
| rand_core | 0.6.4 | MIT OR Apache-2.0 |
| rand_pcg | 0.10.2 | MIT OR Apache-2.0 |
| rangemap | 1.8.0 | MIT/Apache-2.0 |
| raw-window-handle | 0.6.2 | MIT OR Apache-2.0 OR Zlib |
| ref-cast | 1.0.27 | MIT OR Apache-2.0 |
| ref-cast-impl | 1.0.27 | MIT OR Apache-2.0 |
| regex | 1.13.1 | MIT OR Apache-2.0 |
| regex-automata | 0.4.18 | MIT OR Apache-2.0 |
| regex-syntax | 0.8.11 | MIT OR Apache-2.0 |
| relative-path | 2.0.3 | MIT OR Apache-2.0 |
| reqwest | 0.13.5 | MIT OR Apache-2.0 |
| reqwest | 0.12.28 | MIT OR Apache-2.0 |
| rfd | 0.17.2 | MIT |
| ring | 0.17.14 | Apache-2.0 AND ISC |
| rquickjs | 0.14.0 | MIT |
| rquickjs-core | 0.14.0 | MIT |
| rquickjs-sys | 0.14.0 | MIT |
| rustc-hash | 2.1.3 | Apache-2.0 OR MIT |
| rustc_version | 0.4.1 | MIT OR Apache-2.0 |
| rustix | 1.1.6 | Apache-2.0 WITH LLVM-exception OR Apache-2.0 OR MIT |
| rustls | 0.23.46 | Apache-2.0 OR ISC OR MIT |
| rustls-native-certs | 0.8.5 | Apache-2.0 OR ISC OR MIT |
| rustls-pki-types | 1.15.1 | MIT OR Apache-2.0 |
| rustls-platform-verifier | 0.7.1 | MIT OR Apache-2.0 |
| rustls-webpki | 0.103.16 | ISC |
| rustversion | 1.0.23 | MIT OR Apache-2.0 |
| ryu | 1.0.23 | Apache-2.0 OR BSL-1.0 |
| same-file | 1.0.6 | Unlicense/MIT |
| schannel | 0.1.30 | MIT |
| schemars | 0.8.22 | MIT |
| schemars | 0.9.0 | MIT |
| schemars | 1.2.3 | MIT |
| schemars_derive | 0.8.22 | MIT |
| scopeguard | 1.2.0 | MIT OR Apache-2.0 |
| selectors | 0.38.0 | MPL-2.0 |
| semver | 1.0.28 | MIT OR Apache-2.0 |
| serde | 1.0.229 | MIT OR Apache-2.0 |
| serde-untagged | 0.1.9 | MIT OR Apache-2.0 |
| serde_core | 1.0.229 | MIT OR Apache-2.0 |
| serde_derive | 1.0.229 | MIT OR Apache-2.0 |
| serde_derive_internals | 0.29.1 | MIT OR Apache-2.0 |
| serde_json | 1.0.154 | MIT OR Apache-2.0 |
| serde_repr | 0.1.21 | MIT OR Apache-2.0 |
| serde_spanned | 1.1.2 | MIT OR Apache-2.0 |
| serde_spanned | 0.6.9 | MIT OR Apache-2.0 |
| serde_urlencoded | 0.7.1 | MIT/Apache-2.0 |
| serde_with | 3.24.0 | MIT OR Apache-2.0 |
| serde_with_macros | 3.24.0 | MIT OR Apache-2.0 |
| serialize-to-javascript | 0.1.2 | MIT OR Apache-2.0 |
| serialize-to-javascript-impl | 0.1.2 | MIT OR Apache-2.0 |
| servo_arc | 0.4.3 | MIT OR Apache-2.0 |
| sha2 | 0.10.9 | MIT OR Apache-2.0 |
| shlex | 2.0.1 | MIT OR Apache-2.0 |
| signal-hook-registry | 1.4.8 | MIT OR Apache-2.0 |
| simd-adler32 | 0.3.10 | MIT |
| simdutf8 | 0.1.5 | MIT OR Apache-2.0 |
| siphasher | 1.0.4 | MIT OR Apache-2.0 |
| slab | 0.4.12 | MIT |
| smallvec | 1.16.4 | MIT OR Apache-2.0 |
| socket2 | 0.6.5 | MIT OR Apache-2.0 |
| softbuffer | 0.4.8 | MIT OR Apache-2.0 |
| soup3 | 0.5.0 | MIT |
| soup3-sys | 0.5.0 | MIT |
| stable_deref_trait | 1.2.1 | MIT OR Apache-2.0 |
| static_vcruntime | 3.0.0 | MIT OR Apache-2.0 OR Zlib |
| string_cache | 0.9.0 | MIT OR Apache-2.0 |
| string_cache_codegen | 0.6.1 | MIT OR Apache-2.0 |
| stringprep | 0.1.5 | MIT/Apache-2.0 |
| strsim | 0.11.1 | MIT |
| subtle | 2.6.1 | BSD-3-Clause |
| syn | 2.0.119 | MIT OR Apache-2.0 |
| syn | 3.0.9 | MIT OR Apache-2.0 |
| syn | 1.0.109 | MIT OR Apache-2.0 |
| sync_wrapper | 1.0.2 | Apache-2.0 |
| synstructure | 0.14.0 | MIT |
| system-deps | 6.2.2 | MIT OR Apache-2.0 |
| tao | 0.37.2 | Apache-2.0 |
| tar | 0.4.46 | MIT OR Apache-2.0 |
| target-lexicon | 0.12.16 | Apache-2.0 WITH LLVM-exception |
| tauri | 2.12.5 | Apache-2.0 OR MIT |
| tauri-build | 2.7.4 | Apache-2.0 OR MIT |
| tauri-codegen | 2.7.4 | Apache-2.0 OR MIT |
| tauri-macros | 2.7.4 | Apache-2.0 OR MIT |
| tauri-plugin | 2.7.2 | Apache-2.0 OR MIT |
| tauri-plugin-dialog | 2.8.4 | Apache-2.0 OR MIT |
| tauri-plugin-fs | 2.7.1 | Apache-2.0 OR MIT |
| tauri-plugin-global-shortcut | 2.4.1 | Apache-2.0 OR MIT |
| tauri-plugin-opener | 2.7.2 | Apache-2.0 OR MIT |
| tauri-plugin-updater | 2.14.1 | Apache-2.0 OR MIT |
| tauri-runtime | 2.12.2 | Apache-2.0 OR MIT |
| tauri-runtime-wry | 2.12.3 | Apache-2.0 OR MIT |
| tauri-utils | 2.10.2 | Apache-2.0 OR MIT |
| tauri-winres | 0.3.7 | MIT |
| tempfile | 3.27.0 | MIT OR Apache-2.0 |
| tendril | 0.5.1 | MIT OR Apache-2.0 |
| thiserror | 2.0.21 | MIT OR Apache-2.0 |
| thiserror | 1.0.69 | MIT OR Apache-2.0 |
| thiserror-impl | 2.0.21 | MIT OR Apache-2.0 |
| thiserror-impl | 1.0.69 | MIT OR Apache-2.0 |
| time | 0.3.55 | MIT OR Apache-2.0 |
| time-core | 0.1.9 | MIT OR Apache-2.0 |
| time-macros | 0.2.32 | MIT OR Apache-2.0 |
| tinystr | 0.8.5 | Unicode-3.0 |
| tinyvec | 1.13.3 | Zlib OR Apache-2.0 OR MIT |
| tokio | 1.54.1 | MIT |
| tokio-rustls | 0.26.6 | MIT OR Apache-2.0 |
| tokio-util | 0.7.20 | MIT |
| toml | 1.1.8+spec-1.1.0 | MIT OR Apache-2.0 |
| toml | 0.8.2 | MIT OR Apache-2.0 |
| toml_datetime | 1.1.2+spec-1.1.0 | MIT OR Apache-2.0 |
| toml_datetime | 0.6.3 | MIT OR Apache-2.0 |
| toml_edit | 0.20.2 | MIT OR Apache-2.0 |
| toml_edit | 0.25.17+spec-1.1.0 | MIT OR Apache-2.0 |
| toml_edit | 0.19.15 | MIT OR Apache-2.0 |
| toml_parser | 1.1.5+spec-1.1.0 | MIT OR Apache-2.0 |
| toml_writer | 1.1.3+spec-1.1.0 | MIT OR Apache-2.0 |
| tower | 0.5.3 | MIT |
| tower-http | 0.6.11 | MIT |
| tower-layer | 0.3.3 | MIT |
| tower-service | 0.3.3 | MIT |
| tracing | 0.1.44 | MIT |
| tracing-attributes | 0.1.31 | MIT |
| tracing-core | 0.1.36 | MIT |
| tray-icon | 0.25.1 | MIT OR Apache-2.0 |
| try-lock | 0.2.5 | MIT |
| ttf-parser | 0.25.1 | MIT OR Apache-2.0 |
| type1-encoding-parser | 0.1.1 | MIT |
| typed-path | 0.13.0 | MIT OR Apache-2.0 |
| typeid | 1.0.3 | MIT OR Apache-2.0 |
| typenum | 1.20.1 | MIT OR Apache-2.0 |
| unicode-bidi | 0.3.18 | MIT OR Apache-2.0 |
| unicode-ident | 1.0.27 | (MIT OR Apache-2.0) AND Unicode-3.0 |
| unicode-normalization | 0.1.26 | (MIT OR Apache-2.0) AND Unicode-3.0 |
| unicode-properties | 0.1.5 | (MIT OR Apache-2.0) AND Unicode-3.0 |
| unicode-segmentation | 1.13.3 | MIT OR Apache-2.0 |
| untrusted | 0.9.0 | ISC |
| url | 2.5.8 | MIT OR Apache-2.0 |
| urlencoding | 2.1.3 | MIT |
| urlpattern | 0.6.0 | MIT |
| utf8_iter | 1.1.0 | Apache-2.0 OR MIT |
| utf_types | 1.0.0 | Apache-2.0 OR MIT |
| uuid | 1.29.0 | Apache-2.0 OR MIT |
| version-compare | 0.2.1 | MIT |
| version_check | 0.9.5 | MIT/Apache-2.0 |
| vswhom | 0.1.0 | MIT |
| vswhom-sys | 0.1.3 | MIT |
| walkdir | 2.5.0 | Unlicense/MIT |
| want | 0.3.2 | MIT |
| web-time | 1.1.0 | MIT OR Apache-2.0 |
| web_atoms | 0.2.6 | MIT OR Apache-2.0 |
| webkit2gtk | 2.0.2 | MIT |
| webkit2gtk-sys | 2.0.2 | MIT |
| webpki-roots | 1.0.11 | CDLA-Permissive-2.0 |
| webview2-com | 0.39.1 | MIT |
| webview2-com-macros | 0.8.1 | MIT |
| webview2-com-sys | 0.39.1 | MIT |
| weezl | 0.1.12 | MIT OR Apache-2.0 |
| winapi-util | 0.1.11 | Unlicense OR MIT |
| window-vibrancy | 0.8.1 | Apache-2.0 OR MIT |
| windows | 0.62.2 | MIT OR Apache-2.0 |
| windows-collections | 0.3.2 | MIT OR Apache-2.0 |
| windows-core | 0.62.2 | MIT OR Apache-2.0 |
| windows-future | 0.3.2 | MIT OR Apache-2.0 |
| windows-implement | 0.60.2 | MIT OR Apache-2.0 |
| windows-interface | 0.59.3 | MIT OR Apache-2.0 |
| windows-link | 0.2.1 | MIT OR Apache-2.0 |
| windows-numerics | 0.3.1 | MIT OR Apache-2.0 |
| windows-registry | 0.6.1 | MIT OR Apache-2.0 |
| windows-result | 0.4.1 | MIT OR Apache-2.0 |
| windows-strings | 0.5.1 | MIT OR Apache-2.0 |
| windows-sys | 0.61.2 | MIT OR Apache-2.0 |
| windows-sys | 0.59.0 | MIT OR Apache-2.0 |
| windows-sys | 0.60.2 | MIT OR Apache-2.0 |
| windows-targets | 0.53.5 | MIT OR Apache-2.0 |
| windows-targets | 0.52.6 | MIT OR Apache-2.0 |
| windows-threading | 0.2.1 | MIT OR Apache-2.0 |
| windows-version | 0.1.7 | MIT OR Apache-2.0 |
| windows_x86_64_msvc | 0.52.6 | MIT OR Apache-2.0 |
| windows_x86_64_msvc | 0.53.1 | MIT OR Apache-2.0 |
| winnow | 1.0.4 | MIT |
| winnow | 0.5.40 | MIT |
| winreg | 0.56.0 | MIT |
| writeable | 0.6.4 | Unicode-3.0 |
| wry | 0.57.1 | Apache-2.0 OR MIT |
| x11 | 2.21.0 | MIT |
| x11-dl | 2.21.0 | MIT |
| x11rb | 0.13.2 | MIT OR Apache-2.0 |
| x11rb-protocol | 0.13.2 | MIT OR Apache-2.0 |
| xattr | 1.7.0 | MIT OR Apache-2.0 |
| xkeysym | 0.2.1 | MIT OR Apache-2.0 OR Zlib |
| yoke | 0.8.4 | Unicode-3.0 |
| yoke-derive | 0.8.4 | Unicode-3.0 |
| zbus | 5.19.0 | MIT |
| zbus_macros | 5.19.0 | MIT |
| zbus_names | 4.3.5 | MIT |
| zcheapstr | 1.2.0 | MIT |
| zerocopy | 0.8.63 | BSD-2-Clause OR Apache-2.0 OR MIT |
| zerofrom | 0.1.8 | Unicode-3.0 |
| zerofrom-derive | 0.1.8 | Unicode-3.0 |
| zeroize | 1.9.1 | Apache-2.0 OR MIT |
| zeroize_derive | 1.5.0 | Apache-2.0 OR MIT |
| zerotrie | 0.2.5 | Unicode-3.0 |
| zerovec | 0.11.9 | Unicode-3.0 |
| zerovec-derive | 0.11.7 | Unicode-3.0 |
| zip | 9.5.0 | MIT |
| zlib-rs | 0.6.8 | Zlib |
| zmij | 1.0.23 | MIT |
| zopfli | 0.8.4 | Apache-2.0 |
| zvariant | 5.15.1 | MIT |
| zvariant_derive | 5.15.1 | MIT |
| zvariant_utils | 4.2.0 | MIT |

---
Si crees que falta un aviso o uno es incorrecto, escribe a contacto@brakescode.com.
