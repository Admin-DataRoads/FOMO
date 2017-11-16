# FOMO
Forward Operating Mesh Observer (FOMO)

An orchestration of different powered-wire and wireless technologies for multichannel Co-MIMO array mesh coordination. 

This exploits the physics of light that dictate at similar given power levels, radios (or light emitters outside human visible range) that transmit at lower frequencies (or wider wavelengths) convey lower data bandwidth but penetrate farther across more mediums with less attenuation. Conversely, radios at higher frequencies (or smaller wavelengths) convey much higher data bandwidth but attenuate in all mediums (including "free" air) at much closer distances. Additionally, wires that convey electrical power can also act as waveguides or direct conductors for broad bands of high data bandwidth capability, such that both data and power can be shared between any generation and storage nodes on the same wired mesh, where shorter wires can convey more data and power with less loss than longer wires.

At the software layer, this exploits recent technology developments in mesh routing and Co-MIMO multi-radio coordination, utilizing hardware backends with new Software Defined x technologies (or SDx, where x is any technology that used to be the sole province of custom hardware and ASIC designs). In the near term, Software Defined Radio (SDR) and Software Defined Network (SDN) technologies are the most useful technologies for novel Co-MIMO mesh coordination. Developments in power microgrid controllers will similarly create Software Defined Power (SDP) systems which can be exploited for microgrid connections between residential renewable power and storage systems.

# Example Mesh
For a more concrete example hybrid SDP-SDN-SDR mesh with multichannel Co-MIMO orchestration, lets define some nodes with existing power wire connections and ISM/unlicensed band sharing technologies:

Solar and small-wind DC generation, and optionally DC battery storage, connected via USB-C 3.2 and 60GHz 802.11ad WiGig at ~10m spacings between nodes on rooftops.

DC to 120VAC inverter nodes, optionally with AC battery storage (eg. Tesla Powerwalls), connected via <=10Gbps ethernet, PoE, ~6GHz 802.11ac Wave2 MU-MIMO WiFi, and HomePlug AV2 ~2Gbps MIMO ~15A powerlines at ~100m spacing between nodes in garages and basements.

~5.8GHz 802.11ac Wave2 MU-MIMO Wifi nodes receiving wired power and data from one of the above node types, and coordinating Co-MIMO radio mesh arrays at about 150m increments. Due to the prevalence of multi-band WiFi COTS routers on the market that can run OpenWRT/LEDE distributions, this node type will likely be combined with the above node types.

~2.4GHz 802.11n Wave2 MU-MIMO Wifi nodes receiving wired power and data from one of the above node types, and coordinating Co-MIMO radio mesh arrays at about 300m increments. Due to the prevalence of multi-band WiFi COTS routers on the market that can run OpenWRT/LEDE distributions, this node type will likely be combined with the above node types.

~900MHz 802.11ah LoRAWAN nodes receiving wireless power and data from one of the above node types, or local micro-generation and battery storage, and coordinating Co-MIMO radio mesh arrays at about 600m increments. Due to the prevalence of low-cost SDR radio designs in the sub-GHz range, this node type will likely be combined with below node types. Gateways to >2GHz radio meshes will likely be combined to above node types.

~150MHz MURS nodes receiving wireless power and data from one of the above node types, or local micro-generation and battery storage, and coordinating Co-MIMO radio mesh arrays at about 3km increments. Due to the prevalence of low-cost SDR radio designs in the sub-GHz range, this node type will likely be combined with below node types. Gateways to >500MHz radio meshes will likely be combined to above node types.

SDR capable nodes will make it possible to coordinate Co-MIMO arrays of radios using above ISM node meshes for licensed and "light licensed" bands -- for example whitespaces, satellite K bands, UAV or balloon nodes, 3.6GHz security meshes, and licensed cellular pico stations or relays. SDR GPS and GLONASS receivers will also allow all nodes to more precisely coordinate unique node IP numbering and antenna phase timing without outside DHCP or NTP style interventions. Nodes lacking any direct GPS or GLONASS signals can be fed precise location and time data by 3 or more neighbor nodes via signal latency based triangulation.
