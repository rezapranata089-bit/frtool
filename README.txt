FR Patch Tool - Paket Termux
==============================

Isi folder ini:
  - frtool.py         -> tool utama (Find & Replace Patch Engine), sudah diperbaiki
                          bug fallback Auto-Anchor dan Fuzzy Block.
  - test_fallback.py  -> skrip opsional untuk mengecek apakah kedua fallback itu
                          masih berfungsi normal setelah Anda mengubah frtool.py.

Cara pakai di Termux:
  1. Install Python (kalau belum ada):
       pkg update && pkg install python

  2. Ekstrak paket ini ke folder pilihan Anda, misalnya:
       unzip frtool_package.zip -d ~/frtool
       cd ~/frtool

  3. Jalankan tool utamanya:
       python frtool.py

  4. (Opsional) Jalankan test untuk mengecek fallback masih normal:
       python test_fallback.py

     test_fallback.py otomatis mencari frtool.py di folder yang sama,
     jadi tidak perlu edit apa pun selama kedua file ini tetap satu folder.

Catatan:
  - Kalau Anda memindahkan frtool.py ke folder lain, pindahkan juga
    test_fallback.py ke folder yang sama, atau edit variabel FRTOOL_PATH
    di bagian atas test_fallback.py.
