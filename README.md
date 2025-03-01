# Arquitectura ARM

## 1. Introducción a la arquitectura ARM
La arquitectura *ARM (Advanced RISC Machine)* es un conjunto de diseños de procesadores basado en la arquitectura *RISC (Reduced Instruction Set Computing)*. Fue desarrollada por **Acorn Computers** en los años 80 y se ha convertido en una de las arquitecturas más utilizadas en dispositivos móviles, sistemas embebidos y cada vez más en servidores y PCs.

Los procesadores ARM se destacan por su eficiencia energética, rendimiento optimizado y amplio soporte en la industria.

---

## 2. Historia
- *1983*: Acorn Computers inicia el desarrollo de un procesador RISC para sus computadoras personales.
- *1985*: Se lanza el primer procesador ARM, el **ARM1**.
- *1990*: Se funda **ARM Ltd.**, separándose de Acorn.
- *1991-1995*: Se lanzan los procesadores **ARM6 y ARM7**, usados en dispositivos como la Apple Newton.
- *2000s*: Se expanden al mercado de teléfonos móviles, con arquitecturas como **ARM9 y ARM11**.
- *2010s en adelante*: Se desarrollan los **Cortex-A**, utilizados en smartphones, tablets, y más recientemente en computadoras portátiles como los chips **Apple M1/M2/M3** y los **Qualcomm Snapdragon** para PCs.

---

## 3. Ensamblador
El ensamblador ARM es el lenguaje de bajo nivel que se utiliza para programar directamente los procesadores ARM.

### Instrucciones
Las instrucciones en *ARM* siguen el principio RISC, lo que significa que tienen un tamaño fijo (normalmente 32 bits, aunque existen variantes de 16 bits como *Thumb*). Algunos ejemplos de instrucciones son:

- *MOV*: Mueve datos de un registro a otro.  
  ```assembly
  MOV R0, #10   ; R0 = 10

```markdown
- **ADD**: Suma dos valores y almacena el resultado en un registro.

  ```assembly
  ADD R1, R0, #5   ; R1 = R0 + 5
  ```

- **SUB**: Resta un valor de un registro.

  ```assembly
  SUB R2, R1, #3   ; R2 = R1 - 3
  ```

- **B (Branch)**: Salta a una dirección de memoria específica.

  ```assembly
  B etiqueta  ; Salta a la etiqueta especificada
  ```

---

### Registros

ARM utiliza un conjunto de registros generales, entre los cuales destacan:
- **R0 - R12**: Registros de propósito general.
- **R13 (SP)**: Stack Pointer (Puntero de pila).
- **R14 (LR)**: Link Register (Registro de enlace para subrutinas).
- **R15 (PC)**: Program Counter (Contador de programa).

---

## 4. Código ejemplo

Aquí tienes un ejemplo de código en ensamblador ARM que suma dos números y almacena el resultado en un registro:

```assembly
MOV R0, #5       ; R0 = 5
MOV R1, #10      ; R1 = 10
ADD R2, R0, R1   ; R2 = R0 + R1 (R2 = 5 + 10)
```

Si se ejecuta en un procesador ARM, *R2* contendrá el valor 15.

---

## 5. Aplicaciones

La arquitectura ARM tiene una amplia variedad de aplicaciones en la industria, incluyendo:
- **Teléfonos móviles y tablets**: Usado en procesadores Qualcomm Snapdragon, Apple A-series, Exynos y MediaTek.
- **Computadoras personales**: Chips Apple M1/M2/M3, Qualcomm Snapdragon X Elite, y otras arquitecturas emergentes en PCs ARM con Windows.
- **Sistemas embebidos**: Utilizado en dispositivos de IoT, microcontroladores como ARM Cortex-M y Raspberry Pi.
- **Automoción**: ARM es común en sistemas de infoentretenimiento y asistencia en la conducción.
- **Servidores y computación en la nube**: Empresas como Amazon AWS (Graviton) han desarrollado procesadores ARM para servidores eficientes en energía.
