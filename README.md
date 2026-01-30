# AFC - Alpha Flight Controller (Teensy 4.1)

![Status](https://img.shields.io/badge/Status-PCB%20Pronta-green)
![Versao](https://img.shields.io/badge/Versão-1.0-blue)
![DRC](https://img.shields.io/badge/DRC-0%20Erros-brightgreen)

## 📋 Visão Geral

Controlador de navegação desenvolvido pela **Alpha Subsea** para ROVs e drones subaquáticos, baseado na plataforma **Teensy 4.1** (ARM Cortex-M7 @ 600MHz).

### Características Principais:
- **MCU:** Teensy 4.1 (600MHz, 1MB RAM)
- **Sensores:** IMU (ICM-42688-P), Magnetômetro (LIS3MDL), Barômetro (BMP390), Profundidade (MS5837-30BA)
- **PWM:** 16 canais via PCA9685 (8 thrusters + 4 servos)
- **Comunicação:** Serial 1Mbps com Raspberry Pi
- **ADC:** ADS1115 16-bit para monitoramento de tensão/corrente

## 📁 Estrutura de Arquivos

```
├── AFC_CICLO DESENVOLVIMENTO.html    # Ciclo de desenvolvimento (40% completo)
├── AFC_TEENSY_PCB_DOCUMENTACAO.md    # Documentação técnica completa
├── BOM_AFC_TEENSY_LCSC.csv           # Lista de materiais com códigos LCSC
├── Gerber_*.zip                       # Arquivos Gerber para JLCPCB
├── PCB_*.json                         # PCB EasyEDA
├── PCB_*.kicad_pcb                    # PCB KiCad
├── SCH_*.json                         # Esquemático EasyEDA
├── Schematic_*.pdf                    # Esquemático PDF
├── Sheet_1_*.schdoc                   # Esquemático Altium (para KiCad)
└── *.png                              # Screenshots de validação
```

## 🔧 Status do Projeto

| Fase | Progresso | Status |
|------|-----------|--------|
| 1. Plan | 100% | ✅ Concluído |
| 2. Code | 100% | ✅ Firmware + Esquemático prontos |
| 3. Build | 88% | 🟡 Aguardando envio JLCPCB |
| 4. Test | 0% | ⏳ Pendente |
| 5. Homologation | 0% | ⏳ Pendente |

**Progresso Geral: 40%**

## 📦 BOM - Lista de Materiais

Total de **63 componentes** com códigos LCSC para montagem SMD na JLCPCB.

### Componentes Principais:
| Componente | Modelo | LCSC |
|------------|--------|------|
| IMU 6-DoF | ICM-42688-P | C1850418 |
| Magnetômetro | LIS3MDL | C478483 |
| Barômetro | BMP390 | C9900016584 |
| PWM Driver | PCA9685PW | C2678753 |
| ADC 16-bit | ADS1115 | C37593 |
| Buck Converter | MP1584EN | C15051 |
| Power Monitor | INA226 | C49851 |

**Custo estimado:** ~$50-70 USD (sem Teensy e MS5837)

## 🛠️ Como Fabricar

1. **Upload para JLCPCB:**
   - Fazer upload do arquivo `Gerber_*.zip`
   - Selecionar montagem SMD (Assembly)
   - Fazer upload do `BOM_AFC_TEENSY_LCSC.csv`

2. **Importar no KiCad 9.0:**
   - `File` → `Import Project...` → `Altium Designer`
   - Selecionar `Sheet_1_*.schdoc`

## 📡 Firmware

Firmware desenvolvido em PlatformIO com as seguintes features:
- Loop de controle a 400Hz
- PID com anti-windup
- Mixer para 8 thrusters (BlueROV2 Heavy)
- Protocolo binário com CRC16
- Telemetria a 50Hz

## 📄 Documentação

- [Documentação Técnica](AFC_TEENSY_PCB_DOCUMENTACAO.md)
- [Ciclo de Desenvolvimento](AFC_CICLO%20DESENVOLVIMENTO.html)
- [BOM LCSC](BOM_AFC_TEENSY_LCSC.csv)

## 👥 Equipe

**Alpha Subsea** - Tecnologia Submarina  
Desenvolvido por **Arbor Gestão**

---

*Última atualização: Janeiro 2026*
