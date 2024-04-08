<h1>Setting up VLANs in Proxmox</h1>

<p>To change the network interface configuration file to allow VLAN tagging in Proxmox, there are some steps that need to be completed in a shell, and can't be done in the GUI
Open the network interface configuration file located at <code>/etc/network/interfaces</code> using a text editor such as nano or vim.</p>



<div style="display: flex; align-items: center;">
  <div style="flex: 1;">
    <p align="center"> <br/> <h2> default /etc/network/interfaces</h2></p>
    <img src="https://i.imgur.com/f962fcx.png" style="height: 70%; width: auto;/>
  </div>
  <div style="flex: 1; padding-left: 20px;">
  </div>
</div>


<code>auto vmbr0.100
iface vmbr0.100 inet static <ul>address 10.0.0.254/24
        gateway 10.0.0.138</ul></code>


auto vmbr0.100
iface vmbr0.100 inet static
    address 10.0.0.254/24
    gateway 10.0.0.138

    auto vmbr0.100
iface vmbr0.100 inet static
    address 10.0.0.254/24
    gateway 10.0.0.138


    
<div style="display: flex; align-items: center;">
  <div style="flex: 1;">
    <p align="center"> <br/> <h2> Network Logical Topology</h2></p>
    <img src="https://i.imgur.com/6m0E3Fc.jpeg" style="height: 70%; width: auto;/>
  </div>
  <div style="flex: 1; padding-left: 20px;">
  </div>
</div>
