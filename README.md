# Ceph and VMware
In desem "kleinen" Projekt habe ich ein Ceph Cluster virtuell augesetzt und dieses dann an einen ESXi Host angebunden um VMs zu installieren.

## Getting Started
Bevor ich losgelegt habe, habe ich mir ersteinmal Gedanken gemacht, was ich eigentlich brauche:

- Ceph Cluster
- ESXi Host
- Router
- Verwaltungs PC

Soweit so gut. Da ich jedoch nicht die physische Hardware da hatte um diese Infrastruktur aufzubauen, habe ich mich entschieden das alles virtuell mit
[VirtualBox](https://www.virtualbox.org/) aufzusetzten. 

Ich denke es ist klar warum ich die meisten der o.g. Systeme benötige. Den Router könnte man jedoch als überflüssig betrachten ... was er auch ist, wenn man diesen "nur" als Router verwendet. In meinem Testaufbau soll dieser nämlich hauptsächlich als DHCP- und DNS-Server dienen, sowie das Routing zwischen diesem virtuellen Netzwerk und meinem Heimnetzwerk übernehmen.

Bei der Auswahl des Systems habe ich mich für eine [Sophos XG Home Edition](https://www.sophos.com/de-de/free-tools/sophos-xg-firewall-home-edition) entschieden. Diese ist kostenlos und es gibt sie bereits als fertige .ovf-Datei. Eine [OPNsense](https://opnsense.org/) oder [pfSense](https://www.pfsense.org/) hätten diese Jobs auch übernehmen können, aber ich habe mich für Sophos entschieden, da ich hier mehr Erfahrung habe. 
