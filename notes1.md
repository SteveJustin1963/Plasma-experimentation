# explain a microwave-induced plasma system for experimentation, 
referencing a New Atlas article about a microwave air plasma thruster. comprehensive technical breakdown.                                                   
                                                                                                                                                                            
Microwave-Induced Plasma (MIP) systems, also called Microwave Plasma Thrusters (MPT) or Microwave Air Plasma Thrusters, work on the      
principle of using electromagnetic energy in the microwave frequency range to ionize a gas and create plasma, which can then be accelerated for thrust.                     
                                                                                                                                                                            
Key components and physics involved:                                                                                                                                        
                                                                                                                                                                            
1. **Plasma generation**:                                                                                                                                                   
   - Microwave frequencies typically 2.45 GHz (industrial, scientific, medical band) - same as kitchen microwave magnetrons                                                 
   - Free electrons absorb microwave energy through inverse bremsstrahlung                                                                                                  
   - These energetic electrons collide with neutral molecules, ionizing them                                                                                                
   - Creates a self-sustaining plasma discharge                                                                                                                             
                                                                                                                                                                            
2. **Electromagnetic wave-plasma interaction**:                                                                                                                             
   - The plasma has a characteristic plasma frequency: ω_p = √(n_e e²/ε_0 m_e)                                                                                              
   - For microwaves to interact with plasma, the wave frequency must be above the plasma frequency (or use a special configuration)                                         
   - Electron-neutral collision frequency matters for energy coupling                                                                                                       
   - The plasma acts as a load for the microwave circuit                                                                                                                    
                                                                                                                                                                            
3. **Heating mechanisms**:                                                                                                                                                  
   - Ohmic/resistive heating                                                                                                                                                
   - Stochastic (collisionless) heating                                                                                                                                     
   - Resonance absorption                                                                                                                                                   
                                                                                                                                                                            
4. **For thrust**:                                                                                                                                                          
   - Pressure builds up due to heating                                                                                                                                      
   - Nozzle expansion or magnetic nozzle for thrust                                                                                                                         
   - Air-breathing (using atmospheric air) vs. stored propellant                                                                                                            
                                                                                                                                                                            
5. **Key challenges for the air-breathing version**:                                                                                                                        
   - Maintaining plasma in supersonic flow                                                                                                                                  
   - Air is a complex gas (N2, O2) - dissociation and recombination issues                                                                                                  
   - Power requirements enormous for aircraft-scale thrust                                                                                                                  
   - Magnetron efficiency (~70%) but overall system efficiency low                                                                                                          
   - Atmospheric pressure operation                                                                                                                                         
   - Thermal management                                                                                                                                                     
                                                                                                                                                                            
# math/physics:                                                                                                                                        
                                                                                                                                                                            
**Plasma frequency**:                                                                                                                                                       
$$\omega_p = \sqrt{\frac{n_e e^2}{\varepsilon_0 m_e}}$$                                                                                                                     
                                                                                                                                                                            
For 2.45 GHz:                                                                                                                                                               
$$f_p = \frac{\omega_p}{2\pi} = 9\sqrt{n_e}$$                                                                                                                               
where n_e is in m^-3                                                                                                                                                        
                                                                                                                                                                            
For 2.45 GHz, n_e < 7.5 × 10^16 m^-3 (cutoff density)                                                                                                                       
                                                                                                                                                                            
**Power balance**:                                                                                                                                                          
Energy input: microwave power P_in                                                                                                                                          
Energy losses: radiation, convection, recombination, etc.                                                                                                                   
                                                                                                                                                                            
**Thrust calculation**:                                                                                                                                                     
For a thermal-type thruster:                                                                                                                                                
$$F = \dot{m} v_e = \dot{m} \sqrt{\frac{2\gamma}{\gamma-1} \frac{RT}{M}\left[1 - \left(\frac{p_e}{p_c}\right)^{(\gamma-1)/\gamma}\right]}$$                                 
                                                                                                                                                                            
But this is a low-temperature plasma, so thermal thrust model might not apply directly.                                                                                     
                                                                                                                                                                            
For momentum-based:                                                                                                                                                         
$$F = \dot{m} v_{exit}$$                                                                                                                                                    
                                                                                                                                                                            
**Specific impulse**:                                                                                                                                                       
$$I_{sp} = \frac{F}{\dot{m} g_0} = \frac{v_e}{g_0}$$                                                                                                                        
                                                                                                                                                                            
**Power-thrust relationship**:                                                                                                                                              
$$P = \frac{1}{2}\dot{m} v_e^2$$                                                                                                                                            
$$I_{sp} = \frac{2P}{F g_0}$$                                                                                                                                               
$$F = \frac{2P}{I_{sp} g_0}$$                                                                                                                                               
                                                                                                                                                                            
This shows the trade-off: for given power, higher Isp means less thrust but more efficient propellant use.                                                                  
                                                                                                                                                                            
For atmospheric air-breathing plasma thrusters, the key issue is:                                                                                                           
- Power density: You need MW-class power for aircraft thrust                                                                                                                
- A 100 kN thrust system would need... let me calculate                                                                                                                     
- If v_e ≈ 1000-2000 m/s, then for 100 kN: P = 0.5 × ṁ × v² where ṁ × v = 100,000                                                                                           
- So ṁ × v² = 200,000 × v ≈ 200,000 × 1500 = 300 MW                                                                                                                         
- That's way too much power                                                                                                                                                 
                                                                                                                                                                            
Even a small aircraft (10 kN thrust): still need tens of MW                                                                                                                 
                                                                                                                                                                            
Current aircraft have ~50-100 MW total power, but most goes to propulsion. So you can't take power away from engines.                                                       
                                                                                                                                                                            
This is why these systems are limited to very small drones or satellites.                                                                                                   
                                                                                                                                                                            
For lab experiments, the experimental setup typically involves:                                                                                                             
                                                                                                                                                                            
1. **Microwave source**:                                                                                                                                                    
   - Magnetron (cheap, ~70% efficient) - usually 2.45 GHz                                                                                                                   
   - Klystron or solid-state (more expensive, more efficient)                                                                                                               
   - Power: 100 W to 100 kW typical                                                                                                                                         
                                                                                                                                                                            
2. **Waveguide system**:                                                                                                                                                    
   - WR-340 or WR-284 waveguide for 2.45 GHz                                                                                                                                
   - Tuner (3-stub or sliding short) for impedance matching                                                                                                                 
   - Circulator with dummy load to protect source from reflected power                                                                                                      
   - Directional couplers to measure forward/reflected power                                                                                                                
                                                                                                                                                                            
3. **Plasma chamber**:                                                                                                                                                      
   - Quartz or boron nitride tube (transparent to microwaves)                                                                                                               
   - Gas inlet (or air intake)                                                                                                                                              
   - Pressure gauges                                                                                                                                                        
   - Optical emission spectroscopy (OES) for diagnostics                                                                                                                    
   - Langmuir probe for electron temperature/density                                                                                                                        
                                                                                                                                                                            
4. **Diagnostics**:                                                                                                                                                         
   - OES: identify species, measure rotational/vibrational temperatures                                                                                                     
   - Microwave interferometry for electron density                                                                                                                          
   - Schlieren imaging for gas density                                                                                                                                      
   - Mass spectrometry for gas composition                                                                                                                                  
   - Thrust stand for thrust measurement                                                                                                                                    
   - Calorimetry for energy balance                                                                                                                                         
                                                                                                                                                                            
5. **Safety**:                                                                                                                                                              
   - Microwave shielding (Faraday cage)                                                                                                                                     
   - Interlocks on door/access                                                                                                                                              
   - RF radiation monitoring                                                                                                                                                
   - Ventilation for any toxic byproducts (ozone, NOx)                                                                                                                      
                                                                                                                                                                            
6. **Measurement quantities**:                                                                                                                                              
   - S-parameters (forward/reflected power)                                                                                                                                 
   - Plasma temperature (T_e, T_gas, T_vib, T_rot)                                                                                                                          
   - Electron density                                                                                                                                                       
   - Thrust force                                                                                                                                                           
   - Specific impulse                                                                                                                                                       
   - Energy efficiency η = (1/2) ṁ v_e² / P_in                                                                                                                              
                                                                                                                                                                            
# physics of microwave-plasma coupling:                                                                                                             
                                                                                                                                                                            
**Dielectric breakdown**:                                                                                                                                                   
- Free electrons oscillate in the microwave field                                                                                                                           
- When field is strong enough, electrons gain enough energy between collisions to ionize neutrals                                                                           
- This is the "breakdown" threshold                                                                                                                                         
                                                                                                                                                                            
**Microwave penetration depth (skin depth)**:                                                                                                                               
In plasma, EM waves are attenuated. The skin depth is:                                                                                                                      
$$\delta = \frac{c}{\omega_p} \sqrt{\frac{2}{1 - \omega_p^2/\omega^2}}$$                                                                                                    
For over-dense plasma (ω < ω_p), waves are reflected.                                                                                                                       
                                                                                                                                                                            
**Power absorption**:                                                                                                                                                       
- Collisional: P = (1/2) σ |E|² where σ is plasma conductivity                                                                                                              
- Collisionless: stochastic heating, anomalous skin effect                                                                                                                  
                                                                                                                                                                            
**Thermal non-equilibrium**:                                                                                                                                                
- T_e (electron temperature): 1-10 eV (10,000-100,000 K)                                                                                                                    
- T_gas (gas temperature): 300-2000 K (low, hence "low-temperature plasma")                                                                                                 
- Heavy particles stay cold because mass mismatch with electrons                                                                                                            
- This is the key advantage - plasma without melting the chamber                                                                                                            
                                                                                                                                                                            
**Plasma chemistry in air**:                                                                                                                                                
- N2 dissociation                                                                                                                                                           
- O2 dissociation                                                                                                                                                           
- Formation of NO, NO2, O3                                                                                                                                                  
- Vibrational excitation                                                                                                                                                    
- N2 metastable states                                                                                                                                                      
- Recombination at walls                                                                                                                                                    
                                                                                                                                                                            
**Magnetic nozzle** (if used):                                                                                                                                              
- Plasma expands along B field lines                                                                                                                                        
- Converts thermal energy to directed kinetic energy                                                                                                                        
- No physical contact with plasma                                                                                                                                           
- Some plasma detaches via various mechanisms (still active research)                                                                                                       
                                                                                                                                                                            
                                                                                                                                                                            
# Typical experiment layout:                                                                                                                                                  
- Microwave source (magnetron 1-2 kW at 2.45 GHz) → circulator → dummy load → 3-stub tuner → applicator (plasma chamber) → load                                             
- Or via coaxial cable with antenna inside chamber                                                                                                                          
- Gas flow controller (mass flow controller)                                                                                                                                
- Vacuum pump (if low pressure)                                                                                                                                             
- Pressure sensors                                                                                                                                                          
- Optical fiber → spectrometer                                                                                                                                              
- Langmuir probe (movable)                                                                                                                                                  
- Microwave probe for interferometry                                                                                                                                        
- Thrust stand (if measuring thrust)                                                                                                                                        
- Data acquisition system                                                                                                                                                   
                                                                                                                                                                            
                                                                                                                                                                            
1. System overview and basic principle                                                                                                                                      
2. Physics of microwave-plasma coupling (with math)                                                                                                                         
3. Components of the system                                                                                                                                                 
4. Experimental setup                                                                                                                                                       
5. Diagnostics                                                                                                                                                              
6. Performance metrics                                                                                                                                                      
7. Challenges (especially for air-breathing aviation version)                                                                                                               
8. Mathematical scaling for thrust                                                                                                                                          
                                                                                                                                                                            
                                                                                                                                                                            
# Microwave-Induced Plasma (MIP) Systems: Theory, Experiment & Aviation Context                                                                                             

## 1. Operating Principle (from the article)

The New Atlas article describes an **air-breathing microwave plasma thruster**. The cycle is:

```
Air (intake) → compression → ionization (seed plasma) → microwave heating → 
high-T plasma → nozzle expansion → thrust
```

Unlike chemical rockets or even ion engines, **the energy source (microwaves) is decoupled from the propellant (air)**. The propellant is essentially free.

---

## 2. Core Physics: How Microwaves Make Plasma

### 2.1 Plasma Frequency

A plasma oscillates at the **electron plasma frequency**:

$$\boxed{\omega_p = \sqrt{\frac{n_e e^2}{\varepsilon_0 m_e}} \quad \Leftrightarrow \quad f_p \approx 9\,\sqrt{n_e}\,\text{Hz, with } n_e \text{ in m}^{-3}}$$

For microwaves to **propagate through** the plasma, the wave frequency must exceed the plasma frequency:

$$\omega_{MW} > \omega_p \quad \Rightarrow \quad n_e < n_{\text{crit}} = \frac{\varepsilon_0 m_e \omega_{MW}^2}{e^2}$$

| Microwave | 2.45 GHz (magnetron) | 915 MHz (industrial) | 5.8 GHz |
|-----------|----------------------|----------------------|---------|
| $n_{crit}$ (m⁻³) | $7.5 \times 10^{16}$ | $1.0 \times 10^{16}$ | $4.2 \times 10^{17}$ |

Above the critical density, microwaves **reflect** (over-dense plasma) — this is the same physics as ionospheric reflection of radio waves.

### 2.2 Microwave Energy Deposition

Free electrons in the EM field oscillate at the driving frequency. Energy transfer to the plasma occurs through:

**Collisional (ohmic) heating** — dominant at moderate pressures:
$$P_{abs} = \frac{1}{2}\sigma |E|^2 = \frac{n_e e^2 \nu_{en}}{2 m_e(\omega^2 + \nu_{en}^2)} |E|^2 \cdot V$$

where $\nu_{en}$ is the electron–neutral collision frequency.

**Stochastic (collisionless) heating** — important at low pressure:
Electrons reflecting from the oscillating sheath are heated by the Doppler effect.

### 2.3 Breakdown Threshold

For sustained ionization, the field must give each electron enough energy between collisions to ionize one neutral. The threshold follows a **Paschen-like** law, with 
a minimum near:

$$p \cdot d \sim \text{const} \quad \text{(for a given frequency)}$$

For air at 2.45 GHz, breakdown typically requires $E \gtrsim 10^4$–$10^5$ V/m depending on pressure.

### 2.4 Non-Equilibrium (the "magic" of these plasmas)

The most important property: **the plasma is non-thermal**.

$$T_e \sim 1\text{–}5~\text{eV} \quad (10{,}000\text{–}50{,}000~\text{K})$$
$$T_{gas} \sim 300\text{–}2000~\text{K}$$

The gas stays cool because of the **mass mismatch**: an electron transfers at most $\sim 4 m_e/m_n \ll 1$ of its energy per elastic collision with a heavy particle. 
So the walls and bulk gas remain cold, while electrons are hot enough to sustain ionization and dissociation. This is why a quartz tube survives.

---

## 3. System Architecture

### 3.1 Component Block Diagram

```
┌────────────┐   ┌───────────┐   ┌──────┐   ┌─────────┐   ┌──────────────┐
│  Magnetron │──▶│ Circulator│──▶│ 3-stub│──▶│ Quartz  │──▶│ Matching     │
│  (1–2 kW)  │   │ + dummy   │   │ tuner │   │ tube +  │   │ load / plume │
│  2.45 GHz  │◀──│   load    │   │       │   │ plasma  │   │              │
└────────────┘   └───────────┘   └──────┘   └────────┘   └──────────────┘
       │              │              │            │
       ▼              ▼              ▼            ▼
    Forward/     Reflected       Impedance     Diagnostics
    reflected    power           matching
    power        monitor
```

### 3.2 Key Components

| Component | Function | Typical Choice |
|-----------|----------|----------------|
| **Magnetron** | Microwave source | 2.45 GHz, 1–2 kW (e.g., MKS/Alter TM-110 or similar) |
| **Circulator + dummy load** | Protects magnetron from reflected power | Ferrite circulator, water load |
| **3-stub tuner / sliding short** | Matches waveguide impedance to plasma | WR-340 waveguide, brass stubs |
| **Directional couplers** | Measure forward/reflected power | –30 to –50 dB couplers |
| **Quartz/BN tube** | Plasma containment, MW-transparent | OD 10–30 mm |
| **Igniter (Tesla coil / spark)** | Seeds initial electrons | High-voltage pulse |
| **Mass flow controller** | Regulates gas (if bottled) or air intake | 0.1–10 slpm |
| **Thrust stand** | Direct thrust measurement | Pendulum + LVDT, or load cell |
| **Spectrometer** | Optical emission diagnostics | Echelle or Czerny–Turner, fiber-coupled |
| **Langmuir probe** | $T_e$, $n_e$ | Tungsten wire, motorized |
| **Microwave interferometer** | Line-averaged $n_e$ | Separate klystron + horn antennas |
| **Schlieren/shadowgraph** | Gas density / shock visualization | High-speed camera + knife edge |
| **Calorimeter** | Energy balance (losses) | Cooling water ΔT on the chamber |

### 3.3 Safety Infrastructure

Because you're running 1 kW+ of microwave power in a lab:

- **Faraday cage / shielded room** (≥80 dB attenuation, 1.5–2× line frequency harmonics)
- **Door interlocks** (microwave switches)
- **RF leakage monitor** (Narda-type survey meter)
- **Ozone & NOₓ venting** (air plasma produces both, OSHA/NIOSH limits: O₃ < 0.1 ppm, NO₂ < 5 ppm)
- **Waveguide pressurization** with SF₆ or dry air to prevent arcing at high power

---

## 4. Experimental Methodology

### 4.1 Typical Experimental Campaign

A researcher would sweep the following parameters:

| Parameter | Typical Range | Effect |
|-----------|---------------|--------|
| Air mass flow $\dot m$ | 0.1 – 5 g/s | Changes residence time, plasma density |
| Microwave power $P_{MW}$ | 0.5 – 2 kW | Sets $T_e$, degree of ionization |
| Pressure | 1 mbar – 1 atm | Determines collisionality regime |
| Nozzle geometry | Conical, de Laval, magnetic | Affects thrust conversion |
| Pulse mode | CW, pulsed (duty cycle) | Affects thermal load, dynamics |

### 4.2 Diagnostics You Actually Run

**(a) Energy balance** (essential — tells you how much MW actually enters the plasma):
$$P_{forward} - P_{reflected} = P_{abs} = P_{plasma,thrust} + P_{loss}$$
You measure forward/reflected power with directional couplers, calorimetry on the gas stream, and radiative losses via OES (absolute intensity, calibrated with a 
tungsten ribbon lamp).

**(b) Electron temperature and density:**
- Langmuir probe: gives $T_e$, $n_e$, $V_p$ locally. Needs care in MW fields — use **rf-choking** filters (chokes at 2.45 GHz, e.g., resonant λ/4 stubs).
- Microwave interferometry: line-averaged $n_e$ via phase shift $\Delta\phi = \frac{\omega}{2 c n_c} \int n_e \, dz$.
- OES: Boltzmann plot of multiple lines (e.g., N II, O I) gives $T_e$ ≈ excitation temperature.

**(c) Gas temperature:**
- O₂ or N₂ rotational temperature from molecular band spectra (e.g., N₂ 2⁺ system at 380 nm) → gas temperature.
- Doppler broadening of atomic lines (Hα) for heavy-particle temperature.
- IR pyrometry on walls (if you want wall heat flux).

**(d) Thrust measurement:**
The most difficult. Standard techniques:
- **Hanging pendulum** with LVDT displacement → force from $\Delta x = F/k$.
- **Torsion balance** with optical lever.
- **Direct load cell** (less sensitive, but robust).
- Sub-µN resolution requires vibration isolation and thermal drift correction.

**(e) Velocity / specific impulse:**
- **Time-of-flight** between two Langmuir probes separated by distance $L$ along the plume.
- **Pitot probe + static pressure** → Mach number → $v_e$.
- **Doppler shift** of plasma emission lines (often the cleanest).
- $I_{sp} = v_e / g_0$.

### 4.3 Typical Numbers Reported in Literature

| Quantity | Lab value (1 kW class) |
|----------|------------------------|
| $n_e$ | 10¹⁶ – 10¹⁸ m⁻³ |
| $T_e$ | 1 – 5 eV |
| $T_{gas}$ | 500 – 2000 K |
| Ionization fraction | 10⁻⁵ – 10⁻³ |
| Thrust | 10 – 100 mN (lab) |
| $I_{sp}$ | 200 – 1500 s |
| Power–thrust efficiency $\eta = F^2/(2\dot m P)$ | 5 – 30 % |

---

## 5. Theoretical Performance Ceiling (Why Aircraft Is Hard)

### 5.1 Thrust–Power–Isp Relationship

For any propulsive device (rocket equation, ideal gas):

$$F = \dot m \, v_e, \qquad P = \tfrac{1}{2}\dot m v_e^2 + \text{losses}$$

Eliminating $\dot m$:

$$\boxed{\;F = \frac{2P}{v_e} = \frac{2P}{I_{sp}\,g_0}\;}$$

So **for fixed power, thrust scales inversely with Isp**. A thruster optimized for high Isp (efficient, low propellant use) gives small thrust; a thruster optimized 
for high thrust has low Isp.

### 5.2 The Hard Numbers for an Aircraft

Assume a moderately optimistic $I_{sp} = 1500$ s and $\eta = 30\%$:

| Aircraft | Cruise thrust | Power needed | Comment |
|----------|---------------|--------------|---------|
| Quadcopter drone (10 kg) | ~20 N | $P = F g_0 I_{sp}/(2\eta) \approx 0.5$ **MW** | OK at 30% efficiency |
| Small Cessna-class | ~5 kN | ~125 **MW** | Roughly the power output of one jet engine |
| Airliner (Boeing 737) | ~120 kN | ~3 **GW** | Greater than the entire U.S. power grid output |

**Conclusion:** Even at the most optimistic efficiencies, an air-breathing plasma thruster would need a **dedicated MW–GW class power source on board**, in addition 
to the air-breathing propulsion. Today's best batteries store ~250 Wh/kg; you'd need ~10⁵ kg of batteries for a 5 kN cruise. So **the article's device is, at best, a 
drone propulsion concept** — not an airliner one.

### 5.3 Other Physics Hurdles

1. **Air is not xenon.** Dissociation of N₂ (9.8 eV) and O₂ (5.1 eV) consumes microwave power without contributing to thrust. Recombination releases heat in the 
nozzle, choking flow.

2. **Recombination is slow.** In low-T plasma, atomic N and O recombine on **walls**, not in the plume. So you get chemical afterburning on the nozzle/walls — 
corrosion, thermal load, and reduced efficiency.

3. **Nozzle survivability.** Hot plasma + O atoms = aggressive oxidation. Refractory metals melt; water-cooled nozzles are heavy.

4. **Magnetron is cheap but inefficient** and noisy (line harmonics need filtering). Solid-state GaN microwave sources are improving but still expensive at >1 kW.

5. **Plasma stability.** Air is a molecular gas; complex chemistry (N₂, O₂, NO, NO₂, O₃, N₂O, N, O) makes discharge prone to constriction, filamentation, and 
glow-to-arc transitions.

---

## 6. Scaled-Down: What a Lab Setup Actually Looks Like

If you wanted to reproduce the article's experiment at small scale (no thrust measurement, just plasma physics), the bill of materials is roughly:

| Item | Approx. cost (USD) |
|------|-------------------:|
| 1.5 kW, 2.45 GHz magnetron head + HV supply | 1,500 – 4,000 |
| WR-340 waveguide plumbing, tuner, circulator, dummy load | 2,000 – 5,000 |
| Directional couplers + power meters | 1,000 – 2,000 |
| Quartz tube + chamber + gas fittings | 500 – 1,500 |
| Vacuum pump + MFC + Baratron | 3,000 – 8,000 |
| Langmuir probe + stepper | 2,000 – 5,000 |
| Fiber-coupled spectrometer (e.g., Avantes/Ocean) | 4,000 – 15,000 |
| Faraday cage with interlocks | 5,000 – 20,000 |
| Data acquisition (fast digitizer) | 2,000 |
| **Total (rough)** | **$25k – $60k** |

---

## 7. Key Takeaways

1. **The physics is real.** Microwave air plasma has been studied for decades (EHF-series devices, MIPT concepts at European groups, work by Takahashi, Charles, 
Pottinger's group, etc.). Lab thrusters producing 10–100 mN are reproducible.

2. **The article's device is essentially a thermal plasma thruster** with a high-temperature, MW-heated working fluid. The physics of "microwave heats the air → it 
expands out the back" is the same as a resistojet or arcjet, just with a different heating mechanism.

3. **The bottleneck is power, not plasma physics.** The "energy in = air goes fast" idea is limited by what you can carry. A solar-powered stratospheric drone (~10 
kW) might work; a passenger jet is a fantasy without a compact fusion reactor.

4. **The most promising near-term use is for satellites using atmospheric drag makeup** (very low thrust, very high $I_{sp}$ in low Earth orbit air-breathing mode) — 
a niche where the math actually closes.

---

further work:
- **Magnetic nozzle physics** (the next step beyond a simple thermal expansion)?
- **Specific data analysis** for a Langmuir probe in an MIP?
- **The chemistry of air plasmas** (N₂, O₂, NOₓ pathways)?
- **Pulsed operation and time-resolved diagnostics**?
