# AFC - Alpha Flight Controller (Teensy 4.1)

![Status](https://img.shields.io/badge/Status-PCB%20Pronta-green)
![Versao](https://img.shields.io/badge/Versao-1.0-blue)
![DRC](https://img.shields.io/badge/DRC-0%20Erros-brightgreen)

## Visao Geral

Controlador de navegacao desenvolvido pela **Alpha Subsea** para ROVs e drones subaquaticos, baseado na plataforma **Teensy 4.1** (ARM Cortex-M7 @ 600MHz).

### Caracteristicas Principais:
- **MCU:** Teensy 4.1 (600MHz, 1MB RAM)
- **Sensores:** IMU (ICM-42688-P), Magnetometro (LIS3MDL), Barometro (BMP390), Profundidade (MS5837-30BA)
- **PWM:** 16 canais via PCA9685 (8 thrusters + 4 servos)
- **Comunicacao:** Serial 1Mbps com Raspberry Pi
- **ADC:** ADS1115 16-bit para monitoramento de tensao/corrente

## Estrutura de Arquivos

```
AFC_CICLO DESENVOLVIMENTO.html    # Ciclo de desenvolvimento (40% completo)
AFC_TEENSY_PCB_DOCUMENTACAO.md    # Documentacao tecnica completa
BOM_AFC_TEENSY_LCSC.csv           # Lista de materiais com codigos LCSC
Gerber_*.zip                       # Arquivos Gerber para fabricacao
PCB_*.json                         # PCB EasyEDA
PCB_*.kicad_pcb                    # PCB KiCad
SCH_*.json                         # Esquematico EasyEDA
Schematic_*.pdf                    # Esquematico PDF
Sheet_1_*.schdoc                   # Esquematico Altium (para KiCad)
*.png                              # Screenshots de validacao
```

## Status do Projeto

| Fase | Progresso | Status |
|------|-----------|--------|
| 1. Plan | 100% | Concluido |
| 2. Code | 100% | Firmware + Esquematico prontos |
| 3. Build | 100% | Gerbers prontos para fabricacao |
| 4. Test | 0% | Pendente |
| 5. Homologation | 0% | Pendente |

**Progresso Geral: 42%**

## BOM - Lista de Materiais

Total de **63 componentes** com codigos LCSC para montagem SMD.

### Componentes Principais:
| Componente | Modelo | LCSC |
|------------|--------|------|
| IMU 6-DoF | ICM-42688-P | C1850418 |
| Magnetometro | LIS3MDL | C478483 |
| Barometro | BMP390 | C9900016584 |
| PWM Driver | PCA9685PW | C2678753 |
| ADC 16-bit | ADS1115 | C37593 |
| Buck Converter | MP1584EN | C15051 |
| Power Monitor | INA226 | C49851 |

**Custo estimado:** ~$50-70 USD (sem Teensy e MS5837)

## Como Fabricar

1. **Fabricacao da PCB:**
   - Utilizar o arquivo `Gerber_*.zip` para fabricacao
   - BOM disponivel em `BOM_AFC_TEENSY_LCSC.csv`

2. **Importar no KiCad 9.0:**
   - `File` -> `Import Project...` -> `Altium Designer`
   - Selecionar `Sheet_1_*.schdoc`

## Firmware

Firmware desenvolvido em PlatformIO com as seguintes features:
- Loop de controle a 400Hz
- PID com anti-windup
- Mixer para 8 thrusters (BlueROV2 Heavy)
- Protocolo binario com CRC16
- Telemetria a 50Hz

## Documentacao

- [Documentacao Tecnica](AFC_TEENSY_PCB_DOCUMENTACAO.md)
- [Ciclo de Desenvolvimento](AFC_CICLO%20DESENVOLVIMENTO.html)
- [BOM LCSC](BOM_AFC_TEENSY_LCSC.csv)

## Equipe

**Alpha Subsea** - Tecnologia Submarina  
Desenvolvido por **Arbor Gestao**

---

*Ultima atualizacao: Janeiro 2026*
