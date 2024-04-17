# European Synchrotron Radiation Facility

This project is part of my first internship in 2023 at the ESRF (European Synchrotron Radiation Facility) a particle accelerator located in Grenoble, France.

![storage-Ring-ESRF-500x333](https://github.com/Sathet/3D_Design/assets/147035374/eefe2bc8-713b-46fc-a813-b4953842ae00)

*The storage ring of the European Light Source (ESRF) in Grenoble (Credit: ESRF/Vuedici.org)*

The ESRF is one of the world's most advanced research centers in the fields of materials science and structural biology. It houses a high-energy particle accelerator that generates intense synchrotron radiation (X-ray due to Bremsstrahlung braking radiation). It differ from Collider such as the CERN in Geneva where 2 particles are accelerated to bump into each other. 

![Bremsstrahlung_diagram](https://github.com/Sathet/3D_Design/assets/147035374/30d0bcc9-fba5-40af-8179-80214b4f077f)

*Diagram of Bremsstrahlung X-ray production*

This radiation is utilized by researchers worldwide to study the structure and properties of materials at the atomic and molecular scale. Work conducted at the ESRF has applications in numerous fields including medicine, pharmacology, materials physics, chemistry, and biology, contributing to significant scientific advancements and technological innovations.

# Project context

Some samples are studied at high pressure and high temperature for various purposes (phase diagram, etc.). It is therefore essential to have precise knowledge of these two characteristics of the sample, and we need instruments to measure them. The aim of this project is to develop a new instrument called PRL (Pressure Ruby Luminescence) to measure pressure.

This is a very interesting instrument that uses properties of ruby and a bunch of optics to work.

## Theory

>Ruby is chromium-doped corundum (Al2O3). The Cr3+ in corundum's lattice forms an octahedra with surrounding oxygen ions. The octahedral crystal field together with spin-orbital interaction results in different energy levels. Once 3d electrons in Cr3+ are energized by lasers, the excited electrons would go to 4T2 and 2T2 levels. Later they return to 2E levels and the R1, R2 lines come from luminescence from 2E levels to 4A2 ground level.[2] The energy difference of 2E levels are 29 cm−1, corresponding to the splitting of R1, R2 lines at 1.39 nm. [Wikipédia](https://en.wikipedia.org/wiki/Ruby_pressure_scale)

To sum up the paragraph above, when ruby is excited by a laser, the Chromium ions in corundum (Al2O3) cause energy level transitions that result in the emission of visible light.

What interests us here is that the wavelength of the visible light emitted by ruby shifts according to the pressure experienced by the ruby.

<img width="225" alt="Ruby_fluorescence_spectra_at_1atm,_2 23_GPa_and_4_GPa" src="https://github.com/Sathet/3D_Design/assets/147035374/2f76e357-7fa7-4a94-98d2-2d604cc48ff5">

*fluorescence spectrum of ruby*

## Constraints and specifications

Knowing this, we need an instrument (PRL) capable of observing the ruby present in the sample chamber. Excite it with a laser and then measure the wavelength it emits with a spectrometer. The temperature parameter and the wavelength of the measured lines are entered into an internal software. Then it returns the pressure undergone by the sample.

The Pressure Ruby Luminescence on [ID24 Beamline](https://www.esrf.fr/home/UsersAndScience/Experiments/MEx/ID24.html) is old, and doesn't offer enough flexibility when it comes to measuring pressure. Moreover, it's difficult and time-consuming to align the laser and the camera. Therefor, we could buy a PRL on the market. However, this is very expensive (~€30,000). The aim is to design one ourselves, using Thorlabs parts (a supplier of optical equipment) to save money. As a PRL is mainly an optical system, lenght travel by light aren't a problem. So we can arrange to have certain elements in a certain advantageous position. The beamline are quite full of experimental equipment. The space occupied by a device is a critical factor.

It is necessary to be able to move quickly from optical visualisation of the sample (microscope) to pressure measurement (laser/spectrometer).

#  Design 

With these criteria, we imagine a device with a folding mirror, enabling to switched quickly from microscope to PRL position.

My work on solidworks start here and the idea is to use thorlab 3D model available on their website to design the PRL. This phase of work in SolidWorks is important to ensure that the right parts are purchased in the right quantities and that the PRL is feasible. The difficulty was to keep in mind the optical constraints of the system (focal length of the lenses, transmission/absorption wavelength of the beam splitters/dichroic mirror) while working on its mechanical aspect.

The first version of the PRL is an assembly of 60 Thorlabs component.

![PRL_V1](https://github.com/Sathet/3D_Design/assets/147035374/7ddbcf18-9479-4213-b0f9-0d551ae029fd)

*PRL assembly V1*

Many changes were made between the first version in SolidWorks and the final assembly. Note that the final assembly was obtained experimentally. For example, we interchanged the position of the camera and the spectrometer input, added a lens to focus the light coming out of the LED and machined the metal part on which the system rests.

![PRL_VF](https://github.com/Sathet/3D_Design/assets/147035374/b49b665a-4007-4a77-9487-215bf0a17863)

*PRL assembly VF*

I can't share the 3D file assembly on internet, this could potentially infringe upon intellectual property or confidentiality agreements.

# Test

Assembling the final version of the PRL initiates the testing phase. To accomplish this, the laser aligns with the camera, a process achieved by adjusting the various translating lens mounts (CXY1A) on the laser, camera, and spectrometer input. Once alignment is achieved, the system operates in PRL mode. A Ruby sample positions at the output of the lens, followed by laser excitation. Subsequently, the spectrometer collects the spectrum of Ruby's luminescence.

![PRL_dst_microscope](https://github.com/Sathet/3D_Design/assets/147035374/4df26d18-67de-4aff-b1dc-f07287db8c53)
![PRL_dst_pression](https://github.com/Sathet/3D_Design/assets/147035374/e649a28e-41b9-4655-9238-50720f6ad10c)









