# DOCUMENTACAO TECNICA - AFC TEENSY PCB
## Placa de Controle para ROV (Remotely Operated Vehicle)

---

## 1. INFORMACOES GERAIS DO PROJETO

| Parametro | Valor |
|-----------|-------|
| Nome do Projeto | AFC Teensy Controller |
| Versao | 1.0 |
| Data de Criacao | Janeiro 2026 |
| Plataforma de Design | EasyEDA |
| Fabricante Alvo | JLCPCB |

---

## 2. ESPECIFICACOES DA PCB

| Parametro | Valor |
|-----------|-------|
| Dimensoes | 100mm x 80mm |
| Camadas de Cobre | 2 (Top e Bottom) |
| Formato | Retangular |
| Unidade de Medida | Milimetros (mm) |
| Espessura da Placa | 1.6mm (padrao) |
| Material | FR-4 |

---

## 3. LISTA COMPLETA DE COMPONENTES E FOOTPRINTS

### 3.1 Microcontrolador

| Designador | Componente | Descricao | Footprint |
|------------|------------|-----------|-----------|
| U1 | Teensy 4.1 | Microcontrolador principal ARM Cortex-M7 | Modulo Teensy 4.1 |

### 3.2 Sensores I2C

| Designador | Componente | Descricao | Footprint | Endereco I2C |
|------------|------------|-----------|-----------|--------------|
| U2 | INA226 | Monitor de corrente/tensao | MSOP-10 | 0x40 |
| U3 | ICM-42688-P | IMU 6-DOF (Acelerometro + Giroscopio) | QFN-14 | 0x68 |
| U4 | LIS3MDL | Magnetometro 3 eixos | LGA-12 | 0x1C |
| U5 | BMP390 | Barometro/Altimetro | LGA-10 | 0x76 |
| U6 | ADS1115 | ADC 16-bit 4 canais | MSOP-10 | 0x48 |

### 3.3 Reguladores de Tensao

| Designador | Componente | Descricao | Entrada | Saida | Footprint |
|------------|------------|-----------|---------|-------|-----------|
| U7 | MP1584EN | Regulador DC-DC Step-Down | 12V | 5V | SOIC-8 |
| U8 | AMS1117-3.3 | Regulador LDO | 5V | 3.3V | SOT-223 |
| U12 | MP1584EN | Regulador DC-DC Step-Down (secundario) | 12V | 5V | SOIC-8 |

### 3.4 Circuitos de Protecao e Monitoramento

| Designador | Componente | Descricao | Footprint |
|------------|------------|-----------|-----------|
| U10 | Voltage Monitor | Monitor de tensao | SOT-23 |
| U11 | Crystal 32.768kHz | Cristal oscilador | HC-49S |
| D1 | SMBJ24A-TR | TVS Diode protecao ESD | SMB |
| D2 | SS34 | Diodo Schottky | SMA |
| D3 | SS34 | Diodo Schottky | SMA |

### 3.5 Conectores de Servo/PWM (3 pinos) - ATUALIZADOS

| Designador | Funcao | Footprint Original | Footprint Atualizado | LCSC Code |
|------------|--------|--------------------|--------------------|-----------|
| U13 (RX/TX11) | Servo Output 11 | SM03B-GHS-TB | CONN-TH_3P-P2.50_B3B-XH-A-BK-LF-SN | C144394 |
| U14 (RX/TX10) | Servo Output 10 | SM03B-GHS-TB | CONN-TH_3P-P2.50_B3B-XH-A-BK-LF-SN | C144394 |
| U15 (RX/TX9) | Servo Output 9 | SM03B-GHS-TB | CONN-TH_3P-P2.50_B3B-XH-A-BK-LF-SN | C144394 |
| U16 (RX/TX8) | Servo Output 8 | SM03B-GHS-TB | CONN-TH_3P-P2.50_B3B-XH-A-BK-LF-SN | C144394 |
| U17 (RX/TX7) | Servo Output 7 | SM03B-GHS-TB | CONN-TH_3P-P2.50_B3B-XH-A-BK-LF-SN | C144394 |
| U18 (RX/TX6) | Servo Output 6 | SM03B-GHS-TB | CONN-TH_3P-P2.50_B3B-XH-A-BK-LF-SN | C144394 |
| U19 (RX/TX5) | Servo Output 5 | SM03B-GHS-TB | CONN-TH_3P-P2.50_B3B-XH-A-BK-LF-SN | C144394 |
| U20 (RX/TX4) | Servo Output 4 | SM03B-GHS-TB | CONN-TH_3P-P2.50_B3B-XH-A-BK-LF-SN | C144394 |
| U21 (RX/TX3) | Servo Output 3 | SM03B-GHS-TB | CONN-TH_3P-P2.50_B3B-XH-A-BK-LF-SN | C144394 |
| U22 (RX/TX2) | Servo Output 2 | SM03B-GHS-TB | CONN-TH_3P-P2.50_B3B-XH-A-BK-LF-SN | C144394 |
| U23 (RX/TX1) | Servo Output 1 | SM03B-GHS-TB | CONN-TH_3P-P2.50_B3B-XH-A-BK-LF-SN | C144394 |

Pinagem dos conectores de servo (B3B-XH-A):
- Pino 1: GND
- Pino 2: VCC (5V)
- Pino 3: Sinal PWM

### 3.6 Conectores I2C (4 pinos) - ATUALIZADOS

| Designador | Funcao | Footprint Original | Footprint Atualizado | LCSC Code |
|------------|--------|--------------------|--------------------|-----------|
| P1 | I2C Port 1 | JST-4PIN | CONN-TH_B4B-XH-A-LF-SN | C144395 |
| P2 | I2C Port 2 | JST-4PIN | CONN-TH_B4B-XH-A-LF-SN | C144395 |
| P3 | I2C Port 3 | JST-4PIN | CONN-TH_B4B-XH-A-LF-SN | C144395 |
| P4 | I2C Port 4 | JST-4PIN | CONN-TH_B4B-XH-A-LF-SN | C144395 |
| P5 | I2C Port 5 | JST-4PIN | CONN-TH_B4B-XH-A-LF-SN | C144395 |
| P6 | I2C Port 6 | JST-4PIN | CONN-TH_B4B-XH-A-LF-SN | C144395 |
| P7 | I2C Port 7 | JST-4PIN | CONN-TH_B4B-XH-A-LF-SN | C144395 |
| P8 | I2C Port 8 | JST-4PIN | CONN-TH_B4B-XH-A-LF-SN | C144395 |

Pinagem dos conectores I2C (B4B-XH-A):
- Pino 1: GND
- Pino 2: VCC (3.3V)
- Pino 3: SDA
- Pino 4: SCL

### 3.7 Outros Conectores

| Designador | Componente | Descricao | Footprint |
|------------|------------|-----------|-----------|
| CN1 | Conector de Entrada | Entrada de alimentacao principal 12V | Conector Screw Terminal |
| P9 | Header 2x5 | Conector de expansao | PHD2.0mm-2X5 |

### 3.8 Componentes de Interface

| Designador | Componente | Descricao | Footprint |
|------------|------------|-----------|-----------|
| SW1 | Tactile Switch | Botao ARM | 6x6mm Tactile |
| SW2 | Tactile Switch | Botao Emergency Stop | 6x6mm Tactile |
| LED1 | WS2812B-5050 | LED RGB Status 1 | LED-SMD_5050 |
| LED2 | WS2812B-5050 | LED RGB Status 2 | LED-SMD_5050 |
| BUZZER1 | Buzzer 2700Hz | Buzzer piezoeletrico | BUZ-SMD_4P-L8.5 |

### 3.9 Transistores/MOSFETs

| Designador | Componente | Descricao | Footprint |
|------------|------------|-----------|-----------|
| Q1 | AO3400A | N-Channel MOSFET | SOT-23-3 |
| Q2 | AO3400A | N-Channel MOSFET | SOT-23-3 |

### 3.10 Resistores

| Designador | Valor | Descricao | Footprint |
|------------|-------|-----------|-----------|
| R1 | 10K | Pull-up/Pull-down | 0402 |
| R2 | 10K | Pull-up/Pull-down | 0402 |
| R3 | 10K | Pull-up/Pull-down | 0402 |
| R4 | 10K | Pull-up/Pull-down | 0402 |
| R5 | 10K | Pull-up/Pull-down | 0402 |
| R6 | 10K | Pull-up/Pull-down | 0402 |
| R7 | 10K | Pull-up/Pull-down | 0402 |
| R8 | 10K | Pull-up/Pull-down | 0402 |
| R9 | 4.7K | Pull-up I2C SDA | 0402 |
| R10 | 4.7K | Pull-up I2C SCL | 0402 |
| R11 | 1K | Resistor LED | 0402 |
| R12 | 1K | Resistor LED | 0402 |
| R13 | 100R | Resistor de protecao | 0402 |
| R14 | 100R | Resistor de protecao | 0402 |
| R15 | 100R | Resistor de protecao | 0402 |
| R16 | 100R | Resistor de protecao | 0402 |
| R17 | 0.1R | Resistor shunt para INA226 | 2512 |

### 3.11 Capacitores

| Designador | Valor | Descricao | Footprint |
|------------|-------|-----------|-----------|
| C1 | 10uF | Capacitor de desacoplamento | 0805 |
| C2 | 10uF | Capacitor de desacoplamento | 0805 |
| C3 | 10uF | Capacitor de desacoplamento | 0805 |
| C4 | 10uF | Capacitor de desacoplamento | 0805 |
| C5 | 100nF | Capacitor de bypass | 0402 |
| C6 | 100nF | Capacitor de bypass | 0402 |
| C7 | 100nF | Capacitor de bypass | 0402 |
| C8 | 100nF | Capacitor de bypass | 0402 |
| C9 | 100nF | Capacitor de bypass | 0402 |
| C10 | 100nF | Capacitor de bypass | 0402 |
| C11 | 100nF | Capacitor de bypass | 0402 |
| C12 | 100nF | Capacitor de bypass | 0402 |
| C13 | 100nF | Capacitor de bypass | 0402 |
| C14 | 100nF | Capacitor de bypass | 0402 |
| C15 | 100nF | Capacitor de bypass | 0402 |
| C16 | 1uF | Capacitor de filtragem | 0402 |
| C17 | 22uF | Capacitor regulador entrada | 0805 |
| C18 | 22uF | Capacitor regulador saida | 0805 |
| C19 | 47uF | Capacitor bulk entrada | 1206 |
| C20 | 47uF | Capacitor bulk saida | 1206 |

---

## 4. HISTORICO DE ALTERACOES

### 4.1 Alteracoes de Footprint

| Data | Componentes | Alteracao | Motivo |
|------|-------------|-----------|--------|
| Jan 2026 | U13-U23 (RX/TX1-11) | SM03B-GHS-TB para B3B-XH-A | Orientacao vertical para facilitar conexao de cabos pela parte superior |
| Jan 2026 | P1-P8 | JST-4PIN generico para B4B-XH-A | Footprint com modelo 3D e compativel com JLCPCB |

### 4.2 Alteracoes de Nomenclatura

| Componente Original | Novo Nome | Motivo |
|--------------------|-----------|--------|
| RX/TX1 | U23 | Padronizacao de nomenclatura |
| RX/TX2 | U22 | Padronizacao de nomenclatura |
| RX/TX3 | U21 | Padronizacao de nomenclatura |
| RX/TX4 | U20 | Padronizacao de nomenclatura |
| RX/TX5 | U19 | Padronizacao de nomenclatura |
| RX/TX6 | U18 | Padronizacao de nomenclatura |
| RX/TX7 | U17 | Padronizacao de nomenclatura |
| RX/TX8 | U16 | Padronizacao de nomenclatura |
| RX/TX9 | U15 | Padronizacao de nomenclatura |
| RX/TX10 | U14 | Padronizacao de nomenclatura |
| RX/TX11 | U13 | Padronizacao de nomenclatura |

---

## 5. LAYOUT DA PCB

### 5.1 Distribuicao de Areas

| Area | Localizacao | Componentes |
|------|-------------|-------------|
| Entrada de Energia | Borda esquerda superior | CN1, D1, U10 |
| Reguladores | Topo central-esquerdo | U7, U8, U12, C17-C20 |
| Microcontrolador | Centro-esquerda | U1 (Teensy) |
| Sensores I2C | Centro-esquerda | U2, U3, U4, U5, U6, U11 |
| Interface Usuario | Topo central | SW1, SW2, LED1, LED2, BUZZER1 |
| Conectores PWM | Centro | RX/TX1-11 (U13-U23) em grade 4x3 |
| Conectores I2C | Inferior central | P1-P8 em grade 4x2 |
| Conector Expansao | Borda direita | P9 |
| MOSFETs | Direita superior | Q1, Q2 |
| Resistores | Borda direita | R1-R17 |
| Capacitores | Borda inferior | C1-C16 |

### 5.2 Furos de Montagem

| Posicao | Coordenadas Aproximadas |
|---------|------------------------|
| Canto superior esquerdo | (5mm, 5mm) |
| Canto superior direito | (95mm, 5mm) |
| Canto inferior esquerdo | (5mm, 75mm) |
| Canto inferior direito | (95mm, 75mm) |

---

## 6. REDES DE ALIMENTACAO

### 6.1 Tensoes do Sistema

| Rede | Tensao | Fonte | Consumidores |
|------|--------|-------|--------------|
| VIN | 12V | Entrada externa | Reguladores |
| 5V | 5V | U7 (MP1584EN) | Servos, Teensy |
| 3V3 | 3.3V | U8 (AMS1117) | Sensores I2C, LEDs |
| GND | 0V | Referencia comum | Todos os componentes |

### 6.2 Barramentos

| Barramento | Sinais | Componentes Conectados |
|------------|--------|----------------------|
| I2C | SDA, SCL | U2, U3, U4, U5, U6, P1-P8 |
| PWM | PWM1-PWM11 | U13-U23 |
| SPI | MOSI, MISO, SCK, CS | Reservado |

---

## 7. CONSIDERACOES DE DESIGN

### 7.1 Orientacao dos Conectores

Todos os conectores de servo (U13-U23) e I2C (P1-P8) foram posicionados com a abertura voltada para CIMA, permitindo:
- Conexao de cabos pela parte superior da placa
- Facilidade de manutencao
- Acesso visual aos conectores durante operacao

### 7.2 Posicionamento de Componentes Criticos

- Capacitores de desacoplamento proximos aos pinos de alimentacao dos ICs
- Resistor shunt (R17) proximo ao INA226 (U2)
- Cristal (U11) proximo ao microcontrolador
- Reguladores afastados dos sensores para minimizar interferencia termica

### 7.3 Recomendacoes para Roteamento

- Trilhas de alimentacao: minimo 0.5mm de largura
- Trilhas de sinal: 0.25mm de largura
- Via termica sob reguladores
- Plano de terra continuo na camada inferior
- Evitar trilhas longas para sinais I2C

---

## 8. LISTA DE MATERIAIS (BOM) - CODIGOS LCSC ATUALIZADOS

### 8.1 ICs Principais

| Ref | LCSC | Componente | Footprint | Tipo |
|-----|------|------------|-----------|------|
| U1 | C2678753 | PCA9685PW,118 (PWM Driver 16ch) | TSSOP-28 | Extended |
| U2 | C37593 | ADS1115IDGSR (ADC 16-bit) | MSOP-10 | Extended |
| U3 | C1850418 | ICM-42688-P (IMU 6-axis) | LGA-14 | Extended |
| U4 | C478483 | LIS3MDLTR (Magnetometro) | LGA-12 | Extended |
| U5 | C9900016584 | BMP390 (Barometro) | LGA-10 | Extended |
| U6 | C49851 | INA226AIDGSR (Power Monitor) | MSOP-10 | Extended |
| U7 | C15051 | MP1584EN-LF-Z (Buck 3A) | SOIC-8 EP | Extended |
| U8 | C6186 | AMS1117-3.3 (LDO 3.3V) | SOT-223 | Basic |
| U10 | C9900007450 | PPTC 1.5A/13.2V (Fusivel) | 1206 | Extended |
| U11 | C17701336 | Crystal 24MHz | SMD 3225 | Extended |

### 8.2 Diodos e Transistores

| Ref | LCSC | Componente | Footprint | Tipo |
|-----|------|------------|-----------|------|
| D1 | C133668 | SMBJ24A-TR (TVS 24V) | SMB | Extended |
| D2 | C8678 | SS34 (Schottky 3A 40V) | SMA | Basic |
| D3 | C8678 | SS34 (Schottky 3A 40V) | SMA | Basic |
| Q1 | C20917 | AO3400A (MOSFET N-CH) | SOT-23 | Basic |
| Q2 | C20917 | AO3400A (MOSFET N-CH) | SOT-23 | Basic |

### 8.3 Resistores

| Ref | LCSC | Valor | Footprint | Tipo |
|-----|------|-------|-----------|------|
| R1-R8 | C25744 | 10kΩ | 0402 | Basic |
| R9-R12 | C25900 | 4.7kΩ | 0402 | Basic |
| R13-R16 | C2889360 | 330Ω | 0402 | Extended |
| R17 | C76272 | 0.01Ω 1W Shunt | 2512 | Extended |

### 8.4 Capacitores

| Ref | LCSC | Valor | Footprint | Tipo |
|-----|------|-------|-----------|------|
| C1-C4 | C15850 | 10uF 25V | 0805 | Basic |
| C5-C12 | C1525 | 100nF 50V | 0402 | Basic |
| C13-C16 | C52923 | 1uF 16V | 0402 | Basic |
| C17-C18 | C45783 | 22uF 25V | 0805 | Basic |
| C19-C20 | C5448950 | 47uF 10V | 1206 | Extended |

### 8.5 LEDs, Buzzer e Conectores

| Ref | LCSC | Componente | Footprint | Tipo |
|-----|------|------------|-----------|------|
| LED1-LED2 | C2838584 | WS2812B-5050RGB | 5050 | Extended |
| BUZZER1 | C94599 | MLT-8530 (2700Hz) | SMD 8.5x8.5 | Extended |
| CN1 | C5306499 | S4B-XH-SM4-TB(LF)(SN) | JST XH 4P | Extended |
| P9 | C49123 | PHD2.0mm-2X5 Header | THT 2x5 | Extended |

### 8.6 Resumo de Quantidades

| Categoria | Quantidade |
|-----------|------------|
| ICs | 11 |
| Diodos | 3 |
| Transistores | 2 |
| Resistores | 17 |
| Capacitores | 20 |
| LEDs | 2 |
| Buzzer | 1 |
| Conectores | 2 |
| **TOTAL SMT** | **58** |
| Teensy 4.1 (separado) | 1 |

### 8.7 Estimativa de Custos (USD)

| Item | Valor |
|------|-------|
| Basic Parts (35 unid) | ~$1.50 |
| Extended Parts (28 unid) | ~$25-30 |
| Taxa Extended (17 tipos x $3) | ~$51 |
| PCB (5 unidades) | ~$5-10 |
| Teensy 4.1 | ~$30 |
| **TOTAL** | **~$115-125** |

---

## 9. PROXIMOS PASSOS

| Etapa | Status | Descricao |
|-------|--------|-----------|
| 1. Esquematico | COMPLETO | Diagrama multifilar finalizado |
| 2. Conversao para PCB | COMPLETO | Importacao de componentes |
| 3. Atualizacao de Footprints | COMPLETO | U13-U23 e P1-P8 atualizados |
| 4. Posicionamento | COMPLETO | Layout conforme guia visual |
| 5. Auto-Router | COMPLETO | Roteamento das trilhas |
| 6. Planos de Cobre | COMPLETO | GND e VCC planes |
| 7. DRC | COMPLETO | 0 erros |
| 8. Gerber | COMPLETO | Arquivos gerados |
| 9. BOM LCSC | COMPLETO | Lista atualizada com codigos |

---

## 10. ARQUIVOS DO PROJETO

| Arquivo | Descricao |
|---------|-----------|
| SCH_PROJETO-AFC-(LAYOUT-ATUALIZADO-002)_2026-01-30.json | Esquematico EasyEDA |
| Schematic_PROJETO-AFC-(LAYOUT-ATUALIZADO-002)_2026-01-30.pdf | Esquematico PDF |
| PCB_PCB_PROJETO-AFC-(LAYOUT-ATUALIZADO-002)_2_2026-01-30.json | PCB EasyEDA |
| PCB_PCB_PROJETO-AFC-(LAYOUT-ATUALIZADO-002)_2_2026-01-30.kicad_pcb | PCB KiCad |
| PCB_PCB_PROJETO-AFC-(LAYOUT-ATUALIZADO-002)_2_2026-01-30.pdf | PCB PDF |
| Gerber_PROJETO-AFC-...2026-01-30.zip | Arquivos Gerber para JLCPCB |
| BOM_AFC_TEENSY_LCSC.csv | Lista de materiais com codigos LCSC |
| AFC_TEENSY_PCB_DOCUMENTACAO.md | Esta documentacao |
| PLACA AFC FINAL 0 ERROS.png | Screenshot DRC aprovado |

---

## 11. INFORMACOES DE CONTATO E REVISAO

| Campo | Valor |
|-------|-------|
| Projetista | [Nome do Projetista] |
| Revisao | 1.0 |
| Data da Documentacao | Janeiro 2026 |
| Ultima Atualizacao | 30/01/2026 |

---

## NOTAS ADICIONAIS

1. Os footprints B3B-XH-A e B4B-XH-A sao conectores JST XH series, amplamente disponiveis e compativeis com JLCPCB SMT assembly.

2. Os conectores foram especificamente escolhidos para ter orientacao vertical, facilitando a conexao de cabos externos.

3. O layout foi inspirado na placa Navigator da BlueRobotics, otimizado para aplicacoes de ROV.

4. Todos os componentes possuem codigos LCSC validos para fabricacao via JLCPCB.

---

FIM DO DOCUMENTO
