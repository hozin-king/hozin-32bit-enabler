# Hozin 32-bit Enabler

Modul Magisk minimal: menambah `armeabi-v7a`/`armeabi` ke CPU ABI list
supaya **APK 32-bit-only bisa di-install** di HP 64-bit-only (mis. POCO X6 Pro).

## Cara pakai

1. Flash zip via Magisk → Modules → Install from storage
2. Reboot
3. Cek: `getprop ro.product.cpu.abilist` harus berisi `armeabi-v7a`
4. Install APK 32-bit seperti biasa

## Batasan jujur

Ini **hanya membuka kunci instalasi**, bukan translator. Setelah kepasang,
app 32-bit tetap butuh runtime 32-bit untuk jalan — itu urusan
Icebear/ZettaBridge yang masih dalam pengembangan.

## Isi modul

- `system.prop` — `ro.product.cpu.abilist=arm64-v8a,armeabi-v7a,armeabi`
- `module.prop` — metadata modul
- `META-INF/` — installer minimal Magisk
