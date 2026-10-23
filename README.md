# DIY power bank: 120 W target

I started this project to design a compact power bank with a custom enclosure and a high output power target. The case has cutouts for USB-A, USB-C, and a DC input, with my name and logo on the shell.

The design is still in progress. **120 W is the target**, and this repo doesn't include a load test confirming that output.

![Enclosure design](CAD/Images/P3.png)
![Another enclosure view](CAD/Images/P1.png)

## What's here

I designed the case in SolidWorks around the batteries, converters, connectors, and displays. PETG and a 3 mm wall were the starting choices for the printed enclosure, but component fit still needs checking against the actual parts.

The planned electronics use six 18650 cells, battery protection boards, converter modules, a voltage/current display, and a battery indicator. The component list is a record of the design stage; it doesn't establish the finished pack's charging support or usable output power.

## Design files

- [SolidWorks case](CAD/Power%20Bank%20case.SLDPRT)
- [Printable STL](CAD/Power%20Bank%20case.STL)
- [Circuit diagram](CAD/Circuit%20diagram.png)
- [Build journal](JOURNAL.md)
- [BOM](BOM.csv) and [additional BOM files](BOM/)
- [License](LICENSE.MD)

## Original parts estimate

These are the original component prices and supplier links. The rows below add up to **2,878 EGP**; the old README's total was 100 EGP short. This is a parts estimate from that stage, not a current quote.

| Component                          | Qty | EGP/Unit | Sum EGP | Sum USD | Purpose                 | Link |
|-----------------------------------|-----|----------|---------|---------|--------------------------|------|
| 18650 Li-ion 3350mAh battery      | 6   | 130      | 780     | 15.69   | Battery cells            | [Link](https://makerselectronics.com/product/li-ion-rechargeable-bak-18650-battery-high-drain-3-6v-3350mah-10a-n18650cp-used-like-new) |
| 3S 10A BMS board                  | 2   | 65       | 130     | 2.62    | Battery protection       | [Link](https://makerselectronics.com/product/bms-3s-10a-12-6v-lithium-battery-charger-protection-module) |
| USB-PD trigger board             | 1   | 200      | 200     | 4.02    | PD 12V trigger           | [Link](https://makerselectronics.com/product/usb-pd-decoy-trigger-board-adjustable-volt-5v-9v-12v) |
| DC jack w/ terminal block        | 1   | 75       | 75      | 1.51    | Power connector          | [Link](https://makerselectronics.com/product/female-dc-jack-adapter-with-terminal-block) |
| Mini push-button 6x6x9mm         | 2   | 5        | 10      | 0.20    | Manual input             | [Link](https://makerselectronics.com/product/mini-push-button-4-pin-6x6x9mm) |
| DC-DC Boost Converter 400W       | 1   | 350      | 350     | 7.04    | Voltage step-up          | [Link](https://makerselectronics.com/product/dc-dc-boost-converter-voltage-step-up-module-400w-12a) |
| Digital Voltmeter & Ammeter      | 1   | 175      | 175     | 3.52    | Display voltage/current  | [Link](https://makerselectronics.com/product/dc-0-100v-10a-digital-voltmeter-and-ammeter-dual-display) |
| Battery capacity LCD (GY-6)      | 1   | 170      | 170     | 3.42    | Charge indicator         | [Link](https://microohm-eg.com/product/battery-capacity-indicator-tester-lcd-panel-gy-6) |
| QC 4.0 Step-Down Module (AliExpress) | 2 | 300  | 600     | 12.07   | Fast charging input      | [Link](https://www.aliexpress.us/item/3256808964103204.html) |
| USB-C female board (RAM-E)       | 1   | 75       | 75      | 1.51    | USB-C output             | [Link](https://www.ram-e-shop.com/shop/kit-usb9-c-type-usb-type-c-female-interface-board-8031) |
| AWG 12 wire (1m)                 | 1m  | 100      | 100     | 2.01    | Main high-current wiring | [Link](https://store.fut-electronics.com/products/copy-of-wire-awg-12-black-0-5-m) |
| PVC heat-shrink tube (battery wrap) | 1m | 35     | 35      | 0.70    | Insulates packs          | [Link](https://microohm-eg.com/ar/product/lithium-battery-pvc-heat-shrink-blue-tube-for-85mm-180mm-1-meter/) |
| 0.2×8 mm plated nickel strip (1m)| 1m  | 18       | 18      | 0.36    | Battery weld tabs        | [Link](https://microohm-eg.com/ar/product/0-2-x-8-mm-plated-nickel-strip-for-battery-connection-welding-1-meter/) |
| Aluminium soldering flux (10mL)  | 1   | 60       | 60      | 1.21    | Soldering aid            | [Link](https://makerselectronics.com/product/aluminium-soldering-liquid-flux-10ml) |

I'll need to check the finished wiring, charging circuit, thermal performance, and output under load before calling this a working 120 W power bank.
