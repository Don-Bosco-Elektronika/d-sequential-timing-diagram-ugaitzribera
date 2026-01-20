# 🛠️ Cronograma de Circuitos Secuenciales / Zirkuitu Sekuentzialen Kronograma / Sequential Circuit Timing Diagram

| **Alumnos** | **Curso** | **Módulo** |
|-------------|-----------|------------|
| 2ME         | 1º        | EEM (Equipos Microprogramables) |

---

## 📌 Ejercicio / Ariketa / Exercice

**Ariketa (EU): (ZENBAKIA IDATZI)**  
|Izena                     | Txip Zenbakia | Sinboloa        | Funtzionamendu Describapena                                                              |
|---------------------------|------------------|------------------|---------------------------------------------------------------------------------|
| D | 74100            | <img width="147" height="117" alt="74100 D Sinboloa" src="https://github.com/user-attachments/assets/a45d8f19-eada-4a89-ab39-1803079908b5" />| 8 biteko latch-a (bi 4 biteko bloketan banatuta), datuak aldi baterako gordetzeko | 


| Izena                     | Txip Zenbakia | Sinboloa         | Funtzionamendu Describapena                                                                |
|---------------------------|------------------|------------------|---------------------------------------------------------------------------------|
| D | 74175             | <img width="211" height="103" alt="74175 D Sinboloa" src="https://github.com/user-attachments/assets/53050ae2-ab83-476e-ba1e-e2c4a2323467" />| Lau D motako flip-flop, "clear" (garbitu) sarrera komunarekin |  

 
| Izena                     |Txip Zenbakia | Sinboloa        | Funtzionamendu Describapena                                                                |
|---------------------------|------------------|------------------|---------------------------------------------------------------------------------|
| D | 74164 | <img width="211" height="103" alt="74164 D Sinboloa" src="https://github.com/user-attachments/assets/78c4f32f-0529-439c-bbe9-3545ddcd77fb" />| 8 biteko desplazamendu-erregistroa: Serie sarrera eta Paralelo irteera (SIPO) |  


| Izena                     |Txip Zenbakia | Sinboloa        | Funtzionamendu Describapena                                                                |
|---------------------------|------------------|------------------|---------------------------------------------------------------------------------|
| D | 74165 |<img width="211" height="103" alt="74165 D Sinboloa" src="https://github.com/user-attachments/assets/3dd78bd8-97c7-4095-8ca9-4c588ac780c3" />| 8 biteko desplazamendu-erregistroa: Paralelo sarrera eta Serie irteera (PISO) | 


| Izena                     |Txip Zenbakia | Sinboloa        | Funtzionamendu Describapena                                                                |
|---------------------------|------------------|------------------|---------------------------------------------------------------------------------|
| D | 74595 | <img width="211" height="103" alt="74595 D Sinboloa" src="https://github.com/user-attachments/assets/1a845ad2-a972-4183-80a8-0b5c021515b8" />| 8 biteko desplazamendu-erregistroa (SIPO), irteeran latch bat duena datuak egonkor mantentzeko | 

---

## Tabla de la verdad

| Entrada A | Entrada B | Entrada C | Salida    | Salida |
|-----------|-----------|-----------|-----------|--------|
| 0         | 0         | 0         | ░0░       | ░0░    |
| 0         | 0         | 1         | ░1░       | ░1░    |
| 1         | 1         | 0         | ░1░       | ░1░    |
| 1         | 1         | 1         | ░0░       | ░0░    |

---

## 🔲Simulatzeko Zirkuituak 

<img width="1055" height="686" alt="D zirkuituak proteus" src="https://github.com/user-attachments/assets/bc7afff0-ec1e-4bd0-b086-8fc8edf33f7f" />


---

## 🔲  Kronogramaren Emaitza 
D Asincrono

<img width="950" height="745" alt="D asincrono ariketa" src="https://github.com/user-attachments/assets/89c2d5c4-5add-475e-9200-005bdbe6a280" />


D Flanco ascendente

<img width="980" height="762" alt="D flanco ascendente ariketa" src="https://github.com/user-attachments/assets/f2b05c86-e861-4fe0-a16d-0d944a047628" />


D Flanco descendente

<img width="967" height="763" alt="D flanco descendente ariketa" src="https://github.com/user-attachments/assets/ba15c036-f633-4794-8f76-74147cbcda30" />

D Nivel alto

<img width="996" height="720" alt="D nivel alto ariketa" src="https://github.com/user-attachments/assets/6f61230d-9e01-4357-a9f5-5eb9cd9da6d1" />

D Nivel bajo

<img width="967" height="772" alt="D nivel bajo ariketa" src="https://github.com/user-attachments/assets/aaa947ad-b815-451f-b148-cabb225ee773" />


---


## 🔲  Kronogramaren Kodea 
D Asincrono

{signal: [

  {name: 'D',  wave: 'h.l...h..hl.hl..h'},
  
  {},
  
  {name: 'Q',  wave: 'h.l...h...l.hl..h'},
  
  {name: '-Q', wave: 'l.h...l...h.lh..l'}
  
]}


D Flanco ascendnete

{signal: [

  {name: 'clk', wave: 'P........', period: 2},
  
  {name: 'D',   wave: '10101..0.10.101010'},
  
  {},
  
  {name: 'Q',   wave: '1.......0...1.....'},
  
  {name: '-Q',  wave: '0.......1...0.....'},
  
]}

D Flanco descendente

{signal: [

  {name: 'clk', wave: 'N........', period: 2},
  
  {name: 'D',   wave: '0101..0101.0..1010'},
  
  {},
  
  {name: 'Q',   wave: '0.1...0.1.0...1.0.'},
  
  {name: '-Q',  wave: '1.0...1.0.1...0.1.'}
  
]}

D Nivel alto

{signal: [

  {name: 'clk', period: 2, wave: 'p........'},
  
  {name: 'D',   wave: '0101..0.101.0..101'},
  
  {},
  
  {name: 'Q',   wave: '0...1.0.1...0.....'},
  
  {name: '-Q',  wave: '1...0.1.0...1.....'}
  
]}

D Nivel bajo

{signal: [

  {name: 'clk', period: 2, wave: 'n........'},
  
  {name: 'D',   wave: '0101..0101.01010.1'},
  
  {},
  
  {name: 'Q',   wave: '01......01...0...1'},
  
  {name: '-Q',  wave: '10......10...1...0'}
  
]}

---


## 📤 Igo  

➡️ **Instrucciones:**  

- **EU:** Igo hurrengo fitxategiak. Igotako fitxategi guztiek zure izena eduki behar dute.  
  - Sinboloaren argazki bat.  
  - Proteus fitxategia eta zirkuitu bakoitzaren irudia (captura) Proteusen.  
  - Wavedrom bakoitzaren emaitzaren kaptura (grafikoa bakarrik).  
  - **KONTUZ:** Kronogramaren kodea kodea izan behar da, ez irudi bat.




