# zybo-freertos-secure-lock

Sistem distribuit de control al accesului în timp real, pe Zybo Z7 (SoC Zynq-7000, ARM Cortex-A9) cu FreeRTOS. O „încuietoare" și o „cheie" comunică prin CAN, folosind un protocol propriu de nivel înalt de tip challenge-response (cadre cu CRC, nonce anti-replay, timeout). Un task de timp real citește butonul și comandă servo-ul prin PWM, iar un task de comunicație gestionează protocolul. Task-urile se sincronizează prin cozi de mesaje și mutex.
Proiect pentru disciplina Sisteme Distribuite și de Timp Real.

## Structură
- `docs/` - specificații, schemă bloc, analiza de timp real
- `src/`  - cod sursă (Vitis / FreeRTOS)
- `hw/`   - proiect Vivado (script .tcl + .xsa)

## Hardware
- Zybo Z7 (nodul "încuietoare")
- A doua placă (nodul "cheie")
- Servo, buton, LED-uri, legătură UART/CAN

## Stadiu
- [x] Alegere temă și arhitectură
- [ ] Task-uri FreeRTOS + coadă
- [ ] Protocol (cadre, CRC, handshake)
- [ ] Măsurători de timp real
- [ ] Documentație și articol IEEE
