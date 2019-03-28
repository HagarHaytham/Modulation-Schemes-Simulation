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
* Modulation Scheme

![BPSK](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/BPSK.PNG?raw=true)

* Configuration
    * Random Integer Generator
        * Set size: 2


* Scatter Plot Before Noise

![BPSK Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/BPSK%20Scatter%20Plot%20Before%20Noise.png?raw=true)

* Scatter Plot After Noise

![BPSK Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/BPSK%20Scatter%20Plot%20After%20Noise.png?raw=true)

* BER Performance

![BPSK BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/BPSK%20BER%20Performance.png)

### QuadriPhase Shift Keying Modulation (QPSK)
* Modulation Scheme

![QPSK](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QPSK.PNG?raw=true)

* Configuration
    * Random Integer Generator
        * Set size: 4
        
* Scatter Plot Before Noise

![QPSK Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QPSK%20Scatter%20Plot%20Before%20Noise.png?raw=true)

* Scatter Plot After Noise

![QPSK Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QPSK%20Scatter%20Plot%20After%20Noise.png?raw=true)

* BER Performance

![QPSK BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QPSK%20BER%20Performance.png)

### Frequency Shift Keying Modulation (FSK)
* Modulation Scheme

![FSK](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/FSK.PNG?raw=true)

* Configuration
    * Random Integer Generator
        * Set size: 8
        
* Scatter Plot Before Noise

![FSK Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/FSK%20Scatter%20Plot%20Before%20Noise.png?raw=true)

* Scatter Plot After Noise

![FSK Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/FSK%20Scatter%20Plot%20After%20Noise.png?raw=true)

* BER Performance

![FSK BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/FSK%20BER%20Performance.png)

### Quadrature amplitude modulation (QAM)
#### QAM16
* Modulation Scheme

![QAM16](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM16.PNG?raw=true)

* Configuration
    * Random Integer Generator
        * Set size: 16 
        
* Scatter Plot Before Noise

![QAM16 Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM16%20Scatter%20Plot%20Before%20Noise.png?raw=true)

* Scatter Plot After Noise

![QAM16 Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM16%20Scatter%20Plot%20After%20Noise.png?raw=true)


* BER Performance

![QAM16 BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM16%20BER%20Performance.png)

#### QAM64
* Modulation Scheme

![QAM64](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM64.PNG?raw=true)

* Configuration
    * Random Integer Generator
        * Set size: 64
        
* Scatter Plot Before Noise

![QAM64 Scatter Plot Before Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM64%20Scatter%20Plot%20Before%20Noise.png?raw=true)

* Scatter Plot After Noise

![QAM64 Scatter Plot After Noise](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM64%20Scatter%20Plot%20After%20Noise.png?raw=true)

* BER Performance

![QAM64 BER Performance](https://github.com/HagarHaytham/Modulation-Schemes-Simulation/blob/master/Figures/QAM64%20BER%20Performance.png)


#Raised Cosine Simulation

