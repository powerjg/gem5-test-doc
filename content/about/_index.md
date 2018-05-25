---
title: "About"
date: 2018-05-13T18:51:37-04:00
draft: false
weight: 60
---

#### About
The gem5 simulator is a modular platform for computer-system
architecture research, encompassing system-level architecture as
well as processor microarchitecture.

#### Features
##### Multiple interchangeable CPU models.
gem5 provides four interpretation-based CPU models: a simple one-CPI CPU; a
detailed model of an in-order CPU, and a detailed model of an out-of-order CPU.
These CPU models use a common high-level ISA description. In addition, gem5
features a KVM-based CPU that uses virtualisation to accelerate simulation.

##### [Event-driven memory system.](Media:2015_ws_02_hansson_gem5_workshop_2015.pdf "wikilink")
gem5 features a detailed, event-driven memory system including caches,
crossbars, snoop filters, and a fast and accurate DRAM controller model, for
capturing the impact of current and emerging memories, e.g. LPDDR3/4/5, DDR3/4,
GDDR5, HBM1/2/3, HMC, WideIO1/2.  The components can be arranged flexibly,
e.g., to model complex multi-level non-uniform cache hierarchies with
heterogeneous memories.

##### [Multiple ISA support](Supported Architectures "wikilink")
gem5 decouples ISA semantics from its CPU models, enabling effective support
of multiple ISAs. Currently gem5 supports the Alpha, ARM, SPARC, MIPS, POWER,
RISC-V and x86 ISAs. However, all guest platforms aren't
supported on all host platforms (most notably Alpha requires
little-endian hardware). 

##### Homogeneous and heterogeneous multi-core
The CPU models and caches can be combined in arbitrary topologies, creating
homogeneous, and heterogeneous multi-core systems. A MOESI snooping cache
coherence protocol keeps the caches coherent.

##### Full-system capability
  - **Alpha**: gem5 models a DEC Tsunami system in sufficient detail
        to boot unmodified Linux 2.4/2.6, FreeBSD, or L4Ka::Pistachio.
        We have also booted HP/Compaq's Tru64 5.1 operating system in
        the past, though we no longer actively maintain that capability.
  - **ARM**: gem5 can model up to 64 (heterogeneous) cores of a
        Realview ARM platform, and boot [unmodified
        Linux](ARM_Linux_Kernel "wikilink") and
        [Android](Android_Marshmallow "wikilink") with a combination of
        in-order and out-of-order CPUs. The ARM implementation supports
        32 or 64-bit kernels and applications.
  - **SPARC**: The gem5 simulator models a single core of a
        UltraSPARC T1 processor with sufficient detail to boot Solaris
        in a similar manner as the Sun T1 Architecture simulator tools
        (building the hypervisor with specific defines and using the
        HSMID virtual disk driver).
  - **x86**: The gem5 simulator supports a standard PC platform

##### Application-only support
In application-only (non-full-system) mode, gem5 can execute a variety of
architecture/OS binaries with Linux emulation.

##### Multi-system capability
Multiple systems can be instantiated within a single simulation process. In
conjunction with full-system modeling, this feature allows simulation of entire
client-server networks.

##### Power and energy modeling
gem5’s objects are arranged in OS-visible power and clock domains, enabling a
range of experiments in power- and energy-efficiency. With out-of-the-box
support for OS-controller Dynamic Voltage and Frequency (DVFS) scaling, gem5
provides a complete platform for research in future energy-efficient systems.
See [how to run your own DVFS experiments](Running_gem5#Experimenting_with_DVFS
"wikilink").


##### [A trace-based CPU](TraceCPU "wikilink")
CPU model that plays back elastic traces, which are dependency and timing
annotated traces generated by a probe attached to the out-of-order CPU model.
The focus of the Trace CPU model is to achieve memory-system (cache-hierarchy,
interconnects and main memory) performance exploration in a fast and reasonably
accurate way instead of using the detailed CPU model.

##### [Co-simulation with SystemC.](Media:2015_ws_09_2015-06-14_Gem5_ISCA.pptx "wikilink")
gem5 can be included in a SystemC simulation, effectively running as a
thread inside the SystemC event kernel, and keeping the events and timelines
synchronized between the two worlds. This functionality enables the gem5
components to interoperate with a wide range of System on Chip (SoC) component
models, such as interconnects, devices and accelerators. A wrapper for SystemC
Transaction Level Modelling (TLM) is provided.

##### [A NoMali GPU model.](Media:2015_ws_04_ISCA_2015_NoMali.pdf "wikilink")
gem5 comes with an integrated NoMali GPU model that is compatible with the
Linux and Android GPU driver stack, and thus removes the need for software
rendering. The NoMali GPU does not produce any output, but ensures that
CPU-centric experiments produce representative results.


#### Licensing
The gem5 simulator is released under a Berkeley-style open source license.
Roughly speaking, you are free to use our code however you wish, as long as you
leave our copyright on it. For more details, see the LICENSE file included in
the source download. Note that the portions of gem5 derived from other sources
are also subject to the licensing restrictions of the original sources.


#### Publications
A list of [publications](publications "wikilink") using the gem5
simulator is also available. Please append to the list if you publish a
paper using gem5.

If you use gem5 in your research, we would appreciate a citation to,
[*The gem5 Simulator,*](http://dx.doi.org/10.1145/2024716.2024718) from
the May 2011 issue of ACM SIGARCH Computer Architecture News in any
publications you produce. In addition, please [cite the specific
features of gem5](Publications "wikilink") that you are using as part of
your research.

#### Acknowledgments

The gem5 simulator has been developed with generous support from several
sources, including the National Science Foundation, AMD, ARM,
Hewlett-Packard, IBM, Intel, MIPS, and Sun. Individuals working on gem5
have also been supported by fellowships from Intel, Lucent, and the
Alfred P. Sloan Foundation. This material is based upon work supported
by the National Science Foundation under the following grants:
CCR-0105503, CCR-0219640, CCR-0324878, EAI/CNS-0205286, and CCR-0105721.

Any opinions, findings and conclusions or recommendations expressed in
this material are those of the author(s) and do not necessarily reflect
the views of the National Science Foundation (NSF) or any other sponsor.
