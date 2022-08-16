IT'S NOT FINISHED / NÃO ESTÁ PRONTO
# Lenovo G40-80 hackintosh laptop with Open Core. Português/English.

Depois de Diversas Tentativas, consegui ajustar razoavelmente meu hakintosh, vou deixando aqui a minha EFI base e as Atualizações, juntamente com os detalhes de como cheguei até aqui.

## 🚀 Começando

Essa Geração de processadores Intel Broadwell e um pouco complicada, tem varios problemas a se ajustar, fiquei dias por exemplo para conseguir o gráfico integrado haha.
## Specs:
```
Modelo: Lenovo G40-80
CPU: I3-5005U 
GRAPHICS: Intel HD Graphics 5500
DRIVE: SSD Kingston 128gb
RAM: 8GB (2X4)
AUDIO: Conexant ;;;;
ETHERNET: RTL8111
```
### 📋 EFI BASE (Open core 0.8.3)
Creditos ao Gabriel luchina pela EFI base e pelo tutorial.
https://github.com/luchina-gabriel/BASE-EFI-INTEL-DESKTOP-5THGEN-BROADWELL.git

[GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)

[Propertree](https://github.com/corpnewt/ProperTree)

Porem a EFI do repositorio do Gabriel e para desktop, então temos de fazer algumas modificações.
### 🔧 Instalação

Uma série de exemplos passo-a-passo que informam o que você deve executar para ter um ambiente de desenvolvimento em execução.

## DSDT + DSDT PATCH
SSDT-PLUG-DRTNIA
SSDT-EC-LAPTOP
SSDT-PNLF
SSDT-XOSI
dsdt-dl (Compilado Manualmente para funcionar teclas de brilho f11/f12.
## Kexts
Note|##
:---|:---
[Lilu Kext](https://github.com/acidanthera/Lilu/releases)
[SMC Processor, VirtualSMC, SMCsuperIO](https://github.com/acidanthera/VirtualSMC/releases)|
[WhateverGreen](https://github.com/acidanthera/WhateverGreen/releases)|
[AppleALC.kext](https://github.com/acidanthera/AppleALC/releases)
[RealtekRTL8111.kext](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases)
## Drivers
```
Dar exemplos
```
hahaha

E repita:

```
Até finalizar
```

Termine com um exemplo de como obter dados do sistema ou como usá-los para uma pequena demonstração.

## ⚙️ Executando os testes

Explicar como executar os testes automatizados para este sistema.

### 🔩 Analise os testes de ponta a ponta

Explique que eles verificam esses testes e porquê.

```
Dar exemplos
```

### ⌨️ E testes de estilo de codificação

Explique que eles verificam esses testes e porquê.

```
Dar exemplos
```

## 📦 Desenvolvimento

Adicione notas adicionais sobre como implantar isso em um sistema ativo

## 🛠️ Construído com

Mencione as ferramentas que você usou para criar seu projeto

* [D/1.0 frweb usadoghg
* [Mavennpendênciaghgh
* [Rromepara gerar RSSfghfh

## 🖇️ Colaborando

Por favor, leia o [COLABORACAO.md](https://gist.github.com/usuario/linkParaInfoSobreContribuicoes) para obter detalhes sobre o nosso código de conduta e o processo para nos enviar pedidos de solicitação.

## 📌 LINK 
Esses guias me deram um Norte:

[upupming](https://github.com/upupming/Lenovo-G50-80-Clover.git)

[Gabriel Luchina](https://github.com/rodolfom99/BASE-EFI-INTEL-DESKTOP-5THGEN-BROADWELL.git)

[Dortania Guide](https://dortania.github.io/OpenCore-Install-Guide/)

