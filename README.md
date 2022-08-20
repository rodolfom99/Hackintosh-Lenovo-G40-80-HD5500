IT'S NOT FINISHED / NÃO ESTÁ PRONTO
# Lenovo G40-80 hackintosh laptop with Open Core. Português/English (coming soon).
![Screen Shot 2022-08-09 at 07 26 11](https://user-images.githubusercontent.com/111351901/184874734-33abe973-97cc-4b47-b708-f5dd3a31f458.png)"


Depois de Diversas Tentativas, consegui ajustar razoavelmente meu hakintosh, vou deixando aqui a minha EFI base e as Atualizações, juntamente com os detalhes de como cheguei até aqui.

## 🚀 Começando
ATENÇÃO PARA CATALINA OU VERSOES ANTERIORES E NESCESSARIO ADICIONAR NA MINHA EFI MinDate and MinVersion in UEFI > APFS to -1 e também SecureBootModel in Misc > Security to j137. para bigsur ou posterior ignore.
Essa Geração de processadores Intel Broadwell-U e um pouco complicada, tem varios problemas a se ajustar, fiquei dias por exemplo para conseguir o gráfico integrado haha.
## Specs:
```
Modelo: Lenovo G40-80
CPU: I3-5005U ✅
Graphics: Intel HD Graphics 5500 ✅
Drive: SSD Kingston 128gb ✅
RAM: 8GB (2X4) ✅
Audio: Conexant CX20751/2 ✅
Ethernet: RTL8111 ✅
Bluetooth: Atheros AR3012 ❌
WIFI: Atheros AR9565 ❌
WIFI DONGLE TP-LINK TL-WN725N ✅
```
### 📋 [EFI BASE](https://github.com/luchina-gabriel/BASE-EFI-INTEL-DESKTOP-5THGEN-BROADWELL.git)(Open core 0.8.3)
Creditos ao Gabriel luchina pela EFI base e pelo tutorial.
[luchina-gabriel](https://github.com/luchina-gabriel)

Porem a EFI do repositorio do Gabriel e para desktop, então temos de fazer algumas modificações.

### 📋 [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
Note que a SMBIOS gerada para essa EFI é genérica e precisa ser substituída no config.plist assim que o macOS for instalado. gere seus próprios valores com o GenSMBIOS e os insira no arquivo por meio do ProperTree.

### 📋 [Propertree](https://github.com/corpnewt/ProperTree)


### 🔧 Instalação

Uma série de exemplos passo-a-passo que informam o que você deve executar para ter um ambiente de desenvolvimento em execução.

## DSDT + DSDT PATCH
Nota/Note|Link
:---|:---
ALL SSDTs |[SSDTs](https://dortania.github.io/Getting-Started-With-ACPI/ssdt-platform.html#desktop)
SSDT-PLUG-DRTNIA|[Prebuild](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-PLUG-DRTNIA.aml)
SSDT-EC-LAPTOP (for Broadwell and older)|[Prebuild](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-EC-LAPTOP.aml)
SSDT-PNLF (Luz de fundo)|[Prebuild](https://github.com/dortania/Getting-Started-With-ACPI/blob/master/extra-files/compiled/SSDT-PNLF.aml)
SSDT-XOSI|[Prebuild](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/trackpad)
SSDT-
dsdt-dl (Compilado Manualmente para funcionar teclas de brilho f11/f12.| SÓ use no POST INSTALL caso contrario apague e dê clean snapshot.
## ⚙️ Kexts
Nota/Note|##
:---|:---
[Lilu Kext](https://github.com/acidanthera/Lilu/releases)
[SMC Processor, VirtualSMC, SMCsuperIO](https://github.com/acidanthera/VirtualSMC/releases)|
[WhateverGreen](https://github.com/acidanthera/WhateverGreen/releases)|
[AppleALC.kext](https://github.com/acidanthera/AppleALC/releases)
[RealtekRTL8111.kext](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases)
[EC-Enabler
## 🔧 Drivers

Padrão da EFI utilizada como base.

## ⚙️ Executando os testes

### 🔩 Analise os testes de ponta a ponta


### ⌨️ Post Install:
framebuffer-unifiedmem | Data | 
00000040 = 1024MB / 
00000060 = 1536MB / 
00000080 = 2048MB / 
000000A0 = 2560MB / 
000000C0 = 3072MB / 
000000E0 = 3584MB / 
FFFFFFFF = 4096MB
Adicionando a opção acima no config.plist e possivel aumentar a memoria da GPU integrada, eu testei apenas 2048mb.

## Funcionando ✅
```
Adapter WIFI tplink: ✅

Hd Graphics 5500: ✅ 
Não achei bom para jogos.(I didn't find it good for games)

Webcam: ✅

Brightness Control: ✅

Audio: ✅

Mensagem de falha ao desligar incorretamente (Corrigido)✅
```
## 📦 Desenvolvimento / Ainda não Funciona
```
WIFI: não e compativel, tentei trocar para intel mas a bios rejeitou. ❌

Bluetooth: não consegui, creio que não e compativel. ❌

Sleeping: Ao acordar do sleep ele reinicia. (tentando corrigir) ⚠️
```


## 🛠️ Construído com


## 🖇️ Colaborando

## 📌 LINK 
Esses guias me deram um Norte:

[upupming] (https://github.com/upupming/Lenovo-G50-80-Clover.git)

[Gabriel Luchina] (https://github.com/rodolfom99/BASE-EFI-INTEL-DESKTOP-5THGEN-BROADWELL.git)

[Dortania Guide] (https://dortania.github.io/OpenCore-Install-Guide/)

[prabhjot--singh] (https://www.reddit.com/r/hackintosh/comments/hkp7bh/opencore_059_lenovo_g4080_finally_on_catalina/)

[RehabMan] (https://www.tonymacx86.com/threads/guide-patching-laptop-dsdt-ssdts.152573/)
