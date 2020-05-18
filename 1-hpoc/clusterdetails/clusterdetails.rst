.. _clusterdetails:

------------------------
Workshop Cluster Details
------------------------

Cluster Hardware Details
++++++++++++++++++++++++


**Für den Virtual Solutions Workshop wurden zwei Systeme mit 4 Nodes in 2 Höheneinheiten reserviert:**

.. figure:: images/cluster3060g5a.png

.. note::
  Bedenken Sie bitte, dass diese Testumgebung zum nicht zwangsläufig  auf der neuesten Hardware basiert und das zum anderen auf Grund der Entfernung zum Lab-Datacenter entsprechende Latenzen auftreten können. Nichtsdestotrotz lassen sich mit dieser Umgebung die typischen Routineaufgaben bzgl. einer Nutanix-Cluster-Plattform mit einer ausgezeichneten User-Experience testen.

Infrastruktur IPs
+++++++++++++++++

.. list-table::
   :widths: 10 10 10 10
   :header-rows: 1

   * - Nodes
     - CVMs
     - Hypervisors
     - IPMI
   * - **Position A**
     - 10.42.58.29
     - 10.42.58.25
     - 10.42.58.33
   * - **Position B**
     - 10.42.58.30
     - 10.42.58.26
     - 10.42.58.34
   * - **Position C**
     - 10.42.58.31
     - 10.42.58.27
     - 10.42.58.35
   * - **Position D**
     - 10.42.58.32
     - 10.42.58.28
     - 10.42.58.36


.. list-table::
  :widths: 20 20
  :header-rows: 1

  * - Services
    - IP-Adressen
  * - **Cluster virtual IP**
    - 10.42.58.37
  * - **iSCSI Data Services IP**
    - 10.42.58.38
  * - **Prism Central**
    - 10.42.58.39
  * - **Active Directory**
    - 10.42.58.41


Zugangsdaten
++++++++++++

Die folgende Tabelle führt die standardmäßig hinterlegten Zugangsdaten für die Umgebung auf (falls andere zum Einsatz kommen sollten wird dies gesondert aufgeführt):

.. list-table::
  :widths: 20 20 10
  :header-rows: 1

  * - Name
    - Benutzername
    - Passwort
  * - **IPMI**
    - ADMIN
    - ADMIN
  * - **Prism Element Web**
    - admin
    - citrix4AHV!
  * - **Prism Element SSH**
    - nutanix
    - citrix4AHV!
  * - **Prism Central Web**
    - admin
    - citrix4AHV!
  * - **Prism Central SSH**
    - nutanix
    - nutanix/4u
  * - **NTNXLAB Domain**
    - NTNXLAB\\Administrator
    - nutanix/4u
  * - **CentOS VM Image**
    - root
    - nutanix/4u


Darüber hinaus besitzt der Cluster eine dedizierte Domain-Controller-VM, welche die Active-Directory-Services für die **NTNXLAB.local** Domain bereitstellt. Die Domain wurde mit den folgenden Nutzern und Gruppen vorkonfiguriert:

.. list-table::
  :widths: 20 20 10
  :header-rows: 1

  * - Gruppe
    - Benutzername(n)
    - Passwort
  * - **Administrators / Domain Admins**
    - Administrator
    - nutanix/4u
  * - **Bootcamp Users**
    - User01-User25
    - nutanix/4u
  * - **SSP Admins**
    - Adminuser01-Adminuser25
    - nutanix/4u
  * - **SSP Operators**
    - Operator01-Operator25
    - nutanix/4u
  * - **SSP Developers**
    - Devuser01-Devuser25
    - nutanix/4u
  * - **SSP Consumers**
    - Consumer01-Consumer25
    - nutanix/4u
  * - **SSP Custom**
    - Custom01-Custom25
    - nutanix/4u

Netzwerk
++++++++

Die folgenden virtuellen Netzwerke wurden wie folgt vorkonfiguriert:

.. list-table::
   :widths: 33 33 33
   :header-rows: 1

   * -
     - **Primäres** Netzwerk
     - **Sekundäres** Netzwerk
   * - **VLAN**
     - 0
     - 581
   * - **Netzwerk IP Adresse**
     - 10.42.58.0
     - 10.42.58.128
   * - **Netzmaske**
     - 255.255.255.128 (/25)
     - 255.255.255.128 (/25)
   * - **Default Gateway**
     - 10.42.58.1
     - 10.42.58.129
   * - **IP Address Management (IPAM)**
     - Aktiviert
     - Aktiviert
   * - **DHCP Pool**
     - 10.42.58.50  - 125
     - 10.42.58.132 - 253
   * - **Domain**
     - NTNXLAB.local
     - NTNXLAB.local
   * - **DNS**
     - 10.42.58.41 (DC VM)
     - 10.42.58.41 (DC VM)
