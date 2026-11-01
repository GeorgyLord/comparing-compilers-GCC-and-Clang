# Задание №2 по PTP

## Текст программы hello.c
```C
/*
Simple program on C
*/

#include <stdio.h>

#define GREETING "Hello, world!"

int main(void)
{
    puts(GREETING);
    return 0;
}
```
## 1 Компилятор gcc

### 1.1 Версия компилятора
```bash
gcc (Ubuntu 15.2.0-16ubuntu1) 15.2.0
Copyright (C) 2025 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
```

### 1.2 Команда для получения исполняемого файла
```bash
gcc -std=c99 -Wall -Werror -v -save-temps hello.c
```

**-v** - подробный вывод информации о процессе компиляции

**-save-temps** - сохраняет все промежуточные (временные) файлы, которые создаются в процессе сборки программы

#### Вывод компиляции
```bash
Using built-in specs.
COLLECT_GCC=gcc
COLLECT_LTO_WRAPPER=/usr/libexec/gcc/x86_64-linux-gnu/15/lto-wrapper
OFFLOAD_TARGET_NAMES=nvptx-none:amdgcn-amdhsa
OFFLOAD_TARGET_DEFAULT=1
Target: x86_64-linux-gnu
Configured with: ../src/configure -v --with-pkgversion='Ubuntu 15.2.0-16ubuntu1' --with-bugurl=file:///usr/share/doc/gcc-15/README.Bugs --enable-languages=c,ada,c++,go,d,fortran,objc,obj-c++,m2,rust,cobol,algol68 --prefix=/usr --with-gcc-major-version-only --program-suffix=-15 --program-prefix=x86_64-linux-gnu- --enable-shared --enable-linker-build-id --libexecdir=/usr/libexec --without-included-gettext --enable-threads=posix --libdir=/usr/lib --enable-nls --enable-bootstrap --enable-clocale=gnu --enable-libstdcxx-debug --enable-libstdcxx-time=yes --with-default-libstdcxx-abi=new --enable-libstdcxx-backtrace --enable-gnu-unique-object --disable-vtable-verify --enable-plugin --enable-default-pie --with-system-zlib --enable-libphobos-checking=release --with-target-system-zlib=auto --enable-objc-gc=auto --enable-multiarch --disable-werror --enable-cet --with-arch-32=i686 --with-abi=m64 --with-multilib-list=m32,m64,mx32 --enable-multilib --with-tune=generic --enable-offload-targets=nvptx-none=/build/gcc-15-j35TAX/gcc-15-15.2.0/debian/tmp-nvptx/usr,amdgcn-amdhsa=/build/gcc-15-j35TAX/gcc-15-15.2.0/debian/tmp-gcn/usr --enable-offload-defaulted --without-cuda-driver --enable-checking=release --build=x86_64-linux-gnu --host=x86_64-linux-gnu --target=x86_64-linux-gnu --with-build-config=bootstrap-lto-lean --enable-link-serialization=2
Thread model: posix
Supported LTO compression algorithms: zlib zstd
gcc version 15.2.0 (Ubuntu 15.2.0-16ubuntu1) 
COLLECT_GCC_OPTIONS='-std=c99' '-Wall' '-Werror' '-v' '-save-temps' '-mtune=generic' '-march=x86-64' '-dumpdir' 'a-'
 /usr/libexec/gcc/x86_64-linux-gnu/15/cc1 -E -quiet -v -imultiarch x86_64-linux-gnu hello.c -mtune=generic -march=x86-64 -std=c99 -Wall -Werror -fpch-preprocess -fasynchronous-unwind-tables -fstack-protector-strong -Wformat-security -fstack-clash-protection -fcf-protection -fzero-init-padding-bits=all -Wbidi-chars=any -o a-hello.i
ignoring nonexistent directory "/usr/local/include/x86_64-linux-gnu"
ignoring nonexistent directory "/usr/lib/gcc/x86_64-linux-gnu/15/include-fixed/x86_64-linux-gnu"
ignoring nonexistent directory "/usr/lib/gcc/x86_64-linux-gnu/15/include-fixed"
ignoring nonexistent directory "/usr/lib/gcc/x86_64-linux-gnu/15/../../../../x86_64-linux-gnu/include"
#include "..." search starts here:
#include <...> search starts here:
 /usr/lib/gcc/x86_64-linux-gnu/15/include
 /usr/local/include
 /usr/include/x86_64-linux-gnu
 /usr/include
End of search list.
COLLECT_GCC_OPTIONS='-std=c99' '-Wall' '-Werror' '-v' '-save-temps' '-mtune=generic' '-march=x86-64' '-dumpdir' 'a-'
 /usr/libexec/gcc/x86_64-linux-gnu/15/cc1 -fpreprocessed a-hello.i -quiet -dumpdir a- -dumpbase hello.c -dumpbase-ext .c -mtune=generic -march=x86-64 -Wall -Werror -std=c99 -version -fasynchronous-unwind-tables -fstack-protector-strong -Wformat-security -fstack-clash-protection -fcf-protection -fzero-init-padding-bits=all -Wbidi-chars=any -o a-hello.s
GNU C99 (Ubuntu 15.2.0-16ubuntu1) version 15.2.0 (x86_64-linux-gnu)
	compiled by GNU C version 15.2.0, GMP version 6.3.0, MPFR version 4.2.2, MPC version 1.3.1, isl version isl-0.27-GMP

GGC heuristics: --param ggc-min-expand=100 --param ggc-min-heapsize=131072
Compiler executable checksum: edd70396dcc669433a92073f97309866
COLLECT_GCC_OPTIONS='-std=c99' '-Wall' '-Werror' '-v' '-save-temps' '-mtune=generic' '-march=x86-64' '-dumpdir' 'a-'
 /usr/bin/x86_64-linux-gnu-as -v --64 -o a-hello.o a-hello.s
GNU assembler version 2.46 (x86_64-linux-gnu) using BFD version (GNU Binutils for Ubuntu) 2.46
COMPILER_PATH=/usr/libexec/gcc/x86_64-linux-gnu/15/:/usr/libexec/gcc/x86_64-linux-gnu/15/:/usr/libexec/gcc/x86_64-linux-gnu/:/usr/lib/gcc/x86_64-linux-gnu/15/:/usr/lib/gcc/x86_64-linux-gnu/
LIBRARY_PATH=/usr/lib/gcc/x86_64-linux-gnu/15/:/usr/lib/gcc/x86_64-linux-gnu/15/../../../x86_64-linux-gnu/:/usr/lib/gcc/x86_64-linux-gnu/15/../../../../lib/:/lib/x86_64-linux-gnu/:/lib/../lib/:/usr/lib/x86_64-linux-gnu/:/usr/lib/../lib/:/usr/lib/gcc/x86_64-linux-gnu/15/../../../:/lib/:/usr/lib/
COLLECT_GCC_OPTIONS='-std=c99' '-Wall' '-Werror' '-v' '-save-temps' '-mtune=generic' '-march=x86-64' '-dumpdir' 'a.'
 /usr/libexec/gcc/x86_64-linux-gnu/15/collect2 -plugin /usr/libexec/gcc/x86_64-linux-gnu/15/liblto_plugin.so -plugin-opt=/usr/libexec/gcc/x86_64-linux-gnu/15/lto-wrapper -plugin-opt=-fresolution=a.res -plugin-opt=-pass-through=-lgcc -plugin-opt=-pass-through=-lgcc_s -plugin-opt=-pass-through=-lc -plugin-opt=-pass-through=-lgcc -plugin-opt=-pass-through=-lgcc_s --build-id --eh-frame-hdr -m elf_x86_64 --hash-style=gnu --as-needed -dynamic-linker /lib64/ld-linux-x86-64.so.2 -pie -z now -z relro /usr/lib/gcc/x86_64-linux-gnu/15/../../../x86_64-linux-gnu/Scrt1.o /usr/lib/gcc/x86_64-linux-gnu/15/../../../x86_64-linux-gnu/crti.o /usr/lib/gcc/x86_64-linux-gnu/15/crtbeginS.o -L/usr/lib/gcc/x86_64-linux-gnu/15 -L/usr/lib/gcc/x86_64-linux-gnu/15/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/15/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/15/../../.. -L/lib -L/usr/lib a-hello.o -lgcc --push-state --as-needed -lgcc_s --pop-state -lc -lgcc --push-state --as-needed -lgcc_s --pop-state /usr/lib/gcc/x86_64-linux-gnu/15/crtendS.o /usr/lib/gcc/x86_64-linux-gnu/15/../../../x86_64-linux-gnu/crtn.o
COLLECT_GCC_OPTIONS='-std=c99' '-Wall' '-Werror' '-v' '-save-temps' '-mtune=generic' '-march=x86-64' '-dumpdir' 'a.'
```

### 1.3 Список файлов, полученных в результате компиляции
| Имя | Размер (байт) | Тип |
| :-: | :-: | :-: |
| hello.c | 129 | Текстовый |
| a-hello.i | 15184 | Текстовый |
| a-hello.s | 661 | Текстовый |
| a-hello.o | 1496 | Объектный |
| a.out | 15952 | Исполняемый |

### 1.4 Препроцессирование

| Команда для выполнения этапа | `/usr/libexec/gcc/x86_64-linux-gnu/15/cc1 -E -quiet -v -imultiarch x86_64-linux-gnu hello.c -mtune=generic -march=x86-64 -std=c99 -Wall -Werror -fpch-preprocess -fasynchronous-unwind-tables -fstack-protector-strong -Wformat-security -fstack-clash-protection -fcf-protection -fzero-init-padding-bits=all -Wbidi-chars=any -o a-hello.i` |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| Вход                       | hello.c                                                                                                                                                       |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Выход                      | a-hello.i                                                                                                                                                     |
| Назначение                 | удаляет комментарии, вставляет файлы (директива include), заменяет текст (раскрытие макросов, директива define), выполняет условную компиляцию (директива if) |
| Имя утилиты                | `/usr/libexec/gcc/x86_64-linux-gnu/15/cc1` (Внутренний компонент GCC, запущенный в режиме препроцессора)                                                      |
| Способ передачи параметров | Входной файл передан прямым аргументом; имя выходного файла передано через явный ключ `-o`; режим работы препроцессора активирован ключом `-E`.               |


### 1.5 Трансляция на язык ассемблера

| Команда для выполнения этапа | `/usr/libexec/gcc/x86_64-linux-gnu/15/cc1 -fpreprocessed a-hello.i -quiet -dumpdir a- -dumpbase hello.c -dumpbase-ext .c -mtune=generic -march=x86-64 -Wall -Werror -std=c99 -version -fasynchronous-unwind-tables -fstack-protector-strong -Wformat-security -fstack-clash-protection -fcf-protection -fzero-init-padding-bits=all -Wbidi-chars=any -o a-hello.s` |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |

| Вход                       | a-hello.i                                                                                                                                                            |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Выход                      | a-hello.s                                                                                                                                                            |
| Назначение                 | Трансляция предобработанного кода на языке Си в текстовый код на языке ассемблера                                                                                    |
| Имя утилиты                | `/usr/libexec/gcc/x86_64-linux-gnu/15/cc1 (Внутренний компилятор GCC)`                                                                                               |
| Способ передачи параметров | Признак уже обработанного кода задан через ключ `-fpreprocessed`; входной файл передан аргументом; имя результирующего ассемблерного файла передано через ключ `-o`. |

### 1.6 Трансляция программы с языка ассемблера в машинный код
| | |
| --- | --- |
| Команда для выполнения этапа | `/usr/bin/x86_64-linux-gnu-as -v --64 -o a-hello.o a-hello.s` |

| Вход                       | a-hello.s                                                                                                                                          |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| Выход                      | a-hello.o                                                                                                                                          |
| Назначение                 | Ассемблирование (перевод) текста на языке ассемблера в объектный файл, содержащий машинный код                                                     |
| Имя утилиты                | `/usr/bin/x86_64-linux-gnu-as` (GNU Assembler)                                                                                                     |
| Способ передачи параметров | Входной ассемблерный файл передан аргументом; разрядность целевой архитектуры задана ключом `--64`; имя объектного файла передано через ключ `-o`. |

### 1.7 Компоновка

| Команда для выполнения этапа | `/usr/libexec/gcc/x86_64-linux-gnu/15/collect2 -plugin /usr/libexec/gcc/x86_64-linux-gnu/15/liblto_plugin.so -plugin-opt=/usr/libexec/gcc/x86_64-linux-gnu/15/lto-wrapper -plugin-opt=-fresolution=a.res -plugin-opt=-pass-through=-lgcc -plugin-opt=-pass-through=-lgcc_s -plugin-opt=-pass-through=-lc -plugin-opt=-pass-through=-lgcc -plugin-opt=-pass-through=-lgcc_s --build-id --eh-frame-hdr -m elf_x86_64 --hash-style=gnu --as-needed -dynamic-linker /lib64/ld-linux-x86-64.so.2 -pie -z now -z relro /usr/lib/gcc/x86_64-linux-gnu/15/../../../x86_64-linux-gnu/Scrt1.o /usr/lib/gcc/x86_64-linux-gnu/15/../../../x86_64-linux-gnu/crti.o /usr/lib/gcc/x86_64-linux-gnu/15/crtbeginS.o -L/usr/lib/gcc/x86_64-linux-gnu/15 -L/usr/lib/gcc/x86_64-linux-gnu/15/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/15/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/15/../../.. -L/lib -L/usr/lib a-hello.o -lgcc --push-state --as-needed -lgcc_s --pop-state -lc -lgcc --push-state --as-needed -lgcc_s --pop-state /usr/lib/gcc/x86_64-linux-gnu/15/crtendS.o /usr/lib/gcc/x86_64-linux-gnu/15/../../../x86_64-linux-gnu/crtn.o` |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| Вход                       | a-hello.o                                                                                                                                                                                                                                         |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Выход                      | a.out                                                                                                                                                                                                                                             |
| Назначение                 | Связывание объектных файлов и библиотек в единый исполняемый файл, разрешение внешних ссылок и адресов функций                                                                                                                                    |
| Имя утилиты                | `/usr/libexec/gcc/x86_64-linux-gnu/15/collect2` (Внутренний драйвер компоновки GCC, вызывающий системный `ld`)                                                                                                                                    |
| Способ передачи параметров | Объектные файлы, пути к библиотекам (`-L`) и сами системные библиотеки (`-lc`, `-lgcc`) переданы в виде явных ключей и позиционных аргументов командной строки. Дополнительно используются переменные окружения `COMPILER_PATH` и `LIBRARY_PATH`. |

**Список объектных файлов, с которыми компонуется программа:**

| Имя         | Назначение                                                                                                                                                                                                      |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| a-hello.o   | Главный объектный файл, содержащий скомпилированный код функции main                                                                                                                                            |
| Scrt1.o     | Системный файл запуска (C Runtime Startup). Нужен для создания исполняемых файлов в режиме PIE (Position Independent Executable). Содержит точку входа `_start`, которая настраивает окружение и вызывает main. |
| crti.o      | Системный файл, содержащий специальную секцию кода инициализации (пролог функций `.init` и `.fini`), выполняемых до запуска main.                                                                               |
| crtbeginS.o | Объектный файл GCC (суффикс S для PIE), отвечающий за вызов конструкторов глобальных/статических объектов и регистрацию деструкторов.                                                                           |
| crtendS.o   | Объектный файл GCC, завершающий секции конструкторов и деструкторов, созданных в `crtbeginS.o`.                                                                                                                 |
| crtn.o      | Системный файл, закрывающий (эпилог) секции кода инициализации `.init` и `.fini`.                                                                                                                               |




**Список библиотек, с которыми компонуется программа:**

| Имя | Назначение |
| --- | --- |
| -lc (libc.so) | Стандартная библиотека языка Си. Содержит машинный код для базовых системных функций, включая вывод на экран (например, printf или puts). |
| -lgcc (libgcc.a) | Низкоуровневая библиотека поддержки GCC. Содержит вспомогательные внутренние функции для работы с типами данных, которые процессор не может обработать одной инструкцией. |
| -lgcc_s (libgcc_s.so) | Разделяемая (динамическая) часть библиотеки поддержки GCC. В основном отвечает за раскрутку стека (stack unwinding) при обработке исключений. |
| liblto_plugin.so | Плагин и утилита-обертка для оптимизации на этапе линковки (Link Time Optimization), выполняющие сквозную оптимизацию бинарного кода. |
| /lib64/ld-linux-x86-64.so.2 | Динамический линкер (загрузчик), прописываемый в заголовок бинарника для связывания библиотек в момент запуска программы в ОС. |

## 2 Компилятор clang

### 2.1 Версия компилятора
```bash
Ubuntu clang version 21.1.8 (6ubuntu1)
Target: x86_64-pc-linux-gnu
Thread model: posix
InstalledDir: /usr/lib/llvm-21/bin
```

### 2.2 Команда для получения исполняемого файла
```bash
clang -std=c99 -Wall -Werror -v -save-temps hello.c -o program_clang.exe
```

**-v** - подробный вывод информации о процессе компиляции

**-save-temps** - сохраняет все промежуточные (временные) файлы, которые создаются в процессе сборки программы

#### Вывод компиляции
```bash
Ubuntu clang version 21.1.8 (6ubuntu1)
Target: x86_64-pc-linux-gnu
Thread model: posix
InstalledDir: /usr/lib/llvm-21/bin
Found candidate GCC installation: /usr/lib/gcc/x86_64-linux-gnu/15
Selected GCC installation: /usr/lib/gcc/x86_64-linux-gnu/15
Candidate multilib: .;@m64
Selected multilib: .;@m64
 "/usr/lib/llvm-21/bin/clang" -cc1 -triple x86_64-pc-linux-gnu -E -dumpdir program_clang.exe- -save-temps=cwd -disable-free -clear-ast-before-backend -disable-llvm-verifier -discard-value-names -main-file-name hello.c -mrelocation-model pic -pic-level 2 -pic-is-pie -mframe-pointer=all -fmath-errno -ffp-contract=on -fno-rounding-math -mconstructor-aliases -funwind-tables=2 -target-cpu x86-64 -tune-cpu generic -debugger-tuning=gdb -fdebug-compilation-dir=/media/sf_union_dir_ubuntu/clang -v -fcoverage-compilation-dir=/media/sf_union_dir_ubuntu/clang -resource-dir /usr/lib/llvm-21/lib/clang/21 -internal-isystem /usr/lib/llvm-21/lib/clang/21/include -internal-isystem /usr/local/include -internal-isystem /usr/lib/gcc/x86_64-linux-gnu/15/../../../../x86_64-linux-gnu/include -internal-externc-isystem /usr/include/x86_64-linux-gnu -internal-externc-isystem /include -internal-externc-isystem /usr/include -Wall -Werror -std=c99 -ferror-limit 19 -fmessage-length=114 -fgnuc-version=4.2.1 -fskip-odr-check-in-gmf -fcolor-diagnostics -faddrsig -D__GCC_HAVE_DWARF2_CFI_ASM=1 -o hello.i -x c hello.c
clang -cc1 version 21.1.8 based upon LLVM 21.1.8 default target x86_64-pc-linux-gnu
ignoring nonexistent directory "/usr/lib/gcc/x86_64-linux-gnu/15/../../../../x86_64-linux-gnu/include"
ignoring nonexistent directory "/include"
#include "..." search starts here:
#include <...> search starts here:
 /usr/lib/llvm-21/lib/clang/21/include
 /usr/local/include
 /usr/include/x86_64-linux-gnu
 /usr/include
End of search list.
 "/usr/lib/llvm-21/bin/clang" -cc1 -triple x86_64-pc-linux-gnu -emit-llvm-bc -emit-llvm-uselists -dumpdir program_clang.exe- -save-temps=cwd -disable-free -clear-ast-before-backend -disable-llvm-verifier -discard-value-names -main-file-name hello.c -mrelocation-model pic -pic-level 2 -pic-is-pie -mframe-pointer=all -fmath-errno -ffp-contract=on -fno-rounding-math -mconstructor-aliases -funwind-tables=2 -target-cpu x86-64 -tune-cpu generic -debugger-tuning=gdb -fdebug-compilation-dir=/media/sf_union_dir_ubuntu/clang -v -fcoverage-compilation-dir=/media/sf_union_dir_ubuntu/clang -resource-dir /usr/lib/llvm-21/lib/clang/21 -Wall -Werror -std=c99 -ferror-limit 19 -fmessage-length=114 -fgnuc-version=4.2.1 -fskip-odr-check-in-gmf -fcolor-diagnostics -disable-llvm-passes -faddrsig -D__GCC_HAVE_DWARF2_CFI_ASM=1 -o hello.bc -x cpp-output hello.i
clang -cc1 version 21.1.8 based upon LLVM 21.1.8 default target x86_64-pc-linux-gnu
#include "..." search starts here:
End of search list.
 "/usr/lib/llvm-21/bin/clang" -cc1 -triple x86_64-pc-linux-gnu -S -dumpdir program_clang.exe- -save-temps=cwd -disable-free -clear-ast-before-backend -disable-llvm-verifier -discard-value-names -main-file-name hello.c -mrelocation-model pic -pic-level 2 -pic-is-pie -mframe-pointer=all -fmath-errno -ffp-contract=on -fno-rounding-math -mconstructor-aliases -funwind-tables=2 -target-cpu x86-64 -tune-cpu generic -debugger-tuning=gdb -fdebug-compilation-dir=/media/sf_union_dir_ubuntu/clang -v -fcoverage-compilation-dir=/media/sf_union_dir_ubuntu/clang -resource-dir /usr/lib/llvm-21/lib/clang/21 -Wall -Werror -std=c99 -ferror-limit 19 -fmessage-length=114 -fgnuc-version=4.2.1 -fskip-odr-check-in-gmf -fcolor-diagnostics -faddrsig -D__GCC_HAVE_DWARF2_CFI_ASM=1 -o hello.s -x ir hello.bc
clang -cc1 version 21.1.8 based upon LLVM 21.1.8 default target x86_64-pc-linux-gnu
 "/usr/lib/llvm-21/bin/clang" -cc1as -triple x86_64-pc-linux-gnu -filetype obj -main-file-name hello.c -target-cpu x86-64 -fdebug-compilation-dir=/media/sf_union_dir_ubuntu/clang -dwarf-version=5 -mrelocation-model pic -o hello.o hello.s
 "/usr/bin/ld" -z relro --hash-style=gnu --build-id --eh-frame-hdr -m elf_x86_64 -pie -dynamic-linker /lib64/ld-linux-x86-64.so.2 -o program_clang.exe /lib/x86_64-linux-gnu/Scrt1.o /lib/x86_64-linux-gnu/crti.o /usr/lib/gcc/x86_64-linux-gnu/15/crtbeginS.o -L/usr/lib/gcc/x86_64-linux-gnu/15 -L/usr/lib/gcc/x86_64-linux-gnu/15/../../../../lib64 -L/lib/x86_64-linux-gnu -L/lib/../lib64 -L/usr/lib/x86_64-linux-gnu -L/usr/lib64 -L/lib -L/usr/lib hello.o -lgcc --as-needed -lgcc_s --no-as-needed -lc -lgcc --as-needed -lgcc_s --no-as-needed /usr/lib/gcc/x86_64-linux-gnu/15/crtendS.o /lib/x86_64-linux-gnu/crtn.o
```

### 2.3 Список файлов, полученных в результате компиляции
|        Имя        | Размер (байт) |      Тип      |
| :---------------: | :-----------: | :-----------: |
|      hello.c      |      129      |   Текстовый   |
|      hello.i      |     21937     |   Текстовый   |
|     hello.bc      |     2680      | Бинарный файл |
|      hello.s      |      835      |   Текстовый   |
|      hello.o      |     1264      |   Объектный   |
| program_clang.exe |     16000     |  Исполняемый  |

### 2.4 Препроцессирование

| Команда для выполнения этапа | `"/usr/lib/llvm-21/bin/clang" -cc1 -triple x86_64-pc-linux-gnu -E -dumpdir program_clang.exe- -save-temps=cwd -disable-free -clear-ast-before-backend -disable-llvm-verifier -discard-value-names -main-file-name hello.c -mrelocation-model pic -pic-level 2 -pic-is-pie -mframe-pointer=all -fmath-errno -ffp-contract=on -fno-rounding-math -mconstructor-aliases -funwind-tables=2 -target-cpu x86-64 -tune-cpu generic -debugger-tuning=gdb -fdebug-compilation-dir=/media/sf_union_dir_ubuntu/clang -v -fcoverage-compilation-dir=/media/sf_union_dir_ubuntu/clang -resource-dir /usr/lib/llvm-21/lib/clang/21 -internal-isystem /usr/lib/llvm-21/lib/clang/21/include -internal-isystem /usr/local/include -internal-isystem /usr/lib/gcc/x86_64-linux-gnu/15/../../../../x86_64-linux-gnu/include -internal-externc-isystem /usr/include/x86_64-linux-gnu -internal-externc-isystem /include -internal-externc-isystem /usr/include -Wall -Werror -std=c99 -ferror-limit 19 -fmessage-length=114 -fgnuc-version=4.2.1 -fskip-odr-check-in-gmf -fcolor-diagnostics -faddrsig -D__GCC_HAVE_DWARF2_CFI_ASM=1 -o hello.i -x c hello.c` |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |

| Вход                       | hello.c                                                                                                                                                                                                                  |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Выход                      | hello.i                                                                                                                                                                                                                  |
| Назначение                 | удаляет комментарии, вставляет файлы (директива include), заменяет текст (раскрытие макросов, директива define), выполняет условную компиляцию (директива if)                                                            |
| Имя утилиты                | `/usr/lib/llvm-21/bin/clang` (с внутренним флагом `-cc1` в режиме препроцессора `-E`)                                                                                                                                    |
| Способ передачи параметров | Входной файл передан в конце через `-x` c `hello.c`, пути поиска системных заголовков жестко заданы через флаги `-internal-isystem` и `-internal-externc-isystem`, имя выходного файла передано через ключ `-o hello.i`. |



### 2.5 Трансляция Си-кода в промежуточное представление (LLVM Bitcode)

| Команда для выполнения этапа | `"/usr/lib/llvm-21/bin/clang" -cc1 -triple x86_64-pc-linux-gnu -emit-llvm-bc -emit-llvm-uselists -dumpdir program_clang.exe- -save-temps=cwd -disable-free -clear-ast-before-backend -disable-llvm-verifier -discard-value-names -main-file-name hello.c -mrelocation-model pic -pic-level 2 -pic-is-pie -mframe-pointer=all -fmath-errno -ffp-contract=on -fno-rounding-math -mconstructor-aliases -funwind-tables=2 -target-cpu x86-64 -tune-cpu generic -debugger-tuning=gdb -fdebug-compilation-dir=/media/sf_union_dir_ubuntu/clang -v -fcoverage-compilation-dir=/media/sf_union_dir_ubuntu/clang -resource-dir /usr/lib/llvm-21/lib/clang/21 -Wall -Werror -std=c99 -ferror-limit 19 -fmessage-length=114 -fgnuc-version=4.2.1 -fskip-odr-check-in-gmf -fcolor-diagnostics -disable-llvm-passes -faddrsig -D__GCC_HAVE_DWARF2_CFI_ASM=1 -o hello.bc -x cpp-output hello.i` |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| Вход                       | hello.i                                                                                                                                        |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| Выход                      | hello.bc                                                                                                                                       |
| Назначение                 | Синтаксический анализ предобработанного Си-кода и его перевод во внутренний независимый от платформы байт-код LLVM (LLVM Bitcode).             |
| Имя утилиты                | `/usr/lib/llvm-21/bin/clang` (с флагом `-cc1` и инструкцией генерации биткода `-emit-llvm-bc`)                                                 |
| Способ передачи параметров | Входной файл передан через явное указание типа -x cpp-output hello.i, имя результирующего бинарного биткода передано через ключ `-o hello.bc`. |

### 2.6 Трансляция промежуточного представления в код ассемблера

| Команда для выполнения этапа | `"/usr/lib/llvm-21/bin/clang" -cc1 -triple x86_64-pc-linux-gnu -S -dumpdir program_clang.exe- -save-temps=cwd -disable-free -clear-ast-before-backend -disable-llvm-verifier -discard-value-names -main-file-name hello.c -mrelocation-model pic -pic-level 2 -pic-is-pie -mframe-pointer=all -fmath-errno -ffp-contract=on -fno-rounding-math -mconstructor-aliases -funwind-tables=2 -target-cpu x86-64 -tune-cpu generic -debugger-tuning=gdb -fdebug-compilation-dir=/media/sf_union_dir_ubuntu/clang -v -fcoverage-compilation-dir=/media/sf_union_dir_ubuntu/clang -resource-dir /usr/lib/llvm-21/lib/clang/21 -Wall -Werror -std=c99 -ferror-limit 19 -fmessage-length=114 -fgnuc-version=4.2.1 -fskip-odr-check-in-gmf -fcolor-diagnostics -faddrsig -D__GCC_HAVE_DWARF2_CFI_ASM=1 -o hello.s -x ir hello.bc` |
| ---------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| Вход                       | hello.bc                                                                                                                                                       |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Выход                      | hello.s                                                                                                                                                        |
| Назначение                 | Превращение универсального байт-кода LLVM в платформозависимый текстовый код ассемблера под конкретную архитектуру процессора (в данном случае x86-64).        |
| Имя утилиты                | `/usr/lib/llvm-21/bin/clang` (с флагом `-cc1` и инструкцией остановки на этапе ассемблера `-S`)                                                                |
| Способ передачи параметров | Входной файл передан через указание внутреннего промежуточного формата `-x ir hello.bc`, результирующий текстовый ассемблерный файл задан ключом `-o hello.s`. |

### 2.7 Трансляция программы с языка ассемблера в машинный код

| Команда для выполнения этапа | `"/usr/lib/llvm-21/bin/clang" -cc1as -triple x86_64-pc-linux-gnu -filetype obj -main-file-name hello.c -target-cpu x86-64 -fdebug-compilation-dir=/media/sf_union_dir_ubuntu/clang -dwarf-version=5 -mrelocation-model pic -o hello.o hello.s` |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| Вход                       | hello.s                                                                                                                                                   |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Выход                      | hello.o                                                                                                                                                   |
| Назначение                 | Ассемблирование текстового файла инструкций в перемещаемый двоичный объектный файл (машинный код) с добавлением отладочной информации стандарта DWARFv5.  |
| Имя утилиты                | `/usr/lib/llvm-21/bin/clang` (с флагом встроенного ассемблера `-cc1as`)                                                                                   |
| Способ передачи параметров | Входной файл hello.s передан аргументом в конце, тип выходного файла задан ключом `-filetype obj`, имя объектного файла передано через ключ `-o hello.o`. |

### 2.8 Компоновка (Линковка)

| Команда для выполнения этапа | `"/usr/bin/ld" -z relro --hash-style=gnu --build-id --eh-frame-hdr -m elf_x86_64 -pie -dynamic-linker /lib64/ld-linux-x86-64.so.2 -o program_clang.exe /lib/x86_64-linux-gnu/Scrt1.o /lib/x86_64-linux-gnu/crti.o /usr/lib/gcc/x86_64-linux-gnu/15/crtbeginS.o -L/usr/lib/gcc/x86_64-linux-gnu/15 -L/usr/lib/gcc/x86_64-linux-gnu/15/../../../../lib64 -L/lib/x86_64-linux-gnu -L/lib/../lib64 -L/usr/lib/x86_64-linux-gnu -L/usr/lib64 -L/lib -L/usr/lib hello.o -lgcc --as-needed -lgcc_s --no-as-needed -lc -lgcc --as-needed -lgcc_s --no-as-needed /usr/lib/gcc/x86_64-linux-gnu/15/crtendS.o /lib/x86_64-linux-gnu/crtn.o` |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

| Вход                       | hello.o (а также системные файлы инициализации Scrt1.o, crti.o и др.)                                                                                                                                                            |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Выход                      | program_clang.exe                                                                                                                                                                                                                |
| Назначение                 | Связывание объектных модулей программы и необходимых разделяемых библиотек в итоговый позиционно-независимый исполняемый файл.                                                                                                   |
| Имя утилиты                | `/usr/bin/ld` (Системный компоновщик GNU linker)                                                                                                                                                                                 |
| Способ передачи параметров | Пути поиска библиотек (`-L`), флаги динамической линковки (`-lgcc`, `-lc`) и список всех связываемых объектных файлов переданы как прямые аргументы командной строки; имя готовой программы задано через `-o program_clang.exe`. |

**Список объектных файлов, с которыми компонуется программа:**

| Имя | Назначение |
| --- | --- |
| hello.o | Главный объектный файл, содержащий скомпилированный код функции main |
| `/lib/x86_64-linux-gnu/Scrt1.o` | Системный файл инициализации среды выполнения (C Runtime Startup) для программ в режиме PIE. Настраивает стек и содержит точку входа _start, передающую управление в main. |
| `/lib/x86_64-linux-gnu/crti.o` | Специальный системный объектный файл, содержащий точку входа в секции инициализации и финализации (`.init` и `.fini`), выполняемые до и после основного кода программы. |
| `/usr/lib/gcc/x86_64-linux-gnu/15/crtbeginS.o` | Файл из состава установленного в системе GCC 15, отвечающий за корректный запуск конструкторов глобальных и статических объектов Си/C++. |
| `/usr/lib/gcc/x86_64-linux-gnu/15/crtendS.o` | Файл из состава GCC 15, завершающий и закрывающий секции конструкторов и деструкторов. |
| `/lib/x86_64-linux-gnu/crtn.o` | Конечный системный файл, завершающий секции кода инициализации `.init` и `.fini`. |

**Список библиотек, с которыми компонуется программа:**

| Имя | Назначение |
| --- | --- |
| `-lc (libc.so)` | Стандартная библиотека языка Си. Содержит машинный код для базовых системных функций, включая вывод на экран (например, printf или puts). |
| `-lgcc (libgcc.a)` | Низкоуровневая библиотека поддержки GCC. Содержит вспомогательные внутренние функции для работы с типами данных, которые процессор не может обработать одной инструкцией. |
| `-lgcc_s (libgcc_s.so)` | Разделяемая (динамическая) часть библиотеки поддержки GCC. В основном отвечает за раскрутку стека (stack unwinding) при обработке исключений. |
| `/lib64/ld-linux-x86-64.so.2` | Динамический линкер (передан через параметр `-dynamic-linker`), внедряемый в заголовок файла, чтобы операционная система при запуске `program_clang.exe` знала, как связать программу с динамической библиотекой `libc.so`. |


## 3 Дополнительные задания

### 3.1 Какие динамические библиотеки использует исполняемый файл?

Команда для выполнения:
```bash
ldd a.out
```

Вывод:
```bash
	linux-vdso.so.1 (0x00007c1d4805e000)
	libc.so.6 => /usr/lib/x86_64-linux-gnu/libc.so.6 (0x00007c1d47e00000)
	/lib64/ld-linux-x86-64.so.2 (0x00007c1d48060000)
```

Исполняемый файл использует следующие динамические библиотеки:
- `linux-vdso.so.1` - Виртуальная библиотека ядра Linux для ускорения системных вызовов (не хранится на диске).
- `libc.so.6` - Стандартная библиотека языка Си (необходима для работы функции puts).
- `ld-linux-x86-64.so.2` — Динамический линкер/загрузчик операционной системы, который связывает библиотеки в момент запуска программы.

### 3.2 С помощью какого ключа компилятора gcc можно передавать параметры компилятору с языка ассемблера? 

Для передачи параметров напрямую системному ассемблеру (`as`) драйвер компилятора `gcc` использует ключ `-Wa,параметры`. Ключи разделяются запятыми.
Команда для выполнения:
```bash
gcc -Wa,-a,-ad hello.c -o a.out > hello_listing.txt
```

hello_listiong.txt:
```
...
GAS LISTING /tmp/cccRh1SS.s 			page 2


DEFINED SYMBOLS
                            *ABS*:0000000000000000 hello.c
     /tmp/cccRh1SS.s:9      .text:0000000000000000 main

UNDEFINED SYMBOLS
puts
```

Параметр `-Wa,-a,-ad` приказывает ассемблеру сгенерировать подробный листинг кода Си вместе со скомпилированными инструкциями процессора и адресами памяти, который перенаправлен в файл `hello_listing.txt`.

### 3.3 С помощью какого ключа компилятора gcc можно передавать параметры компоновщику. 

Для передачи параметров напрямую системному компоновщику (`ld`) драйвер компилятора `gcc` использует ключ `-Wl,параметры`.

Команда для выполнения:
```bash
gcc -Wl,-Map=output.map hello.c -o a.out
```

Часть файла output.map:
```
...
Memory Configuration

Name             Origin             Length             Attributes
*default*        0x0000000000000000 0xffffffffffffffff

Linker script and memory map
...
```

Параметр `-Wl,-Map=output.map` приказывает компоновщику выгрузить карту распределения памяти (Map-файл) в текстовый документ `output.map`. В нем подробно расписано, по каким адресам в бинарном файле расположились функции, переменные и системные библиотеки.
### 3.4 Влияние флагов отладки на размер исполняемого файла

Флаги `-g0, -g1, -g2, -g3` управляют уровнем генерации отладочной информации компилятора.

```bash
gcc -g0 hello.c -o res_g0 && gcc -g1 hello.c -o res_g1 && gcc -g2 hello.c -o res_g2 && gcc -g3 hello.c -o res_g3 && wc -c res_g*
```

Значения для Ubuntu x86-64 выглядят так:

| | Размер исполняемого файла (в байтах) |
| --- | --- |
| g0 | 15952 |
| g1 | 16952 |
| g2 | 17168 |
| g3 | 45408 |

Вывод:
С увеличением числового индекса в ключе `-g` (от 0 до 3) размер исполняемого файла последовательно растет. Это происходит потому, что компилятор внедряет внутрь исполняемого файла (`.ELF` (Executable and Linkable Format)) дополнительные служебные секции отладки (например, `.debug_info`, `.debug_line`, `.debug_macro`), которые не влияют на скорость выполнения программы, но необходимы отладчику `gdb` для сопоставления машинного кода с исходным текстом Си.