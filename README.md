# Modulation Schemes Simulation
Simulating the performance of different modulation schemes, BPSK, QPSK, FSK, QAM16 and QAM64 in an AWGN environment using matlab simulink.
Also simulating these schemes after adding raised cosine filter.

# General Configurations
Set the simulation time to 100

* Random Integer Generator
    * Source of initial seed: parameter
    * Initial seed: 37
    * Samples per frame: 100
    
* AWGN Channel
    * Eb/No (dB): EbNo
   
* Error Rate Calculation
    * Output data : Port
    * check stop simulation
    * Target number of errors: 100
    * Maximum number of symbols: 1e4
    
 
### Binary Phase Shift Keying Modulation (BPSK)
Binary phase shift keying is a modulation scheme that can transfer one bit per symbol. So we use two phase offsets (one for logic high, one for logic low). We want the maximum seperation between the phase options, which in this case is 180°.

* Modulation Schematic

The *Random Integer generator* generates random uniformaly distributed integers from range [0,M-1] , M is set to 2 So here it generates 0,1.
These bits enter the *BPSK Modulator* and then passes through the *AWGN channel*. At the other side the *BPSK Demodulator* takes the transmitted bits and demodulates them.
To calculate the error , An *Error Rate Calculation* block is added and its inputs are the bits comming out of the *Random Integer generator* and the bits from the *BPSK Demodulator* 

A *Constellation Diagram* is put at the transmitter and another one is put at the reciever to obtain the scatter plots.

The *Display* block is added to display three values. The first value is the BER, the second value is the number of incorrect bits, and the third value is the total number of bits received.

Also adding a sink *To Workspace* to obtain the BER performance figure.

![BPSK](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/BPSK.PNG?raw=true)

* Configuration
    * Random Integer Generator
        * Set size: 2
    * AWGN Channel
        * Number of bits per symbol: 1
 

* Scatter Plot Before Noise

![BPSK Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/BPSK%20Scatter%20Plot%20Before%20Noise.png?raw=true)

* Scatter Plot After Noise

![BPSK Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/BPSK%20Scatter%20Plot%20After%20Noise.png?raw=true)

* BER Performance

![BPSK BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/BPSK%20BER%20Performance.png)

### QuadriPhase Shift Keying Modulation (QPSK)
QPSK is a modulation scheme that allows one symbol to transfer two bits of data. There are four possible two-bit numbers (00, 01, 10, 11), and consequently we need four phase offsets. We want maximum separation between the phase options, which in this case is 90°.

* Modulation Schematic

The *Random Integer generator* generates random uniformaly distributed integers from range [0,M-1] , M is set to 4 So here it generates (00,01,10,11)
These bits enter the *QPSK Modulator* and then passes through the *AWGN channel*. At the other side the *QPSK Demodulator* takes the transmitted bits and demodulates them.
To calculate the error , An *Error Rate Calculation* block is added and its inputs are the bits comming out of the *Random Integer generator* and the bits from the *QPSK Demodulator* 

A *Constellation Diagram* is put at the transmitter and another one is put at the reciever to obtain the scatter plots.

The *Display* block is added to display three values. The first value is the BER, the second value is the number of incorrect bits, and the third value is the total number of bits received.

Also adding a sink *To Workspace* to obtain the BER performance figure.

![QPSK](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QPSK.PNG?raw=true)

* Configuration
    * Random Integer Generator
        * Set size: 4
    * AWGN Channel
        * Number of bits per symbol: 2 
        
* Scatter Plot Before Noise

![QPSK Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QPSK%20Scatter%20Plot%20Before%20Noise.png?raw=true)

* Scatter Plot After Noise

![QPSK Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QPSK%20Scatter%20Plot%20After%20Noise.png?raw=true)

* BER Performance

![QPSK BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QPSK%20BER%20Performance.png)

### Frequency Shift Keying Modulation (FSK)
* Modulation Schematic

The *Random Integer generator* generates random uniformaly distributed integers from range [0,M-1] , M is set to 8.
These bits enter the *FSK Modulator* and then passes through the *AWGN channel*. At the other side the *FSK Demodulator* takes the transmitted bits and demodulates them.
To calculate the error , An *Error Rate Calculation* block is added and its inputs are the bits comming out of the *Random Integer generator* and the bits from the *FSK Demodulator* 

A *Constellation Diagram* is put at the transmitter and another one is put at the reciever to obtain the scatter plots.

The *Display* block is added to display three values. The first value is the BER, the second value is the number of incorrect bits, and the third value is the total number of bits received.

Also adding a sink *To Workspace* to obtain the BER performance figure.

![FSK](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/FSK.PNG?raw=true)

* Configuration
    * Random Integer Generator
        * Set size: 8
    * AWGN Channel
        * Number of bits per symbol: 3
    * M-FSK Modulation Baseband 
        * M-ary Number: 8
    * M-FSK Demodulation Baseband
        * M-ary Number: 8
        
* Scatter Plot Before Noise

![FSK Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/FSK%20Scatter%20Plot%20Before%20Noise.png?raw=true)

* Scatter Plot After Noise

![FSK Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/FSK%20Scatter%20Plot%20After%20Noise.png?raw=true)

* BER Performance

![FSK BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/FSK%20BER%20Performance.png)

### Quadrature amplitude modulation (QAM)
#### QAM16
* Modulation Schematic

The *Random Integer generator* generates random uniformaly distributed integers from range [0,M-1] , M is set to 16.
These bits enter the *QAM Modulator* and then passes through the *AWGN channel*. At the other side the *QAM Demodulator* takes the transmitted bits and demodulates them.
To calculate the error , An *Error Rate Calculation* block is added and its inputs are the bits comming out of the *Random Integer generator* and the bits from the *QAM Demodulator* 

A *Constellation Diagram* is put at the transmitter and another one is put at the reciever to obtain the scatter plots.

The *Display* block is added to display three values. The first value is the BER, the second value is the number of incorrect bits, and the third value is the total number of bits received.

Also adding a sink *To Workspace* to obtain the BER performance figure.

![QAM16](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM16.PNG?raw=true)

* Configuration
    * Random Integer Generator
        * Set size: 16 
    * AWGN Channel
        * Number of bits per symbol: 4
    * Rectangular QAM Modulator Baseband
        * M-ary Number: 16
    * Rectangular QAM Demodulator Baseband
        * M-ary Number: 16
        
* Scatter Plot Before Noise

![QAM16 Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM16%20Scatter%20Plot%20Before%20Noise.png?raw=true)

* Scatter Plot After Noise

![QAM16 Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM16%20Scatter%20Plot%20After%20Noise.png?raw=true)


* BER Performance

![QAM16 BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM16%20BER%20Performance.png)

#### QAM64

* Modulation Schematic

The *Random Integer generator* generates random uniformaly distributed integers from range [0,M-1] , M is set to 64.
These bits enter the *QAM Modulator* and then passes through the *AWGN channel*. At the other side the *QAM Demodulator* takes the transmitted bits and demodulates them.
To calculate the error , An *Error Rate Calculation* block is added and its inputs are the bits comming out of the *Random Integer generator* and the bits from the *QAM Demodulator* 

A *Constellation Diagram* is put at the transmitter and another one is put at the reciever to obtain the scatter plots.

The *Display* block is added to display three values. The first value is the BER, the second value is the number of incorrect bits, and the third value is the total number of bits received.

Also adding a sink *To Workspace* to obtain the BER performance figure.

![QAM64](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM64.PNG?raw=true)

* Configuration
    * Random Integer Generator
        * Set size: 64
    * AWGN Channel
        * Number of bits per symbol: 6
    * Rectangular QAM Modulator Baseband
        * M-ary Number: 16
    * Rectangular QAM Demodulator Baseband
        * M-ary Number: 16
        
* Scatter Plot Before Noise

![QAM64 Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM64%20Scatter%20Plot%20Before%20Noise.png?raw=true)

* Scatter Plot After Noise

![QAM64 Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM64%20Scatter%20Plot%20After%20Noise.png?raw=true)

* BER Performance

![QAM64 BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM64%20BER%20Performance.png)


# Raised Cosine Simulation

### Binary Phase Shift Keying Modulation (BPSK) with raised cosine
* Modulation Schematic

![BPSK](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/BPSK%20Raised%20Cosine.PNG)
* Configuration
    * Random Integer Generator
        * Set size: 2


* Scatter Plot Before Noise

![BPSK Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/BPSK%20Scatter%20Plot%20Before%20Noise%20Raised%20Cosine.png?raw=true)

* Scatter Plot After Noise

![BPSK Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/BPSK%20Scatter%20Plot%20After%20Noise%20Raised%20Cosine.png?raw=true)

* BER Performance

![BPSK BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/BPSK%20BER%20Performance%20Raised%20Cosine.png)

### QuadriPhase Shift Keying Modulation (QPSK) with raised cosine

* Modulation Schematic

![QPSK](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/QPSK%20Raised%20Cosine.PNG?raw=true)

* Configuration
    * Random Integer Generator
        * Set size: 4
        
* Scatter Plot Before Noise

![QPSK Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/QPSK%20Scatter%20Plot%20Before%20Noise%20Raised%20Cosine.png?raw=true)

* Scatter Plot After Noise

![QPSK Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/QPSK%20Scatter%20Plot%20After%20Noise%20Raised%20Cosine.png?raw=true)

* BER Performance

![QPSK BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/QPSK%20BER%20Performance%20Raised%20Cosine.png)

### Frequency Shift Keying Modulation (FSK) with raised cosine

* Modulation Schematic

![FSK](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/FSK%20Raised%20Cosine.PNG?raw=true)

* Configuration
    * Random Integer Generator
        * Set size: 8
        
* Scatter Plot Before Noise

![FSK Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/FSK%20Scatter%20Plot%20Before%20Noise%20Raised%20Cosine.png?raw=true)

* Scatter Plot After Noise

![FSK Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/FSK%20Scatter%20Plot%20After%20Noise%20Raised%20Cosine.png?raw=true)

* BER Performance

![FSK BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/FSK%20BER%20Performance%20Raised%20Cosine.png)

### Quadrature amplitude modulation (QAM) with raised cosine
#### QAM16 with raised cosine

* Modulation Schematic

![QAM16](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/QAM16%20Raised%20Cosine.PNG?raw=true)

* Configuration
    * Random Integer Generator
        * Set size: 16 
        
* Scatter Plot Before Noise

![QAM16 Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/QAM16%20Scatter%20Plot%20Before%20Noise%20Raised%20Cosine.png?raw=true)

* Scatter Plot After Noise

![QAM16 Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/QAM16%20Scatter%20Plot%20After%20Noise%20Raised%20Cosine.png?raw=true)


* BER Performance

![QAM16 BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/QAM16%20BER%20Performance%20Raised%20Cosine.png)

#### QAM64 with raised cosine

* Modulation Schematic

![QAM64](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/QAM64%20Raised%20Cosine.PNG?raw=true)

* Configuration
    * Random Integer Generator
        * Set size: 64
        
* Scatter Plot Before Noise

![QAM64 Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/QAM64%20Scatter%20Plot%20Before%20Noise%20Raised%20Cosine.png?raw=true)

* Scatter Plot After Noise

![QAM64 Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/QAM64%20Scatter%20Plot%20After%20Noise%20Raised%20Cosine.png?raw=true)

* BER Performance

![QAM64 BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Raised%20Cosine%20Figures/QAM64%20BER%20Performance%20Raised%20Cosine.png)



