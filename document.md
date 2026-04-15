www.ti.com

TPS54302
TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

TPS54302 4.5-V to 28-V Input, 3-A Output, EMI-Friendly
Synchronous Step-Down Converter

1 Features

3 Description

• 4.5-V to 28-V wide input voltage range
•

Integrated 85-mΩ and 40-mΩ MOSFETs for 3-A,
continuous output current

Internal 5-ms soft start

• Low 2-μA shutdown, 45-μA quiescent current
•
• Fixed 400-kHz switching frequency
• Frequency spread spectrum to reduce EMI
• Advanced Eco-mode™ pulse skip
• Peak current-mode control
•
Internal loop compensation
• Overcurrent protection for both MOSFETs with

hiccup mode protection
• Overvoltage protection
• Thermal shutdown
• SOT-23 (6) package

2 Applications

• 12-V, 24-V distributed power-bus supply
•

Industry application
– White goods

• Consumer application

– Audio
– STB, DTV
– Printer

The TPS54302 device is a 4.5-V to 28-V input voltage
range,  3-A  synchronous  buck  converter.  The  device
includes  two  integrated  switching  FETs,  internal  loop
compensation,  and  5-ms  internal  soft  start  to  reduce
component count.

By  integrating  the  MOSFETs  and  employing  the
SOT-23 package, the TPS54302 device achieves the
high power density and offers a small footprint on the
PCB.

Advanced  Eco-mode  implementation  maximizes  the
light load efficiency and reduces the power loss.

the  TPS54302  device,

In
spectrum operation is introduced for EMI reduction.

frequency  spread

the

Cycle-by-cycle current limit in both high-side MOSFET
protects  the  converter  in  an  overload  condition  and
is  enhanced  by  a  low-side  MOSFET  freewheeling
current  limit  which  prevents  current  runaway.  Hiccup
the  overcurrent
triggered
mode  protection
condition  has  persisted  for  longer  than  the  present
time.

is

if

PART NUMBER

Device Information
PACKAGE(1)

BODY SIZE (NOM)

TPS54302

SOT-23-THIN (6)

1.60 mm × 2.90 mm

(1)

For all available packages, see the orderable addendum at

the end of the data sheet.

Simplified Schematic

Efficiency vs Output Current

Copyright © 2021 Texas Instruments Incorporated

An IMPORTANT NOTICE at the end of this data sheet addresses availability, warranty, changes, use in safety-critical applications,
Submit Document Feedback
intellectual property matters and other important disclaimers. PRODUCTION DATA.

1

Product Folder Links: TPS54302

TPS54302VINENGNDBOOTFBSWVINVOUTENLO315246CINCBOOTRFB1RFB2COCopyright © 2017, Texas Instruments IncorporatedOutput Current (A)Efficiency (%)01020304050607080901000.0010.010.11D100VIN = 12 V, VOUT = 5 VVIN = 12 V, VOUT = 3.3 VVIN = 24 V, VOUT = 5 VVIN = 24 V, VOUT = 3.3 VTPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

www.ti.com

Table of Contents

1 Features............................................................................1
2 Applications..................................................................... 1
3 Description.......................................................................1
4 Revision History.............................................................. 2
5 Pin Configuration and Functions...................................3
6 Specifications.................................................................. 4
6.1 Absolute Maximum Ratings........................................ 4
6.2 ESD Ratings............................................................... 4
6.3 Recommended Operating Conditions.........................4
6.4 Thermal Information....................................................4
6.5 Electrical Characteristics.............................................5
6.6 Timing Requirements.................................................. 5
6.7 Typical Characteristics................................................ 6
7 Detailed Description........................................................8
7.1 Overview..................................................................... 8
7.2 Functional Block Diagram........................................... 9
7.3 Feature Description.....................................................9

7.4 Device Functional Modes..........................................13
8 Application and Implementation.................................. 14
8.1 Application Information............................................. 14
8.2 Typical Application.................................................... 14
9 Power Supply Recommendations................................21
10 Layout...........................................................................22
10.1 Layout Guidelines................................................... 22
10.2 Layout Example...................................................... 22
11 Device and Documentation Support..........................23
11.1 Device Support........................................................23
11.2 Receiving Notification of Documentation Updates.. 23
11.3 Support Resources................................................. 23
11.4 Trademarks............................................................. 23
11.5 Electrostatic Discharge Caution.............................. 23
11.6 Glossary.................................................................. 23

12 Mechanical, Packaging, and Orderable

Information.................................................................... 23

4 Revision History
NOTE: Page numbers for previous revisions may differ from page numbers in the current version.

Changes from Revision A (May 2016) to Revision B (April 2021)
Page
• Updated the numbering format for tables, figures, and cross-references throughout the document. ................1

Changes from Revision * (May 2016) to Revision A (May 2016)
Page
• Changed from Product Preview to Production Data .......................................................................................... 1

2

Submit Document Feedback

Copyright © 2021 Texas Instruments Incorporated

Product Folder Links: TPS54302

www.ti.com

5 Pin Configuration and Functions

TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

Figure 5-1. DDC Package 6-Pin SOT-23-THIN Top View

Table 5-1. Pin Functions

DESCRIPTION

Supply input for the high-side NFET gate drive circuit. Connect a 0.1-μF capacitor between BOOT and
SW pins.

This pin is the enable pin. Float the EN pin to enable.

Converter feedback input. Connect to output voltage with feedback resistor divider.

Ground pin Source terminal of low-side power NFET as well as the ground terminal for controller circuit.
Connect sensitive VFB to this GND at a single point.

Switch node connection between high-side NFET and low-side NFET.

Input voltage supply pin. The drain terminal of high-side power NFET.

PIN

NAME

NO.

TYPE(1)

BOOT

EN

FB

GND

SW

VIN

6

5

4

1

2

3

O

I

I

—

O

—

(1) O = output; I = input

Copyright © 2021 Texas Instruments Incorporated

Submit Document Feedback

3

Product Folder Links: TPS54302

1GND6 BOOT2SW5 EN3VIN4 FBTPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

6 Specifications
6.1 Absolute Maximum Ratings

over operating free-air temperature range (unless otherwise noted)(1)

Input voltage, VI

Output voltage, VO

Operating junction temperature, TJ

Storage temperature, Tstg

VIN

EN

FB

BOOT-SW

SW

SW (20 ns transient)

www.ti.com

MIN

–0.3

–0.3

–0.3

–0.3

–0.3

–5

–40

–65

MAX

UNIT

30

7

7

7

30

30

150

150

V

V

V

V

V

V

°C

°C

(1)

Stresses beyond those listed under Absolute Maximum Ratings may cause permanent damage to the device. These are stress

ratings only, which do not imply functional operation of the device at these or any other conditions beyond those indicated under
Recommended Operating Conditions. Exposure to absolute-maximum-rated conditions for extended periods may affect device

reliability.

6.2 ESD Ratings

V(ESD)

Electrostatic
discharge

Human-body model (HBM), per ANSI/ESDA/JEDEC JS-001(1)

Charged-device model (CDM), per JEDEC specification JESD22-C101(2)

VALUE

UNIT

±4000

±1500

V

(1)

(2)

JEDEC document JEP155 states that 500-V HBM allows safe manufacturing with a standard ESD control process.

JEDEC document JEP157 states that 250-V CDM allows safe manufacturing with a standard ESD control process.

6.3 Recommended Operating Conditions

over operating free-air temperature range (unless otherwise noted)

Input voltage

Output voltage

VIN

EN

FB

BOOT-SW

SW

Operating junction temperature

VI

VO

TJ

6.4 Thermal Information

THERMAL METRIC(1)

RθJA

RθJC(top)

RθJB

ψJT

ψJB

Junction-to-ambient thermal resistance

Junction-to-case (top) thermal resistance

Junction-to-board thermal resistance

Junction-to-top characterization parameter

Junction-to-board characterization parameter

MIN

4.5

–0.1

–0.1

–0.1

–0.1

–40

MAX

UNIT

28

7

7

7

28

125

V

V

V

V

V

°C

TPS54302

DDC (SOT-23)

UNIT

6 PINS

87.1

35.5

14.4

0.9

14.2

°C/W

°C/W

°C/W

°C/W

°C/W

(1)

For more information about traditional and new thermal metrics, see the Semiconductor and IC Package Thermal Metrics application
report.

4

Submit Document Feedback

Copyright © 2021 Texas Instruments Incorporated

Product Folder Links: TPS54302

www.ti.com

6.5 Electrical Characteristics

TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

The electrical ratings specified in this section apply to all specifications in this document, unless otherwise noted. These
specifications are interpreted as conditions that do not degrade the device parametric or functional specifications for the life
of the product containing it. TJ = –40°C to +125°C, VIN = 4.5 V to 28 V, (unless otherwise noted).

PARAMETER

TEST CONDITIONS

MIN

TYP

MAX UNIT

INPUT SUPPLY

Input voltage range

Non switching quiescent current

EN = 5 V, VFB = 1 V

VIN

IQ

IOFF

VIN(UVLO)

Shut down current

VIN under voltage lockout

Hysteresis

ENABLE (EN PIN)

VENrising

VENfalling

Enable threshold

I(EN_INPUT)

Input current

I(EN_HYS)

Hysteresis current

FEEDBACK AND ERROR AMPLIFIER

VFB

Feedback Voltage

EN = GND

Rising VIN

Falling VIN

Rising

Falling

VEN = 1 V

VEN = 1.5 V

VIN = 12 V

4.5

3.8

3.3

400

1.1

28

4.4

3.9

V

µA

µA

V

V

45

2

4.1

3.6

480

560 mV

1.21

1.19

0.7

1.55

1.28

V

V

μA

μA

0.581

0.596

0.611

V

PULSE SKIP MODE
I(SKIP) (1)
POWER STAGE

Pulse skip mode peak inductor current threshold VIN = 12 V, VOUT = 5 V, L = 10 µH

R(HSD)

R(LSD)

High-side FET on resistance

Low-side FET on resistance

CURRENT LIMIT

TA = 25°C, VBST – SW = 6 V

TA = 25°C, VIN = 12

I(LIM_HS)

I(LIM_LS)

OSCILLATOR

High-side current limit

Maximum inductor peak current

Low-side source current limit

Maximum inductor valley current

4

3.1

500

85

40

5

4

mA

mΩ

mΩ

5.9

5.5

A

A

fSW

Centre switching frequency

OVERTEMPERATURE PROTECTION

Rising temperature

Thermal
Shutdown(1)

Hysteresis

Hiccup time

(1) Not production tested

6.6 Timing Requirements

OVERCURRENT PROTECTION

Hiccup wait time

Hiccup time before restart

Soft-start time

tHIC_WAIT

tHIC_RESTART

tSS

ON TIME CONTROL

tMIN_ON (1)

(1) Not production tested

290

400

510

kHz

165

10

32768

°C

°C

Cycles

MIN

NOM

MAX

UNIT

512

16384

5

Cycles

Cycles

ms

Minimum on time, measured at 90% to 90% and 1-A
loading

110

ns

Copyright © 2021 Texas Instruments Incorporated

Submit Document Feedback

5

Product Folder Links: TPS54302

TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

6.7 Typical Characteristics

VIN = 12, unless otherwise specified

www.ti.com

Figure 6-1. Shutdown Quiescent Current vs
Junction Temperature

Figure 6-2. Non-Switching Operating Quiescent
Current vs Junction Temperature

Figure 6-3. High-Side Resistance vs Junction
Temperature

Figure 6-4. Low-Side FET On Resistance vs
Junction Temperature

Figure 6-5. Reference Voltage vs Junction
Temperature

Figure 6-6. Centre Switching Frequency vs
Junction Temperature

6

Submit Document Feedback

Copyright © 2021 Texas Instruments Incorporated

Product Folder Links: TPS54302

Junction Temperature (qC)Shutdown Quiescent Current (PA)-50-25025507510012500.511.522.5D001Junction Temperature (qC)Non-Switching Operating Quiescent Current (PA)-50-25025507510012520406080D002Junction Temperature (qC)High side FET Rds(on) (m:)-50-250255075100125406080100120140160180200220240D003Junction Temperature (qC)Low side FET Rds(on) (m:)-50-25025507510012520304050607080D004Junction Temperature (qC)Reference Voltage (mV)-50-2502550751001250.5900.5920.5940.5960.5980.600D005Junction Temperature (qC)Switching Frequency (kHz)-50-250255075100125380385390395400405410415420D006www.ti.com

TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

Figure 6-7. High-Side Current Limit Threshold vs
Junction Temperature

Figure 6-8. Low-Side Current Limit Threshold vs
Junction Temperature

Figure 6-9. BOOT-SW UVLO Threshold vs Junction
Temperature

Figure 6-10. VIN UVLO Threshold vs Junction
Temperature

Figure 6-11. EN Threshold vs Junction
Temperature

Figure 6-12. EN Hysteresis Current vs Junction
Temperature

Copyright © 2021 Texas Instruments Incorporated

Submit Document Feedback

7

Product Folder Links: TPS54302

Junction Temperature (qC)High Side Current Limit (A)-50-2502550751001252.83.33.84.34.85.35.8D007Junction Temperature (qC)Low Side Current Limit (A)-50-2502550751001253.13.33.53.73.94.14.3D008Junction Temperature (qC)BOOT UVLO Threshold (V)-50-2502550751001252.002.052.102.152.20D009Junction Temperature (qC)VIN UVLO Threshold (V)-50-2502550751001253.33.53.73.94.14.34.5D010L->HH->LJunction Temperature (qC)EN UVLO Threshold (V)-50-2502550751001251.11.141.181.221.261.3D011L->HH->LJunction Temperature (qC)EN Hysteresis Current (PA)-50-2502550751001251.401.451.501.551.601.651.70D012TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

7 Detailed Description
7.1 Overview

www.ti.com

The  TPS54302  device  is  a  28-V,  3-A,  synchronous  step-down  (buck)  converter  with  two  integrated  n-channel
MOSFETs. To improve performance during line and load transients the device implements a constant-frequency,
peak  current-mode  control  which  reduces  output  capacitance.  The  optimized  internal  compensation  network
minimizes the external component counts and simplifies the control loop design.

The switching frequency of the device is fixed to 400 kHz.

The  TPS54302  device  starts  switching  when  VIN  is  4.5  V.  The  operating  current  is  45  μA  (typical)  when  not
switching and under no load. When the device is disabled, the supply current is 2 µA (typical).

The integrated 85-mΩ high-side MOSFET and 40-mΩ low-side MOSFET allow for high-efficiency power-supply
designs with continuous output currents up to 3 A.

The TPS54302 device reduces the external component count by integrating the boot recharge diode. The bias
voltage for the integrated high-side MOSFET is supplied by an external capacitor on the BOOT to PH pins. The
boot capacitor voltage is monitored by an UVLO circuit and turns off the high-side MOSFET when the voltage
falls below a preset threshold of 2.1 V (typical).

The  device  minimizes  excessive  output  overvoltage  transients  by  taking  advantage  of  the  overvoltage
comparator.  When  the  regulated  output  voltage  is  greater  than  108%  of  the  nominal  voltage,  the  overvoltage
comparator  is  activated,  and  the  high-side  MOSFET  is  turned  off  and  masked  from  turning  on  until  the  output
voltage is lower than 104%.

The TPS54302 device has internal 5-ms soft-start time to minimize inrush currents.

8

Submit Document Feedback

Copyright © 2021 Texas Instruments Incorporated

Product Folder Links: TPS54302

www.ti.com

7.2 Functional Block Diagram

TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

7.3 Feature Description
7.3.1 Fixed-Frequency PWM Control

The device uses a fixed-frequency, peak current-mode control. The output voltage is compared through external
resistors on the FB pin to an internal voltage reference by an error amplifier. An internal oscillator initiates the
turnon  of  the  high-side  power  switch.  The  error  amplifier  output  is  compared  to  the  current  of  the  high-side
power  switch.  When  the  power-switch  current  reaches  the  error  amplifier  output  voltage  level,  the  high-side
power  switch  is  turned  off  and  the  low-side  power  switch  is  turned  on.  The  error  amplifier  output  voltage
increases and decreases as the output current increases and decreases. The device implements a current-limit
by clamping the error amplifier voltage to a maximum level and also implements a minimum clamp for improved
transient-response performance.

7.3.2 Pulse Skip Mode

The  TPS54302  device  is  designed  to  operate  in  pulse-skipping  mode  at  light-load  currents  to  boost  light-load
efficiency.  When  the  peak  inductor  current  is  lower  than  500  mA  (typical),  the  device  enters  pulse-skipping
mode. When the device is in pulse-skipping mode, the error amplifier output voltage is clamped which prevents
the high-side integrated MOSFET from switching. The peak inductor current must rise above 500 mA and exit

Copyright © 2021 Texas Instruments Incorporated

Submit Document Feedback

9

Product Folder Links: TPS54302

FBVoltage ReferenceHS MOSFET Current ComparatorSlope CompensationOverloadRecoveryMaximumClampOscillatorPower Stageand Dead TimeControl LogicLS MOSFETCurrent LimitMaximum Clamp Pulse SkipOvervoltage ComparatorBoot UVLORegulatorVINBoot ChargeGNDBOOTSWCurrent SenseCurrent SenseINIhIpENEnable ComparatorShutdownLogicThermal HiccupUVLOHiccup ShutdownHiccup Shutdown+±+±+Soft Start2.04 nF20 k(cid:13)ErrorAmplifier2 pFCopyright © 2017, Texas Instruments IncorporatedTPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

www.ti.com

pulse skip mode. Because the integrated current comparator catches the peak inductor current only, the average
load current entering pulse-skipping mode varies with the applications and external output filters.

7.3.3 Error Amplifier

The device has a transconductance amplifier as the error amplifier. The error amplifier compares the FB voltage
to the lower of the internal soft-start voltage or the internal 0.596-V voltage reference. The transconductance of
the error amplifier is 240 µA/V (typical). The frequency compensation components are placed internal between
the output of the error amplifier and ground.

7.3.4 Slope Compensation and Output Current

The  device  adds  a  compensating  ramp  to  the  signal  of  the  switch  current.  This  slope  compensation  prevents
sub-harmonic oscillations as the duty cycle increases. The available peak inductor current remains constant over
the full duty-cycle range.

7.3.5 Enable and Adjusting Undervoltage Lockout

The EN pin provides electrical on and off control of the device. When the EN pin voltage exceeds the threshold
voltage,  the  device  begins  operation.  If  the  EN  pin  voltage  is  pulled  below  the  threshold  voltage,  the  regulator
stops switching and enters the low-quiescent (IQ) state.

The EN pin has an internal pullup-current source which allows the user to float the EN pin to enable the device.
If an application requires control of the EN pin, use open-drain or open-collector output logic to interface with the
pin.

The  device  implements  internal  undervoltage-lockout  (UVLO)  circuitry  on  the  VIN  pin.  The  device  is  disabled
when the VIN pin voltage falls below the internal VIN UVLO threshold. The internal VIN UVLO threshold has a
hysteresis of 480 mV.

If an application requires a higher UVLO threshold on the VIN pin, then the EN pin can be configured as shown
in Figure 7-1. When using the external UVLO function, setting the hysteresis at a value greater than 500 mV is
recommended.

The  EN  pin  has  a  small  pullup  current,  Ip,  which  sets  the  default  state  of  the  pin  to  enable  when  no  external
components  are  connected.  The  pullup  current  is  also  used  to  control  the  voltage  hysteresis  for  the  UVLO
function because it increases by Ih when the EN pin crosses the enable threshold. Use Equation 1 and Equation
2 to calculate the values of R4 and R5 for a specified UVLO threshold.

10

Submit Document Feedback

Copyright © 2021 Texas Instruments Incorporated

Product Folder Links: TPS54302

www.ti.com

TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

Figure 7-1. Adjustable VIN Undervoltage Lockout

where

Ip = 0.7 µA
•
Ih = 1.55 µA
•
• VENfalling = 1.19 V
• VENrising = 1.22 V

(1)

(2)

7.3.6 Safe Startup into Pre-Biased Outputs

The  device  has  been  designed  to  prevent  the  low-side  MOSFET  from  discharging  a  prebiased  output.  During
monotonic  prebiased  startup,  both  high-side  and  low-side  MOSFETs  are  not  allowed  to  be  turned  on  until  the
internal soft-start voltage is higher than FB pin voltage.

7.3.7 Voltage Reference

The  voltage  reference  system  produces  a  precise  ±2.5%  voltage-reference  over  temperature  by  scaling  the
output of a temperature stable band-gap circuit. The typical voltage reference is designed at 0.596 V.

7.3.8 Adjusting Output Voltage

The output voltage is set with a resistor divider from the output node to the FB pin. TI recommends using divider
resistors with 1% tolerance or better. Start with 100 kΩ for the upper resistor divider, use Equation 3 to calculate
the output voltage. To improve efficiency at light loads consider using larger value resistors. If the values are too
high the regulator is more susceptible to noise and voltage errors from the FB input current are noticeable.

(3)

Copyright © 2021 Texas Instruments Incorporated

Submit Document Feedback

11

Product Folder Links: TPS54302

DeviceENIpVINR4R5IhENfallingSTARTSTOPENrisingENfallingphENrisingVVVVR4VI1IVæö-ç÷ç÷èø=æö-+ç÷ç÷èø()ENfallingSTOPENfallingphR4VR5VVR4II´=-++OUTrefR2VV1R3ªº u(cid:14)«»¬¼TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

7.3.9 Internal Soft-Start

www.ti.com

The TPS54302 device uses the internal soft-start function. The internal soft start time is set to 5 ms (typical).

7.3.10 Bootstrap Voltage (BOOT)

The  TPS54302  device  has  an  integrated  boot  regulator  and  requires  a  0.1-µF  ceramic  capacitor  between  the
BOOT  and  SW  pins  to  provide  the  gate-drive  voltage  for  the  high-side  MOSFET.  A  ceramic  capacitor  with
an  X7R  or  X5R  grade  dielectric  is  recommended  because  of  the  stable  characteristics  over  temperature  and
voltage. To improve drop out, the TPS54302 device is designed to operate at 100% duty cycle as long as the
BOOT to SW pin voltage is greater than 2.1 V (typical).

7.3.11 Overcurrent Protection

The  device  is  protected  from  overcurrent  conditions  by  cycle-by-cycle  current  limiting  on  both  the  high-side
MOSFET and the low-side MOSFET.

7.3.11.1 High-Side MOSFET Overcurrent Protection

The device implements current-mode control which uses the internal COMP voltage to control the turnoff of the
high-side  MOSFET  and  the  turnon  of  the  low-side  MOSFET  on  a  cycle-by-cycle  basis.  During  each  cycle,  the
switch current and the current reference generated by the internal COMP voltage are compared. When the peak
switch current intersects the current reference the high-side switch turns off.

7.3.11.2 Low-Side MOSFET Overcurrent Protection

While  the  low-side  MOSFET  is  turned  on,  the  conduction  current  is  monitored  by  the  internal  circuitry.  During
normal operation the low-side MOSFET sources current to the load. At the end of every clock cycle, the low-side
MOSFET sourcing current  is  compared to the internally set low-side sourcing current-limit. The inductor valley
current is exceeded the low-side source current limit, the high-side MOSFET does not turn on and the low-side
MOSFET stays on for the next cycle. The high-side MOSFET turns on again when the inductor valley current is
below the low-side sourcing current-limit at the start of a cycle as shown in Figure 7-2.

t = 1 / fSW

Figure 7-2. Overcurrent Protection for Both MOSFETs

12

Submit Document Feedback

Copyright © 2021 Texas Instruments Incorporated

Product Folder Links: TPS54302

I(LIM_HS)I(LIM_LS)ILHigh-SideMOS FETLow-SideMOS FETSkip pulse when IL is higher than I(LIM_LS)Skip pulse when IL is higher than I(LIM_LS)ttttwww.ti.com

TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

Furthermore, if an output overload condition occurs for more than the hiccup wait time, which is programmed for
512 switching cycles, the device shuts down and restarts after the hiccup time of 16384 cycles. The hiccup mode
helps to reduce the device power dissipation under severe overcurrent conditions.

7.3.12 Spread Spectrum

To  reduce  EMI,  the  TPS54302  device  introduces  frequency  spread  spectrum.  The  jittering  span  is  ±6%  of  the
switching frequency with 1/512 swing frequency.

7.3.13 Output Overvoltage Protection (OVP)

The  TPS54302  incorporates  an  overvoltage  transient  protection  (OVTP)  circuit  to  minimize  output  voltage
overshoot when recovering from output fault conditions or strong unload transients. The OVTP circuit includes
an overvoltage comparator to compare the FB pin voltage and internal thresholds. When the FB pin voltage goes
above 108% × Vref, the high-side MOSFET is forced off. When the FB pin voltage falls below 104% × Vref, the
high-side MOSFET is enabled again.

7.3.14 Thermal Shutdown

The internal thermal-shutdown circuitry forces the device to stop switching if the junction temperature exceeds
165°C  (typical).  When  the  junction  temperature  drops  below  155°C  (typical),  the  internal  thermal-hiccup  timer
begins  to  count.  The  device  reinitiates  the  power-up  sequence  after  the  built-in  thermal-shutdown  hiccup  time
(32768 cycles) is over.

7.4 Device Functional Modes
7.4.1 Normal Operation

When  the  input  voltage  is  above  the  UVLO  threshold,  the  TPS54302  device  can  operate  in  normal  switching
modes. Normal continuous conduction mode (CCM) occurs when inductor peak current is above 0 A. In CCM,
the TPS54302 device operates at a fixed frequency.

7.4.2 Eco-mode™ Operation

The  device  is  designed  to  operate  in  high-efficiency  pulse-skipping  mode  under  light-load  conditions.  Pulse
skipping initiates when the switch current falls to 500 mA (typical). During pulse skipping, the low-side FET turns
off when the switch current falls to 0 A. The switching node (the SW pin) waveform takes on the characteristics
of  discontinuous  conduction  mode  (DCM)  operation  and  the  apparent  switching  frequency  decreases.  As  the
output current decreases, the perceived time between switching pulses increases.

Copyright © 2021 Texas Instruments Incorporated

Submit Document Feedback

13

Product Folder Links: TPS54302

TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

8 Application and Implementation

www.ti.com

Note

Information  in  the  following  applications  sections  is  not  part  of  the  TI  component  specification,
and  TI  does  not  warrant  its  accuracy  or  completeness.  TI’s  customers  are  responsible  for
determining suitability of components for their purposes, as well as validating and testing their design
implementation to confirm system functionality.

8.1 Application Information

The TPS54302 device is typically used as a step-down converter, which converts an input voltage from 8 V to 28
V to a fixed output voltage of 5 V.

8.2 Typical Application
8.2.1 TPS54302 8-V to 28-V Input, 5-V Output Converter

Figure 8-1. 5-V, 3-A Reference Design

8.2.2 Design Requirements

For this design example, use the parameters in Table 8-1.

Table 8-1. Design Parameters

PARAMETER

Input voltage range

Output voltage

Output current

Transient response, 1.5-A load step

Input ripple voltage

Output voltage ripple

Switching frequency

VALUE

8 V to 28 V

5 V

3 A

ΔVOUT = ±5 %

400 mV

30 mVPP

400 kHz

14

Submit Document Feedback

Copyright © 2021 Texas Instruments Incorporated

Product Folder Links: TPS54302

VINENGNDBOOTFBSWVINVOUTL110 µH315246C110 µFC30.1 µFR149.9 (cid:13)R313.3 k(cid:13)C675 pFU1TPS54302VIN = 8 V to ~28 VC20.1 µFR4511 k(cid:13)R5105 k(cid:13)R2100 k(cid:13)C422 µFC522 µFVOUT = 5 V, 3 ACopyright © 2017, Texas Instruments Incorporatedwww.ti.com

8.2.3 Detailed Design Procedure

8.2.3.1 Input Capacitor Selection

TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

The device requires an input decoupling capacitor and a bulk capacitor is needed depending on the application.
A  ceramic  capacitor  over  10  µF  is  recommended  for  the  decoupling  capacitor.  An  additional  0.1-µF  capacitor
(C2)  from  the  VIN  pin  to  GND  is  optional  to  provide  additional  high  frequency  filtering.  The  capacitor  voltage
rating must be greater than the maximum input voltage.

Use Equation 4 to calculate the input ripple voltage (ΔVIN).

(4)

where

• CBULK is the bulk capacitor value.
fSW is the switching frequency.
•
IOUT(MAX) is the maximum loading current.
•
• ESRMAX is maximum series resistance of the bulk capacitor.

The  maximum  RMS  (root  mean  square)  ripple  current  must  also  be  checked.  For  worst  case  conditions,  use
Equation 5 to calculate ICIN(RMS).

(5)

The  actual  input-voltage  ripple  is  greatly  affected  by  parasitic  associated  with  the  layout  and  the  output
impedance  of  the  voltage  source.  The  Section  8.2.2  show  the  actual  input  voltage  ripple  for  this  circuit  which
is  larger  than  the  calculated  value.  This  measured  value  is  still  below  the  specified  input  limit  of  400  mV.  The
maximum voltage across the input capacitors is VINmax + ΔVIN / 2. The selected bypass capacitor is rated for 35
V and the ripple current capacity is greater than 2 A. Both values provide ample margin. The maximum ratings
for voltage and current must not be exceeded under any circumstance.

8.2.3.2 Bootstrap Capacitor Selection

A  0.1-µF  ceramic  capacitor  must  be  connected  between  the  BOOT  to  SW  pin  for  proper  operation.  TI
recommends using a ceramic capacitor.

8.2.3.3 Output Voltage Set Point

The  output  voltage  of  the  TPS54302  device  is  externally  adjustable  using  a  resistor  divider  network.  In  the
application circuit of Figure 8-1, this divider network comprises R2 and R3. Use Equation 6 and Equation 7 to
calculate the relationship of the output voltage to the resistor divider.

Select a value of R2 to be approximately 100 kΩ. Slightly increasing or decreasing the value of R3 can result in
closer output voltage matching when using standard value resistors. In this design, R2 = 100 kΩ and R3 = 13.3
kΩ which results in a 5-V output voltage. The 49.9-Ω resistor, R1, is provided as a convenient location to break
the control loop for stability testing.

(6)

(7)

Copyright © 2021 Texas Instruments Incorporated

Submit Document Feedback

15

Product Folder Links: TPS54302

()()()OUTMAXINMAXOUTMAXBULKswI 0.25VIESRCf´D=+´´OUT(MAX)CIN(RMS)II2 refOUTrefR2VR3VV´=-OUTrefR2VV1R3ªº u(cid:14)«»¬¼TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

8.2.3.4 Undervoltage Lockout Set Point

www.ti.com

The  undervoltage  lockout  (UVLO)  set  point  can  be  adjusted  using  the  external-voltage  divider  network  of  R4
and R5. The R4 resistor is connected between the VIN and EN pins of the TPS54302 device. The R5 resistor
is connected between the EN and GND pins. The UVLO has two thresholds, one for power up when the input
voltage is rising and one for power down or brownouts when the input voltage is falling. For the example design,
the minimum input voltage is 8 V, so the start voltage threshold is set to 6.74 V and the stop voltage threshold is
set to 5.83 V. Use Equation 1 and Equation 2 to calculate the values for the upper and lower resistor values of
R4 and R5.

8.2.3.5 Output Filter Components

Two components must be selected for the output filter: the output inductor (LO) and CO.

8.2.3.5.1 Inductor Selection

Use Equation 8 to calculate the minimum value of the output inductor (LMIN).

(8)

where

• KIND is a coefficient that represents the amount of inductor ripple current relative to the maximum output

current.

In general, the value of KIND is at the discretion of the designer; however, the following guidelines may be used.
For designs using low-ESR output capacitors, such as ceramics, a higher KIND can be used. When using higher
ESR output capacitors, KIND = 0.2 yields better results.

For this design example, use KIND = 0.35. The minimum inductor value is calculated as 9.78 μH. For this design,
a close standard value of 10 μH was selected for LMIN.

For  the  output  filter  inductor,  the  RMS  current  and  saturation  current  ratings  must  not  be  exceeded.  Use
Equation 9 to calculate the RMS inductor current (IL(RMS)).

Use Equation 10 to calculate the peak inductor current (IL(PK)).

(9)

(10)

Smaller or larger inductor values can be used depending on the amount of ripple current the designer wants to
allow so long as the other design requirements are met. Larger value inductors have lower AC current and result
in lower output voltage ripple. Smaller inductor values increase AC current and output voltage ripple.

8.2.3.5.2 Output Capacitor Selection

Consider three primary factors when selecting the value of the output capacitor. The output capacitor determines
the modulator pole, the output voltage ripple, and how the regulator responds to a large change in load current.
The output capacitance must be selected based on the more stringent of these three criteria.

The desired response to a large change in the load current is the first criterion. The output capacitor must supply
the load with current when the regulator cannot. This situation occurs if the desired hold-up times are present for

16

Submit Document Feedback

Copyright © 2021 Texas Instruments Incorporated

Product Folder Links: TPS54302

()()()OUTOUTINMAXINDOUTswINMINMAXVVVVfLKI´-=´´´(cid:11)(cid:12)(cid:11)(cid:12)(cid:11)(cid:12)(cid:11)(cid:12)2OUTOUTINMAX2OUTMAXOSWINMAL(AXXM)VVV1I12VLf0.8I§·u(cid:16)¨¸ (cid:14)u¨¸uuu¨¸©¹(cid:11)(cid:12)(cid:11)(cid:12)(cid:11)(cid:12)(cid:11)(cid:12)OUTOUTINMAL(XOUTMAXOSWINMAPK)XVVVI1.6VLIfu(cid:16) (cid:14)uuuwww.ti.com

TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

the regulator. In this case, the output capacitor must hold the output voltage above a certain level for a specified
amount  of  time  after  the  input  power  is  removed.  The  regulator  is  also  temporarily  unable  to  supply  sufficient
output current if a large, fast increase occurs affecting the current requirements of the load, such as a transition
from no load to full load. The regulator usually requires two or more clock cycles for the control loop to notice
the  change  in  load  current  and  output  voltage  and  to  adjust  the  duty  cycle  to  react  to  the  change.  The  output
capacitor must be sized to supply the extra current to the load until the control loop responds to the load change.
The  output  capacitance  must  be  large  enough  to  supply  the  difference  in  current  for  2  clock  cycles  while  only
allowing  a  tolerable  amount  of  drop  in  the  output  voltage.  Use  Equation  11  to  calculate  the  minimum  required
output capacitance.

(11)

where

• ∆IOUT is the change in output current.
•
• ∆VOUTb is the allowable change in the output voltage.

fSW is the switching frequency of the regulator.

For this example, the transient load response is specified as a 5% change in the output voltage, VOUT, for a load
step  of  1.5  A.  For  this  example,  ΔIOUT  =  1.5  A  and  ΔVOUT  =  0.05  ×  5  =  0.25  V.  Using  these  values  results  in
a  minimum  capacitance  of  30  μF.  This  value  does  not  consider  the  ESR  of  the  output  capacitor  in  the  output
voltage change. For ceramic capacitors, the ESR is usually small enough to ignore in this calculation.

Use  Equation  12  to  calculate  the  minimum  output  capacitance  required  to  meet  the  output  voltage  ripple
specification.  In  this  case,  the  maximum  output  voltage  ripple  is  30  mV.  Under  this  requirement,  Equation  12
yields 10.7 μF.

where

• ƒSW is the switching frequency.
• VOUTripple is the maximum allowable output voltage ripple.
•

Iripple is the inductor ripple current

Use Equation 13 to calculate the maximum ESR an output capacitor can have to meet the output-voltage ripple
specification. Equation 13 indicates the ESR should be less than 29.2 mΩ. In this case, the ESR of the ceramic
capacitor is much smaller than 29.2 mΩ.

(12)

The  output  capacitor  can  affect  the  crossover  frequency  fo.  Considering  the  loop  stability  and  effect  of  the
internal  parasitic  parameters,  choose  the  crossover  frequency  less  than  40  kHz  without  considering  the  feed
forward capacitor. A simple estimation for the crossover frequency without feed forward capacitor C6 is shown in
Equation 14, assuming CO has small ESR.

(13)

Additional  capacitance  deratings  for  aging,  temperature,  and  DC  bias  should  be  considered  which  increases
this minimum value. For this example, two 22-uF 25-V, X7R ceramic capacitors are used. Capacitors generally
have limits to the amount of ripple current they can handle without failing or producing excess heat. An output

(14)

Copyright © 2021 Texas Instruments Incorporated

Submit Document Feedback

17

Product Folder Links: TPS54302

OUTOswOUT2ICfVu'!u'OOUTrippleSWripple11CV8fI´>´OUTrippleESRrippleVRI<oOUTO5.1f= V CuTPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

www.ti.com

capacitor that can support the inductor ripple current must be specified. Some capacitor data sheets specify the
RMS value of the maximum ripple current. Use Equation 15 to calculate the RMS ripple current that the output
capacitor must support. For this application, Equation 15 yields 296 mA for each capacitor.

8.2.3.5.3 Feedforward Capacitor

The  TPS54302  device  is  internally  compensated  and  the  internal  compensation  network  is  composed  of  two
capacitors and one resister shown on the Section 7.2. Depending on the VOUT, if the output capacitor COUT is
dominated  by  low  ESR  (ceramic  types)  capacitors,  it  could  result  in  low  phase  margin.  To  improve  the  phase
boost an external feedforward capacitor C6 can be added in parallel with R2. The C6 capacitor is chosen such
that phase margin is boosted at the crossover frequency.

Equation 16 for C6 was tested.

(15)

(16)

For this design, C6 = 75 pF. The C6 capacitor is not needed when COUT has high ESR, and C6 calculated from
Equation 16 should be reduced with medium ESR. Table 8-2 can be used as a starting point.

Table 8-2 lists some recommended component values.

VOUT (V)

L (µH)

COUT (µF)

R2 (kΩ)

R3 (kΩ)

C8 (pF)

Table 8-2. Recommended Component Values

1.8

2.5

3.3

5

12

4.7

5.6

6.8

10

15

66

66

44

44

44

100

100

100

100

100

49.9

31.6

22.1

13.3

5.23

33

47

47

75

100

18

Submit Document Feedback

Copyright © 2021 Texas Instruments Incorporated

Product Folder Links: TPS54302

(cid:11)(cid:12)(cid:11)(cid:12)(cid:11)(cid:12)(cid:11)(cid:12)OUTOUTINMAXCOUTRMSOSWCINMAXVVV1IVLfN12§·u(cid:16)¨¸ u¨¸uuu¨¸©¹o11C6 = 2fR2uSwww.ti.com

8.2.4 Application Curves

TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

Figure 8-2. Efficiency

Figure 8-3. Line Regulation

Figure 8-4. Load Regulation

Figure 8-5. Input Voltage Ripple

IOUT = 0 A

IOUT = 10 mA

Figure 8-6. Output Voltage Ripple

Figure 8-7. Output Voltage Ripple

Copyright © 2021 Texas Instruments Incorporated

Submit Document Feedback

19

Product Folder Links: TPS54302

Output Current (A)Efficiency (%)01020304050607080901000.0010.010.11D013VIN = 24 V, VOUT = 5 VVIN = 12 V, VOUT = 5 VInput Voltage (V)Line Regulation (%)6810121416182022242628-0.5-0.4-0.3-0.2-0.100.10.20.30.40.5D014Output Current (A)Load Regulation (%)0.10.61.11.62.12.63.1-0.8-0.6-0.4-0.200.20.40.60.8D015VIN = 24 VVIN = 12 VVIN = 200 mV/div (ac coupled)PH = 10 V/divTime - 2s/divmVOUT= 20 mV/div (ac coupled)PH = 10 V/divTime - 4 ms/divVOUT= 20 mV/div (ac coupled)PH = 10 V/divTime - 40s/divmTPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

www.ti.com

IOUT = 100 mA

IOUT = 1.5 A

Figure 8-8. Output Voltage Ripple

Figure 8-9. Output Voltage Ripple

IOUT = 3 A

0.75 to 2.25-A load step

Slew rate = 250

mA/μs

Figure 8-10. Transient Response

Figure 8-11. Transient Response

Figure 8-12. Start-Up Relative to VIN

Figure 8-13. Shutdown Relative to VIN

20

Submit Document Feedback

Copyright © 2021 Texas Instruments Incorporated

Product Folder Links: TPS54302

VOUT= 20 mV/div (ac coupled)PH = 10 V/divTime - 4s/divmVOUT= 20 mV/div (ac coupled)PH = 10 V/divTime - 2s/divmVOUT- 20 mV/div (ac coupled)PH = 10 V/divTime - 200s/divmVOUT= 100 mV/div (ac coupled)IOUT= 1A/divTime - 200s/divmVin = 10 V/divEN = 2 V/divVout = 2 V/divTime - 2 ms/divVin = 10 V/divEN = 2 V/divVout = 2 V/divTime - 4 ms/divwww.ti.com

TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

Figure 8-14. Start-Up Relative to EN

Figure 8-15. Shutdown Relative to EN

9 Power Supply Recommendations

The device is designed to operate from an input voltage supply range from 4.5 V to 28 V. This input supply must
be well regulated. If the input supply is located more than a few inches from the device or converter, additional
bulk capacitance may be required in addition to the ceramic bypass capacitors. An electrolytic capacitor with a
value of 47 µF is a typical choice.

Copyright © 2021 Texas Instruments Incorporated

Submit Document Feedback

21

Product Folder Links: TPS54302

Vin = 10 V/divEN = 2 V/divVout = 2 V/divTime - 2 ms/divVout = 2 V/divEN = 2 V/divVin = 10 V/divTime - 2 ms/divTPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

10 Layout
10.1 Layout Guidelines

Follow these layout guidelines:

www.ti.com

• The VIN and GND traces should be as wide as possible to reduce trace impedance. The wide areas are also

of advantage from the view point of heat dissipation.

• The input capacitor and output capacitor should be placed as close to the device as possible to minimize

trace impedance.

• Provide sufficient vias for the input capacitor and output capacitor.
• Keep the SW trace as physically short and wide as practical to minimize radiated emissions.
• Do not allow switching current to flow under the device.
• A separate VOUT path should be connected to the upper feedback resistor.
• Make a Kelvin connection to the GND pin for the feedback path.
• The voltage feedback loop should be placed away from the high-voltage switching trace, and preferably has

ground shield.

• The trace of the VFB node should be as small as possible to avoid noise coupling.
• The GND trace between the output capacitor and the GND pin should be as wide as possible to minimize its

trace impedance.

10.2 Layout Example

Figure 10-1. Board Layout

22

Submit Document Feedback

Copyright © 2021 Texas Instruments Incorporated

Product Folder Links: TPS54302

ENVFBVBSTGNDSWFEEDBACKRESISTORSTO ENABLECONTROLVINGNDBOOSTCAPACITOROUTPUTINDUCTOROUTPUTCAPACITORVOUTINPUT BYPASCAPACITORVINSW node copper pour area on internal or bottom layerAdditionalVias to the GND planeVias to the internal SW node copperVias to the internal SW node copperwww.ti.com

11 Device and Documentation Support
11.1 Device Support
11.1.1 Third-Party Products Disclaimer

TPS54302
SLVSDG6B – MAY 2016 – REVISED APRIL 2021

TI'S PUBLICATION OF INFORMATION REGARDING THIRD-PARTY PRODUCTS OR SERVICES DOES NOT
CONSTITUTE  AN  ENDORSEMENT  REGARDING  THE  SUITABILITY  OF  SUCH  PRODUCTS  OR  SERVICES
OR A WARRANTY, REPRESENTATION OR ENDORSEMENT OF SUCH PRODUCTS OR SERVICES, EITHER
ALONE OR IN COMBINATION WITH ANY TI PRODUCT OR SERVICE.

11.2 Receiving Notification of Documentation Updates

To  receive  notification  of  documentation  updates,  navigate  to  the  device  product  folder  on  ti.com.  Click  on
Subscribe to updates to register and receive a weekly digest of any product information that has changed. For
change details, review the revision history included in any revised document.

11.3 Support Resources

TI  E2E™  support  forums  are  an  engineer's  go-to  source  for  fast,  verified  answers  and  design  help  —  straight
from the experts. Search existing answers or ask your own question to get the quick design help you need.

Linked content is provided "AS IS" by the respective contributors. They do not constitute TI specifications and do
not necessarily reflect TI's views; see TI's Terms of Use.

11.4 Trademarks
Eco-mode™ and TI E2E™ are trademarks of Texas Instruments.
All trademarks are the property of their respective owners.
11.5 Electrostatic Discharge Caution

This integrated circuit can be damaged by ESD. Texas Instruments recommends that all integrated circuits be handled
with appropriate precautions. Failure to observe proper handling and installation procedures can cause damage.

ESD damage can range from subtle performance degradation to complete device failure. Precision integrated circuits may
be more susceptible to damage because very small parametric changes could cause the device not to meet its published
specifications.

11.6 Glossary

TI Glossary

This glossary lists and explains terms, acronyms, and definitions.

12 Mechanical, Packaging, and Orderable Information

The  following  pages  include  mechanical,  packaging,  and  orderable  information.  This  information  is  the  most
current data available for the designated devices. This data is subject to change without notice and revision of
this document. For browser-based versions of this data sheet, refer to the left-hand navigation.

Copyright © 2021 Texas Instruments Incorporated

Submit Document Feedback

23

Product Folder Links: TPS54302

www.ti.com

9-Nov-2025

PACKAGE OPTION ADDENDUM

PACKAGING INFORMATION

Orderable part number

Status

Material type

Package | Pins

Package qty | Carrier

RoHS

(1)

(2)

TPS54302DDCR

Active

Production

TPS54302DDCR.A

Active

Production

TPS54302DDCR.B

Active

Production

TPS54302DDCT

Active

Production

TPS54302DDCT.A

Active

Production

TPS54302DDCT.B

Active

Production

SOT-23-
THIN (DDC) | 6

SOT-23-
THIN (DDC) | 6

SOT-23-
THIN (DDC) | 6

SOT-23-
THIN (DDC) | 6

SOT-23-
THIN (DDC) | 6

SOT-23-
THIN (DDC) | 6

3000 | LARGE T&R

3000 | LARGE T&R

3000 | LARGE T&R

250 | SMALL T&R

250 | SMALL T&R

250 | SMALL T&R

(3)

Yes

Yes

Yes

Yes

Yes

Yes

Lead finish/
Ball material

(4)

SN

SN

SN

SN

SN

SN

(1) Status:  For more details on status, see our product life cycle.

Op temp (°C)

Part marking

MSL rating/
Peak reflow

(5)

Level-1-260C-UNLIM

-40 to 125

Level-1-260C-UNLIM

-40 to 125

Level-1-260C-UNLIM

-40 to 125

Level-1-260C-UNLIM

-40 to 125

Level-1-260C-UNLIM

-40 to 125

Level-1-260C-UNLIM

-40 to 125

(6)

4302

4302

4302

4302

4302

4302

(2) Material type:  When designated, preproduction parts are prototypes/experimental devices, and are not yet approved or released for full production. Testing and final process, including without limitation quality assurance,
reliability performance testing, and/or process qualification, may not yet be complete, and this item is subject to further changes or possible discontinuation. If available for ordering, purchases will be subject to an additional
waiver at checkout, and are intended for early internal evaluation purposes only. These items are sold without warranties of any kind.

(3) RoHS values:  Yes, No, RoHS Exempt. See the TI RoHS Statement for additional information and value definition.

(4) Lead finish/Ball material:  Parts may have multiple material finish options. Finish options are separated by a vertical ruled line. Lead finish/Ball material values may wrap to two lines if the finish value exceeds the maximum
column width.

(5) MSL rating/Peak reflow:  The moisture sensitivity level ratings and peak solder (reflow) temperatures. In the event that a part has multiple moisture sensitivity ratings, only the lowest level per JEDEC standards is shown.
Refer to the shipping label for the actual reflow temperature that will be used to mount the part to the printed circuit board.

(6) Part marking:  There may be an additional marking, which relates to the logo, the lot trace code information, or the environmental category of the part.

Multiple part markings will be inside parentheses. Only one part marking contained in parentheses and separated by a "~" will appear on a part. If a line is indented then it is a continuation of the previous line and the two
combined represent the entire part marking for that device.

Addendum-Page 1

www.ti.com

9-Nov-2025

PACKAGE OPTION ADDENDUM

Important Information and Disclaimer:The information provided on this page represents TI's knowledge and belief as of the date that it is provided. TI bases its knowledge and belief on information provided by third parties, and
makes no representation or warranty as to the accuracy of such information. Efforts are underway to better integrate information from third parties. TI has taken and continues to take reasonable steps to provide representative
and accurate information but may not have conducted destructive testing or chemical analysis on incoming materials and chemicals. TI and TI suppliers consider certain information to be proprietary, and thus CAS numbers
and other limited information may not be available for release.

In no event shall TI's liability arising out of such information exceed the total purchase price of the TI part(s) at issue in this document sold by TI to Customer on an annual basis.

Addendum-Page 2

www.ti.com

13-Oct-2025

PACKAGE MATERIALS INFORMATION

TAPE AND REEL INFORMATION

REEL DIMENSIONS

TAPE DIMENSIONS

K0

 P1

B0 W

Reel
Diameter

Cavity

A0

A0
B0
K0
W
P1

Dimension designed to accommodate the component width
Dimension designed to accommodate the component length
Dimension designed to accommodate the component thickness
Overall width of the carrier tape
Pitch between successive cavity centers

Reel Width (W1)

QUADRANT ASSIGNMENTS FOR PIN 1 ORIENTATION IN TAPE

Sprocket Holes

Q1

Q2

Q1

Q2

Q3

Q4

Q3

Q4

User Direction of Feed

Pocket Quadrants

*All dimensions are nominal

Device

Package
Type

Package
Drawing

Pins

SPQ

Reel
Diameter
(mm)

Reel
Width
W1 (mm)

A0
(mm)

B0
(mm)

K0
(mm)

P1
(mm)

W
(mm)

Pin1
Quadrant

TPS54302DDCR

TPS54302DDCR

TPS54302DDCT

TPS54302DDCT

SOT-23-
THIN

SOT-23-
THIN

SOT-23-
THIN

SOT-23-
THIN

DDC

DDC

DDC

DDC

6

6

6

6

3000

180.0

9.5

3.17

3.1

1.1

4.0

8.0

3000

180.0

9.5

3.17

3.1

1.1

4.0

8.0

250

180.0

9.5

3.17

3.1

1.1

4.0

8.0

250

180.0

9.5

3.17

3.1

1.1

4.0

8.0

Q3

Q3

Q3

Q3

Pack Materials-Page 1

PACKAGE MATERIALS INFORMATION

www.ti.com

13-Oct-2025

TAPE AND REEL BOX DIMENSIONS

Width (mm)

H

W

L

*All dimensions are nominal

Device

Package Type

Package Drawing Pins

TPS54302DDCR

SOT-23-THIN

TPS54302DDCR

SOT-23-THIN

TPS54302DDCT

SOT-23-THIN

TPS54302DDCT

SOT-23-THIN

DDC

DDC

DDC

DDC

6

6

6

6

SPQ

3000

3000

250

250

Length (mm) Width (mm) Height (mm)

205.0

184.0

205.0

184.0

200.0

184.0

200.0

184.0

30.0

19.0

30.0

19.0

Pack Materials-Page 2

DDC0006A

SCALE  4.000

PACKAGE OUTLINE

SOT-23 - 1.1 max height

SMALL OUTLINE TRANSISTOR

PIN 1
INDEX AREA

4X  0.95

1.9

1

3

0 -8  TYP

0.20
0.12

 TYP

3.05
2.55

1.75
1.45

B

A

0.1 C

1.1
0.7

6

4

3.05
2.75

4X 0 -15

6X

0.5
0.3
0.2

C A B

4X 4 -15

C

0.1
0.0

 TYP

SEATING PLANE

0.25
GAGE PLANE

0.6
0.3

 TYP

NOTES:

1. All linear dimensions are in millimeters. Any dimensions in parenthesis are for reference only. Dimensioning and tolerancing
    per ASME Y14.5M.
2. This drawing is subject to change without notice.
3. Reference JEDEC MO-193.

4214841/E   08/2024

www.ti.com

DDC0006A

EXAMPLE BOARD LAYOUT

SOT-23 - 1.1 max height

SMALL OUTLINE TRANSISTOR

6X (1.1)

SYMM

1

3

6X (0.6)

4X (0.95)

(R0.05) TYP

SYMM

6

4

(2.7)

LAND PATTERN EXAMPLE
EXPLOSED METAL SHOWN
SCALE:15X

SOLDER MASK
OPENING

METAL

METAL UNDER
SOLDER MASK

SOLDER MASK
OPENING

EXPOSED METAL

EXPOSED METAL

0.07 MAX
ARROUND

NON SOLDER MASK
DEFINED

0.07 MIN
ARROUND

SOLDER MASK
DEFINED

SOLDERMASK DETAILS

NOTES: (continued)

4. Publication IPC-7351 may have alternate designs.
5. Solder mask tolerances between and around signal pads can vary based on board fabrication site.

4214841/E   08/2024

www.ti.com

DDC0006A

EXAMPLE STENCIL DESIGN

SOT-23 - 1.1 max height

SMALL OUTLINE TRANSISTOR

1

3

6X (0.6)

4X(0.95)

(R0.05) TYP

SYMM

6X (1.1)

SYMM

6

4

(2.7)

SOLDER PASTE EXAMPLE
BASED ON 0.125 THICK STENCIL
SCALE:15X

NOTES: (continued)

6. Laser cutting apertures with trapezoidal walls and rounded corners may offer better paste release. IPC-7525 may have alternate
     design recommendations.
7. Board assembly site may have different recommendations for stencil design.

4214841/E   08/2024

www.ti.com

IMPORTANT NOTICE AND DISCLAIMER
TI PROVIDES TECHNICAL AND RELIABILITY DATA (INCLUDING DATASHEETS), DESIGN RESOURCES (INCLUDING REFERENCE
DESIGNS), APPLICATION OR OTHER DESIGN ADVICE, WEB TOOLS, SAFETY INFORMATION, AND OTHER RESOURCES “AS IS”
AND WITH ALL FAULTS, AND DISCLAIMS ALL WARRANTIES, EXPRESS AND IMPLIED, INCLUDING WITHOUT LIMITATION ANY
IMPLIED WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE OR NON-INFRINGEMENT OF THIRD
PARTY INTELLECTUAL PROPERTY RIGHTS.

These resources are intended for skilled developers designing with TI products. You are solely responsible for (1) selecting the appropriate
TI products for your application, (2) designing, validating and testing your application, and (3) ensuring your application meets applicable
standards, and any other safety, security, regulatory or other requirements.

These resources are subject to change without notice. TI grants you permission to use these resources only for development of an
application that uses the TI products described in the resource. Other reproduction and display of these resources is prohibited. No license
is granted to any other TI intellectual property right or to any third party intellectual property right. TI disclaims responsibility for, and you fully
indemnify TI and its representatives against any claims, damages, costs, losses, and liabilities arising out of your use of these resources.

TI’s products are provided subject to TI’s Terms of Sale, TI’s General Quality Guidelines, or other applicable terms available either on
ti.com or provided in conjunction with such TI products. TI’s provision of these resources does not expand or otherwise alter TI’s applicable
warranties or warranty disclaimers for TI products. Unless TI explicitly designates a product as custom or customer-specified, TI products
are standard, catalog, general purpose devices.

TI objects to and rejects any additional or different terms you may propose.

IMPORTANT NOTICE

Copyright © 2025, Texas Instruments Incorporated

Last updated 10/2025

