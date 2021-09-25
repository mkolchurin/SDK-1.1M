
# non-standart IDEs

Программирование микроконтроллеров, в том числе тех, что представлены в платформе SDK-1.1M, подразумевает широкую вариативность в выборе инструментов. STMicroelectronics предоставляет all-in-one инструмент [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html), который позволяет в кратчайшие сроки и бесплатно перейти к созданию продукта для их микроконтроллеров. Однако, не всем может прийтись по вкусу выбор среды для разработки - Eclipse (который является основой для STM32CubeIDE), а также системы сборки выбранной по-умолчанию - [Eclipse CDT](https://www.eclipse.org/cdt/).

Выбор среды удобной для разработчика, должен быть за разработчиком, в связи с чем даннай гайд направлен на то чтобы предоставить такой выбор. Однако, в связи с тем, что существующие IDE в большинстве своем не all-in-one решения, разработчику необходимо установить специализированные инструментальные средства для сборки, компиляции, загрузки и отладки программ для микроконтроллеров.

SDK-1.1M может поставляться с несколькими процессорными модулями, в том числе и не STM32, однако реализации наибольшего числа SDK-1.1M представлены с микроконтроллерами STMicroelectronics, в связи с чем, данная инструкция направлена на работу с ними.

## Инструментальные средства

- [arm-none-eabi toolchain](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads) - линковка, компиляция и откладка

- [CMake](https://cmake.org/) - автоматизация сборки (не обязательно)

- [Make](https://www.gnu.org/software/make/), [Ninja](https://ninja-build.org/), [Eclipse CDT](https://www.eclipse.org/cdt/) и другие - система сборки

- [OpenOCD](https://openocd.org/) - встроенное (on-chip) программирование и отладка

# Установка и настройка toolchain

## Общий путь\*

1. Загрузить и извлечь бинарный пакет соответствующий вашей операционной системе и архитектуре с сайта [ARM](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads)

2. Указать путь системе сборки, используемой в проекте

\*данный путь не оптимален и требует тянуть за проектом весь toolchain, однако максимально портативен.

## Windows

### Вариант №1

1

### Вариант №2

Наиболее удобным вариантом сборки приложений для микроконтроллеров ARM из Windows является использование [WSL/WSL2](https://docs.microsoft.com/ru-ru/windows/wsl/install-win10#simplified-installation-for-windows-insiders)

После установки одной из операционных систем, необходимо установить toolchain в гостевую среду. Данный процесс подробно описан в [Linux][1]

## Linux


## CLion

1. Установить и настроить WSL/WSL2
2. Запустить Clion
3. Выбрать toolchain как remote wsl

## VSC
	1. W


## MacOS - brew
https://github.com/ARMmbed/homebrew-formulae

## Linux
sudo apt install gcc-arm-none-eabi
Pacman -S arm-none-eabi-gcc

## Системы сборки

Для сборки проектов STM32 подойдет любая система сборки, которая умеет работать с C/C++ кодом,одни из самых популярных вариантов - [make](https://www.gnu.org/software/make/) и [ninja](https://ninja-build.org/).

## Системы автоматизации сборки

# Clion
Windows 
ПО:
Git
Cmake
OpenOCD

# UNIT тестирование (unfinished)
