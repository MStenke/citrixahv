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

**Bootcamp Cluster A**

.. list-table::
   :widths: 10 10 10 10
   :header-rows: 1

   * - Nodes
     - CVMs
     - Hypervisors
     - IPMI
   * - **Position A**
     - 10.136.227.29
     - 10.136.227.25
     - 10.136.227.33
   * - **Position B**
     - 10.136.227.30
     - 10.136.227.26
     - 10.136.227.34
   * - **Position C**
     - 10.136.227.31
     - 10.136.227.27
     - 10.136.227.35
   * - **Position D**
     - 10.136.227.32
     - 10.136.227.28
     - 10.136.227.36

**Bootcamp Cluster B**

.. list-table::
   :widths: 10 10 10 10
   :header-rows: 1

   * - Nodes
     - CVMs
     - Hypervisors
     - IPMI
   * - **Position A**
     - 10.136.228.29
     - 10.136.228.25
     - 10.136.228.33
   * - **Position B**
     - 10.136.228.30
     - 10.136.228.26
     - 10.136.228.34
   * - **Position C**
     - 10.136.228.31
     - 10.136.228.27
     - 10.136.228.35
   * - **Position D**
     - 10.136.228.32
     - 10.136.228.28
     - 10.136.228.36


.. list-table::
  :widths: 25 25 25
  :header-rows: 1

  * - Services
    - Bootcamp Cluster A
    - Bootcamp Cluster B
  * - **Cluster virtual IP**
    - 10.136.227.37
    - 10.136.228.37
  * - **iSCSI Data Services IP**
    - 10.136.227.38
    - 10.136.228.38
  * - **Prism Central**
    - 10.136.227.39
	- 10.136.228.39
  * - **Active Directory**
    - 10.136.227.41
	- 10.136.228.39


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


Darüber hinaus besitzt jeder Cluster eine dedizierte Domain-Controller-VM, welche die Active-Directory-Services für die jeweilige **NTNXLAB.local** Domain bereitstellt. Die beiden Domain's wurde mit den folgenden Nutzern und Gruppen vorkonfiguriert:

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

**Bootcamp Cluster A**

.. list-table::
   :widths: 33 33 33
   :header-rows: 1

   * -
     - **Primäres** Netzwerk
     - **Sekundäres** Netzwerk
   * - **VLAN**
     - 0
     - 2271
   * - **Netzwerk IP Adresse**
     - 10.136.227.0
     - 10.136.227.128
   * - **Netzmaske**
     - 255.255.255.128 (/25)
     - 255.255.255.128 (/25)
   * - **Default Gateway**
     - 10.136.227.1
     - 10.136.227.129
   * - **IP Address Management (IPAM)**
     - Aktiviert
     - Aktiviert
   * - **DHCP Pool**
     - 10.136.227.50  - 125
     - 10.136.227.132 - 253
   * - **Domain**
     - NTNXLAB.local
     - NTNXLAB.local
   * - **DNS**
     - 10.136.227.41 (DC VM)
     - 10.136.227.41 (DC VM)

**Bootcamp Cluster B**

.. list-table::
   :widths: 33 33 33
   :header-rows: 1

   * -
     - **Primäres** Netzwerk
     - **Sekundäres** Netzwerk
   * - **VLAN**
     - 0
     - 2271
   * - **Netzwerk IP Adresse**
     - 10.136.228.0
     - 10.136.228.128
   * - **Netzmaske**
     - 255.255.255.128 (/25)
     - 255.255.255.128 (/25)
   * - **Default Gateway**
     - 10.136.228.1
     - 10.136.228.129
   * - **IP Address Management (IPAM)**
     - Aktiviert
     - Aktiviert
   * - **DHCP Pool**
     - 10.136.228.50  - 125
     - 10.136.228.132 - 253
   * - **Domain**
     - NTNXLAB.local
     - NTNXLAB.local
   * - **DNS**
     - 10.136.228.41 (DC VM)
     - 10.136.228.41 (DC VM)