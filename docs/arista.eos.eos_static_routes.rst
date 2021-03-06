:source: 


.. _arista.eos.eos_static_routes_:


arista.eos.eos_static_routes -- Configures and manages attributes of static routes on Arista EOS platforms.
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++


.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module configures and manages the attributes of static routes on Arista EOS platforms.




Parameters
----------

.. raw:: html

    <table  border=0 cellpadding=0 class="documentation-table">
        <tr>
            <th colspan="5">Parameter</th>
            <th>Choices/<font color="blue">Defaults</font></th>
                            <th>Configuration</th>
                        <th width="100%">Comments</th>
        </tr>
                    <tr>
                                                                <td colspan="5">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>config</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">list</span>
                         / <span style="color: purple">elements=dictionary</span>                                            </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>A list of configurations for static routes.</div>
                                                        </td>
            </tr>
                                                            <tr>
                                                    <td class="elbow-placeholder"></td>
                                                <td colspan="4">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>address_families</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">list</span>
                         / <span style="color: purple">elements=dictionary</span>                                            </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>A dictionary specifying the address family to which the static route(s) belong.</div>
                                                        </td>
            </tr>
                                                            <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="3">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>afi</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                 / <span style="color: red">required</span>                    </div>
                                    </td>
                                <td>
                                                                                                                            <ul style="margin: 0; padding: 0"><b>Choices:</b>
                                                                                                                                                                <li>ipv4</li>
                                                                                                                                                                                                <li>ipv6</li>
                                                                                    </ul>
                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Specifies the top level address family indicator.</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="3">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>routes</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">list</span>
                         / <span style="color: purple">elements=dictionary</span>                                            </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>A dictionary that specifies the static route configurations.</div>
                                                        </td>
            </tr>
                                                            <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>dest</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                 / <span style="color: red">required</span>                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Destination IPv4 subnet (CIDR or address-mask notation).</div>
                                            <div>The address format is &lt;v4/v6 address&gt;/&lt;mask&gt; or &lt;v4/v6 address&gt; &lt;mask&gt;.</div>
                                            <div>The mask is number in range 0-32 for IPv4 and in range 0-128 for IPv6.</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>next_hops</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">list</span>
                         / <span style="color: purple">elements=dictionary</span>                                            </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Details of route to be taken.</div>
                                                        </td>
            </tr>
                                                            <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>admin_distance</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">integer</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Preference or administrative distance of route (range 1-255).</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>description</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Name of the static route.</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>forward_router_address</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Forwarding router&#x27;s address on destination interface.</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>interface</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Outgoing interface to take. For anything except &#x27;null0&#x27;, then next hop IP address should also be configured.</div>
                                            <div>IP address of the next hop router or</div>
                                            <div>null0 Null0 interface or</div>
                                            <div>ethernet e_num Ethernet interface or</div>
                                            <div>loopback l_num Loopback interface or</div>
                                            <div>management m_num Management interface or</div>
                                            <div>port-channel p_num</div>
                                            <div>vlan v_num</div>
                                            <div>vxlan vx_num</div>
                                            <div>Nexthop-Group  Specify nexthop group name</div>
                                            <div>Tunnel  Tunnel interface</div>
                                            <div>vtep  Configure VXLAN Tunnel End Points</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>mpls_label</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">integer</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>MPLS label</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>nexthop_grp</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Nexthop group</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>tag</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">integer</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Route tag value (ranges from 0 to 4294967295).</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>track</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Track value (range 1 - 512). Track must already be configured on the device before adding the route.</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>vrf</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>VRF of the destination.</div>
                                                        </td>
            </tr>
                    
                                    
                                    
                                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                                <td colspan="4">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>vrf</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>The VRF to which the static route(s) belong.</div>
                                                        </td>
            </tr>
                    
                                                <tr>
                                                                <td colspan="5">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>running_config</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>The module, by default, will connect to the remote device and retrieve the current running-config to use as a base for comparing against the contents of source. There are times when it is not desirable to have the task get the current running-config for every task in a playbook.  The <em>running_config</em> argument allows the implementer to pass in the configuration to use as the base config for comparison. This value of this option should be the output received from device by executing command</div>
                                                        </td>
            </tr>
                                <tr>
                                                                <td colspan="5">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>state</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                            <ul style="margin: 0; padding: 0"><b>Choices:</b>
                                                                                                                                                                <li>deleted</li>
                                                                                                                                                                                                <li><div style="color: blue"><b>merged</b>&nbsp;&larr;</div></li>
                                                                                                                                                                                                <li>overridden</li>
                                                                                                                                                                                                <li>replaced</li>
                                                                                                                                                                                                <li>gathered</li>
                                                                                                                                                                                                <li>rendered</li>
                                                                                                                                                                                                <li>parsed</li>
                                                                                    </ul>
                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>The state the configuration should be left in.</div>
                                                        </td>
            </tr>
                        </table>
    <br/>


Notes
-----

.. note::
   - Tested against Arista EOS 4.20.10M
   - This module works with connection ``network_cli``. See the `EOS Platform Options <../network/user_guide/platform_eos.html>`_.



Examples
--------

.. code-block:: yaml+jinja

    
    # Using deleted

    # Various scenarios for delete operations:

    # Before state:
    # ------------
    # veos(config)#show running-config | grep route
    # ip route 10.2.2.0/24 Ethernet1
    # ip route 10.2.2.0/24 64.1.1.1 label 17 33
    # ip route 33.33.33.0/24 Nexthop-Group testgrp
    # ip route vrf testvrf 22.65.1.0/24 Null0 90 name testroute
    # ipv6 route 5222:5::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Ethernet1 55
    # ipv6 route vrf testvrf 2222:6::/64 Null0 90 name testroute1
    # veos(config)#

    - name: Delete nexthop
      eos_static_routes:
        config:
          - address_families:
              - afi: ipv4
                routes:
                  - dest: 10.2.2.0/24
                    next_hops:
                      - interface: 64.1.1.1
                        mpls_label: 17
                        admin_distance: 33
                  - dest: "33.33.33.0 255.255.255.0"
                    next_hops:
                      - interface: 'Nexthop-Group testgrp'
        state: "deleted"

    # "after": [
    #         {
    #             "address_families": [
    #                 {
    #                     "afi": "ipv4",
    #                     "routes": [
    #                         {
    #                             "dest": "10.2.2.0/24",
    #                             "next_hops": [
    #                                 {
    #                                     "interface": "Ethernet1"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 },
    #                 {
    #                     "afi": "ipv6",
    #                     "routes": [
    #                         {
    #                             "dest": "5222:5::/64",
    #                             "next_hops": [
    #                                 {
    #                                     "forward_router_address": "4312:100::1",
    #                                     "interface": "Management1"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 }
    #             ]
    #         },
    #         {
    #             "address_families": [
    #                 {
    #                     "afi": "ipv4",
    #                     "routes": [
    #                         {
    #                             "dest": "22.65.1.0/24",
    #                             "next_hops": [
    #                                 {
    #                                     "admin_distance": 90,
    #                                     "description": "testroute",
    #                                     "interface": "Null0"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 },
    #                 {
    #                     "afi": "ipv6",
    #                     "routes": [
    #                         {
    #                             "dest": "2222:6::/64",
    #                             "next_hops": [
    #                                 {
    #                                     "forward_router_address": "4312:100::1",
    #                                     "interface": "Management1"
    #                                 },
    #                                 {
    #                                     "admin_distance": 55,
    #                                     "interface": "Ethernet1"
    #                                 },
    #                                 {
    #                                     "admin_distance": 90,
    #                                     "description": "testroute1",
    #                                     "interface": "Null0"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 }
    #             ],
    #             "vrf": "testvrf"
    #         }
    #     ],
    #     "before": [
    #         {
    #             "address_families": [
    #                 {
    #                     "afi": "ipv4",
    #                     "routes": [
    #                         {
    #                             "dest": "10.2.2.0/24",
    #                             "next_hops": [
    #                                 {
    #                                     "interface": "Ethernet1"
    #                                 },
    #                                 {
    #                                     "admin_distance": 33,
    #                                     "interface": "64.1.1.1",
    #                                     "mpls_label": 17
    #                                 }
    #                             ]
    #                         },
    #                         {
    #                             "dest": "33.33.33.0/24",
    #                             "next_hops": [
    #                                 {
    #                                     "nexthop_grp": "testgrp"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 },
    #                 {
    #                     "afi": "ipv6",
    #                     "routes": [
    #                         {
    #                             "dest": "5222:5::/64",
    #                             "next_hops": [
    #                                 {
    #                                     "forward_router_address": "4312:100::1",
    #                                     "interface": "Management1"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 }
    #             ]
    #         },
    #         {
    #             "address_families": [
    #                 {
    #                     "afi": "ipv4",
    #                     "routes": [
    #                         {
    #                             "dest": "22.65.1.0/24",
    #                             "next_hops": [
    #                                 {
    #                                     "admin_distance": 90,
    #                                     "description": "testroute",
    #                                     "interface": "Null0"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 },
    #                 {
    #                     "afi": "ipv6",
    #                     "routes": [
    #                         {
    #                             "dest": "2222:6::/64",
    #                             "next_hops": [
    #                                 {
    #                                     "forward_router_address": "4312:100::1",
    #                                     "interface": "Management1"
    #                                 },
    #                                 {
    #                                     "admin_distance": 55,
    #                                     "interface": "Ethernet1"
    #                                 },
    #                                 {
    #                                     "admin_distance": 90,
    #                                     "description": "testroute1",
    #                                     "interface": "Null0"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 }
    #             ],
    #             "vrf": "testvrf"
    #         }
    #     ],
    #     "changed": true,
    #     "commands": [
    #         "no ip route 10.2.2.0/24 64.1.1.1 label 17 33",
    #         "no ip route 33.33.33.0/24 Nexthop-Group testgrp"
    #     ]


    # After State
    # -----------

    # veos(config)#show running-config | grep route
    # ip route 10.2.2.0/24 Ethernet1
    # ip route vrf testvrf 22.65.1.0/24 Null0 90 name testroute
    # ipv6 route 5222:5::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Ethernet1 55
    # ipv6 route vrf testvrf 2222:6::/64 Null0 90 name testroute1
    # veos(config)#


    # Before State
    # ____________

    # veos(config)#show running-config | grep route
    # ip route 10.2.2.0/24 Ethernet1
    # ip route vrf testvrf 22.65.1.0/24 Null0 90 name testroute
    # ipv6 route 5222:5::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Ethernet1 55
    # ipv6 route vrf testvrf 2222:6::/64 Null0 90 name testroute1
    # veos(config)#

    - name: Delete route
      eos_static_routes:
        config:
          - address_families:
            - afi: ipv4
              routes:
                - dest: 10.2.2.0/24
        state: "deleted"

    # "after": [
    #         {
    #             "address_families": [
    #                 {
    #                     "afi": "ipv6",
    #                     "routes": [
    #                         {
    #                             "dest": "5222:5::/64",
    #                             "next_hops": [
    #                                 {
    #                                     "forward_router_address": "4312:100::1",
    #                                     "interface": "Management1"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 }
    #             ]
    #         },
    #         {
    #             "address_families": [
    #                 {
    #                     "afi": "ipv4",
    #                     "routes": [
    #                         {
    #                             "dest": "22.65.1.0/24",
    #                             "next_hops": [
    #                                 {
    #                                     "admin_distance": 90,
    #                                     "description": "testroute",
    #                                     "interface": "Null0"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 },
    #                 {
    #                     "afi": "ipv6",
    #                     "routes": [
    #                         {
    #                             "dest": "2222:6::/64",
    #                             "next_hops": [
    #                                 {
    #                                     "forward_router_address": "4312:100::1",
    #                                     "interface": "Management1"
    #                                 },
    #                                 {
    #                                     "admin_distance": 55,
    #                                     "interface": "Ethernet1"
    #                                 },
    #                                 {
    #                                     "admin_distance": 90,
    #                                     "description": "testroute1",
    #                                     "interface": "Null0"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 }
    #             ],
    #             "vrf": "testvrf"
    #         }
    #     ],
    #     "before": [
    #         {
    #             "address_families": [
    #                 {
    #                     "afi": "ipv4",
    #                     "routes": [
    #                         {
    #                             "dest": "10.2.2.0/24",
    #                             "next_hops": [
    #                                 {
    #                                     "interface": "Ethernet1"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 },
    #                 {
    #                     "afi": "ipv6",
    #                     "routes": [
    #                         {
    #                             "dest": "5222:5::/64",
    #                             "next_hops": [
    #                                 {
    #                                     "forward_router_address": "4312:100::1",
    #                                     "interface": "Management1"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 }
    #             ]
    #         },
    #         {
    #             "address_families": [
    #                 {
    #                     "afi": "ipv4",
    #                     "routes": [
    #                         {
    #                             "dest": "22.65.1.0/24",
    #                             "next_hops": [
    #                                 {
    #                                     "admin_distance": 90,
    #                                     "description": "testroute",
    #                                     "interface": "Null0"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 },
    #                 {
    #                     "afi": "ipv6",
    #                     "routes": [
    #                         {
    #                             "dest": "2222:6::/64",
    #                             "next_hops": [
    #                                 {
    #                                     "forward_router_address": "4312:100::1",
    #                                     "interface": "Management1"
    #                                 },
    #                                 {
    #                                     "admin_distance": 55,
    #                                     "interface": "Ethernet1"
    #                                 },
    #                                 {
    #                                     "admin_distance": 90,
    #                                     "description": "testroute1",
    #                                     "interface": "Null0"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 }
    #             ],
    #             "vrf": "testvrf"
    #         }
    #     ],
    #     "changed": true,
    #     "commands": [
    #         "no ip route 10.2.2.0/24 Ethernet1"
    #     ]

    # After State
    # -----------
    # veos(config)#show running-config | grep route
    # ip route vrf testvrf 22.65.1.0/24 Null0 90 name testroute
    # ipv6 route 5222:5::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Ethernet1 55
    # ipv6 route vrf testvrf 2222:6::/64 Null0 90 name testroute1
    # veos(config)#


    # Before State:
    # ------------

    # veos(config)#show running-config | grep route
    # ip route vrf testvrf 22.65.1.0/24 Null0 90 name testroute
    # ipv6 route 5222:5::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Ethernet1 55
    # ipv6 route vrf testvrf 2222:6::/64 Null0 90 name testroute1
    # veos(config)#

    - name: Delete afi
      eos_static_routes:
        config:
          - vrf: "testvrf"
            address_families:
            - afi: "ipv4"
        state: "deleted"

    #    "after": [
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv6",
    #                    "routes": [
    #                        {
    #                            "dest": "5222:5::/64",
    #                            "next_hops": [
    #                                {
    #                                    "forward_router_address": "4312:100::1",
    #                                    "interface": "Management1"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }
    #            ]
    #        },
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv6",
    #                    "routes": [
    #                        {
    #                            "dest": "2222:6::/64",
    #                            "next_hops": [
    #                                {
    #                                    "forward_router_address": "4312:100::1",
    #                                    "interface": "Management1"
    #                                },
    #                                {
    #                                    "admin_distance": 55,
    #                                    "interface": "Ethernet1"
    #                                },
    #                                {
    #                                    "admin_distance": 90,
    #                                    "description": "testroute1",
    #                                    "interface": "Null0"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }
    #            ],
    #            "vrf": "testvrf"
    #        }
    #    ],
    #    "before": [
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv6",
    #                    "routes": [
    #                        {
    #                            "dest": "5222:5::/64",
    #                            "next_hops": [
    #                                {
    #                                    "forward_router_address": "4312:100::1",
    #                                    "interface": "Management1"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }
    #            ]
    #        },
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv4",
    #                    "routes": [
    #                        {
    #                            "dest": "22.65.1.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "admin_distance": 90,
    #                                    "description": "testroute",
    #                                    "interface": "Null0"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                },
    #                {
    #                    "afi": "ipv6",
    #                    "routes": [
    #                        {
    #                            "dest": "2222:6::/64",
    #                            "next_hops": [
    #                                {
    #                                    "forward_router_address": "4312:100::1",
    #                                    "interface": "Management1"
    #                                },
    #                                {
    #                                    "admin_distance": 55,
    #                                    "interface": "Ethernet1"
    #                                },
    #                                {
    #                                    "admin_distance": 90,
    #                                    "description": "testroute1",
    #                                    "interface": "Null0"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }
    #            ],
    #            "vrf": "testvrf"
    #        }
    #    ],
    #    "changed": true,
    #    "commands": [
    #        "no ip route vrf testvrf 22.65.1.0/24 Null0 90 name testroute"
    #    ],

    # After State
    # ___________

    # veos(config)#show running-config | grep route
    # ipv6 route 5222:5::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Ethernet1 55
    # ipv6 route vrf testvrf 2222:6::/64 Null0 90 name testroute1

    # Before State
    #-------------

    # veos(config)#show running-config | grep route
    # ipv6 route 5222:5::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Ethernet1 55
    # ipv6 route vrf testvrf 2222:6::/64 Null0 90 name testroute1

    - name: Delete vrf
      eos_static_routes:
        config:
          - vrf: testvrf
        state: "deleted"

    # "after": [
    #         {
    #             "address_families": [
    #                 {
    #                     "afi": "ipv6",
    #                     "routes": [
    #                         {
    #                             "dest": "5222:5::/64",
    #                             "next_hops": [
    #                                 {
    #                                     "forward_router_address": "4312:100::1",
    #                                     "interface": "Management1"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 }
    #             ]
    #         }
    #     ],
    #     "before": [
    #         {
    #             "address_families": [
    #                 {
    #                     "afi": "ipv6",
    #                     "routes": [
    #                         {
    #                             "dest": "5222:5::/64",
    #                             "next_hops": [
    #                                 {
    #                                     "forward_router_address": "4312:100::1",
    #                                     "interface": "Management1"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 }
    #             ]
    #         },
    #         {
    #             "address_families": [
    #                 {
    #                     "afi": "ipv6",
    #                     "routes": [
    #                         {
    #                             "dest": "2222:6::/64",
    #                             "next_hops": [
    #                                 {
    #                                     "forward_router_address": "4312:100::1",
    #                                     "interface": "Management1"
    #                                 },
    #                                 {
    #                                     "admin_distance": 55,
    #                                     "interface": "Ethernet1"
    #                                 },
    #                                 {
    #                                     "admin_distance": 90,
    #                                     "description": "testroute1",
    #                                     "interface": "Null0"
    #                                 }
    #                             ]
    #                         }
    #                     ]
    #                 }
    #             ],
    #             "vrf": "testvrf"
    #         }
    #     ],
    #     "changed": true,
    #     "commands": [
    #         "no ipv6 route vrf testvrf 2222:6::/64 Management1 4312:100::1",
    #         "no ipv6 route vrf testvrf 2222:6::/64 Ethernet1 55",
    #         "no ipv6 route vrf testvrf 2222:6::/64 Null0 90 name testroute1"
    #     ]
    #
    # After State:
    # -----------

    # veos(config)#show running-config | grep route
    # ipv6 route 5222:5::/64 Management1 4312:100::1
    # veos(config)#


    #
    # Using merged

    # Before : [
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv4",
    #                    "routes": [
    #                        {
    #                            "dest": "165.10.1.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "admin_distance": 100,
    #                                    "interface": "Ethernet1"
    #                                }
    #                            ]
    #                        },
    #                        {
    #                            "dest": "172.17.252.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "nexthop_grp": "testgroup"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                },
    #                {
    #                    "afi": "ipv6",
    #                    "routes": [
    #                        {
    #                            "dest": "5001::/64",
    #                            "next_hops": [
    #                                {
    #                                    "admin_distance": 50,
    #                                    "interface": "Ethernet1"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }
    #            ]
    #        },
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv4",
    #                    "routes": [
    #                        {
    #                            "dest": "130.1.122.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "interface": "Ethernet1",
    #                                    "tag": 50
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }
    #            ],
    #            "vrf": "testvrf"
    #        }
    #    ]
    #
    # Before State
    # -------------
    # veos(config)#show running-config | grep "route"
    # ip route 165.10.1.0/24 Ethernet1 100
    # ip route 172.17.252.0/24 Nexthop-Group testgroup
    # ip route vrf testvrf 130.1.122.0/24 Ethernet1 tag 50
    # ipv6 route 5001::/64 Ethernet1 50
    # veos(config)#

    - name: Merge new static route configuration
      eos_static_routes:
        config:
          - vrf: testvrf
            address_families:
              - afi: ipv6
                routes:
                  - dest: 2211::0/64
                    next_hop:
                      - forward_router_address: 100:1::2
                        interface: "Ethernet1"
        state: merged

    # After State
    # -----------

    #After [
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv4",
    #                    "routes": [
    #                        {
    #                            "dest": "165.10.1.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "admin_distance": 100,
    #                                    "interface": "Ethernet1"
    #                                }
    #                            ]
    #                        },
    #                        {
    #                            "dest": "172.17.252.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "nexthop_grp": "testgroup"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                },
    #                {
    #                    "afi": "ipv6",
    #                    "routes": [
    #                        {
    #                            "dest": "5001::/64",
    #                            "next_hops": [
    #                                {
    #                                    "admin_distance": 50,
    #                                    "interface": "Ethernet1"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }
    #            ]
    #        },
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv4",
    #                    "routes": [
    #                        {
    #                            "dest": "130.1.122.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "interface": "Ethernet1",
    #                                    "tag": 50
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                },
    #                {
    #                    "afi": "ipv6",
    #                    "routes": [
    #                        {
    #                            "dest": "2211::0/64",
    #                            "next_hops": [
    #                                {
    #                                    "aforward_router_address": 100:1::2
    #                                    "interface": "Ethernet1"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }

    #            ],
    #            "vrf": "testvrf"
    #        }
    #    ]
    #
    # veos(config)#show running-config | grep "route"
    # ip route 165.10.1.0/24 Ethernet1 100
    # ip route 172.17.252.0/24 Nexthop-Group testgroup
    # ip route vrf testvrf 130.1.122.0/24 Ethernet1 tag 50
    # ipv6 route 2211::/64 Ethernet1 100:1::2
    # ipv6 route 5001::/64 Ethernet1 50
    # veos(config)#


    # Using overridden


    # Before State
    # -------------

    #    "before": [
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv4",
    #                    "routes": [
    #                        {
    #                            "dest": "165.10.1.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "admin_distance": 100,
    #                                    "interface": "Ethernet1"
    #                                }
    #                            ]
    #                        },
    #                        {
    #                            "dest": "172.17.252.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "nexthop_grp": "testgroup"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                },
    #                {
    #                    "afi": "ipv6",
    #                    "routes": [
    #                        {
    #                            "dest": "5001::/64",
    #                            "next_hops": [
    #                                {
    #                                    "admin_distance": 50,
    #                                    "interface": "Ethernet1"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }
    #            ]
    #        },
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv4",
    #                    "routes": [
    #                        {
    #                            "dest": "130.1.122.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "interface": "Ethernet1",
    #                                    "tag": 50
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }
    #            ],
    #            "vrf": "testvrf"
    #        }
    #    ]
    # veos(config)#show running-config | grep "route"
    # ip route 165.10.1.0/24 Ethernet1 100
    # ip route 172.17.252.0/24 Nexthop-Group testgroup
    # ip route vrf testvrf 130.1.122.0/24 Ethernet1 tag 50
    # ipv6 route 5001::/64 Ethernet1 50
    # veos(config)#

    - name: Overridden static route configuration
      eos_static_routes:
        config:
          - address_families:
              - afi: ipv4
                routes:
                  - dest: 10.2.2.0/24
                    next_hop:
                      - interface: "Ethernet1"
        state: replaced

    # After State
    # -----------

    # "after": [
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv4",
    #                    "routes": [
    #                        {
    #                            "dest": "10.2.2.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "interface": "Ethernet1"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }
    #            ]
    #        }
    #    ]
    # veos(config)#show running-config | grep "route"
    # ip route 10.2.2.0/24 Ethernet1
    # veos(config)#


    # Using replaced

    # Before State
    # -------------

    # ip route 10.2.2.0/24 Ethernet1
    # ip route 10.2.2.0/24 64.1.1.1 label 17 33
    # ip route 33.33.33.0/24 Nexthop-Group testgrp
    # ip route vrf testvrf 22.65.1.0/24 Null0 90 name testroute
    # ipv6 route 5222:5::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Ethernet1 55
    # ipv6 route vrf testvrf 2222:6::/64 Null0 90 name testroute1

    # [
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv4",
    #                    "routes": [
    #                        {
    #                            "dest": "10.2.2.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "interface": "Ethernet1"
    #                                },
    #                                {
    #                                    "admin_distance": 33,
    #                                    "interface": "64.1.1.1",
    #                                    "mpls_label": 17
    #                                }
    #                            ]
    #                        },
    #                        {
    #                            "dest": "33.33.33.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "nexthop_grp": "testgrp"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                },
    #                {
    #                    "afi": "ipv6",
    #                    "routes": [
    #                        {
    #                            "dest": "5222:5::/64",
    #                            "next_hops": [
    #                                {
    #                                    "forward_router_address": "4312:100::1",
    #                                    "interface": "Management1"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }
    #            ]
    #        },
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv4",
    #                    "routes": [
    #                        {
    #                            "dest": "22.65.1.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "admin_distance": 90,
    #                                    "description": "testroute",
    #                                    "interface": "Null0"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                },
    #                {
    #                    "afi": "ipv6",
    #                    "routes": [
    #                        {
    #                            "dest": "2222:6::/64",
    #                            "next_hops": [
    #                                {
    #                                    "forward_router_address": "4312:100::1",
    #                                    "interface": "Management1"
    #                                },
    #                                {
    #                                    "admin_distance": 90,
    #                                    "description": "testroute1",
    #                                    "interface": "Null0"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }
    #            ],
    #            "vrf": "testvrf"
    #        }
    #    ]

    - name: Replace nexthop
      eos_static_routes:
        config:
          - vrf: testvrf
            address_families:
              - afi: ipv6
                routes:
                  - dest: 2222:6::/64
                    next_hops:
                      - admin_distance: 55
                        interface: "Ethernet1"
        state: "replaced"

    # After State
    # -----------

    # veos(config)#show running-config | grep route
    # ip route 10.2.2.0/24 Ethernet1
    # ip route 10.2.2.0/24 64.1.1.1 label 17 33
    # ip route 33.33.33.0/24 Nexthop-Group testgrp
    # ip route vrf testvrf 22.65.1.0/24 Null0 90 name testroute
    # ipv6 route 5222:5::/64 Management1 4312:100::1
    # ipv6 route vrf testvrf 2222:6::/64 Ethernet1 55

    # "after": [
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv4",
    #                    "routes": [
    #                        {
    #                            "dest": "10.2.2.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "interface": "Ethernet1"
    #                                },
    #                                {
    #                                    "admin_distance": 33,
    #                                    "interface": "64.1.1.1",
    #                                    "mpls_label": 17
    #                                }
    #                            ]
    #                        },
    #                        {
    #                            "dest": "33.33.33.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "nexthop_grp": "testgrp"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                },
    #                {
    #                    "afi": "ipv6",
    #                    "routes": [
    #                        {
    #                            "dest": "5222:5::/64",
    #                            "next_hops": [
    #                                {
    #                                    "forward_router_address": "4312:100::1",
    #                                    "interface": "Management1"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }
    #            ]
    #        },
    #        {
    #            "address_families": [
    #                {
    #                    "afi": "ipv4",
    #                    "routes": [
    #                        {
    #                            "dest": "22.65.1.0/24",
    #                            "next_hops": [
    #                                {
    #                                    "admin_distance": 90,
    #                                    "description": "testroute",
    #                                    "interface": "Null0"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                },
    #                {
    #                    "afi": "ipv6",
    #                    "routes": [
    #                        {
    #                            "dest": "2222:6::/64",
    #                            "next_hops": [
    #                                {
    #                                    "admin_distance": 55,
    #                                    "interface": "Ethernet1"
    #                                }
    #                            ]
    #                        }
    #                    ]
    #                }
    #            ],
    #            "vrf": "testvrf"
    #        }
    #    ]

    # Before State
    # -------------
    # veos(config)#show running-config | grep "route"
    # ip route 165.10.1.0/24 Ethernet1 10.1.1.2 100
    # ipv6 route 5001::/64 Ethernet1
    # veos(config)#


    - name: Gather the exisitng condiguration
      eos_static_routes:
        state: gathered

    # returns :
    #  eos_static_routes:
    #    config:
    #      - address_families:
    #          - afi: ipv4
    #            routes:
    #              - dest: 165.10.1.0/24
    #                next_hop:
    #                  - forward_router_address: 10.1.1.2
    #                    interface: "Ethernet1"
    #                    admin_distance: 100
    #          - afi: ipv6
    #            routes:
    #              - dest: 5001::/64
    #                next_hop:
    #                  - interface: "Ethernet1"


    # Using rendered

    #   eos_static_routes:
    #    config:
    #      - address_families:
    #          - afi: ipv4
    #            routes:
    #              - dest: 165.10.1.0/24
    #                next_hop:
    #                  - forward_router_address: 10.1.1.2
    #                    interface: "Ethernet1"
    #                    admin_distance: 100
    #         - afi: ipv6
    #            routes:
    #              - dest: 5001::/64
    #                next_hop:
    #                  - interface: "Ethernet1"

    # returns:

    # ip route 165.10.1.0/24 Ethernet1 10.1.1.2 100
    # ipv6 route 5001::/64 Ethernet1






Return Values
-------------
Common return values are documented :ref:`here <common_return_values>`, the following are the fields unique to this :

.. raw:: html

    <table border=0 cellpadding=0 class="documentation-table">
        <tr>
            <th colspan="1">Key</th>
            <th>Returned</th>
            <th width="100%">Description</th>
        </tr>
                    <tr>
                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="return-"></div>
                    <b>after</b>
                    <a class="ansibleOptionLink" href="#return-" title="Permalink to this return value"></a>
                    <div style="font-size: small">
                      <span style="color: purple">list</span>
                                          </div>
                                    </td>
                <td>when changed</td>
                <td>
                                                                        <div>The resulting configuration model invocation.</div>
                                                                <br/>
                                            <div style="font-size: smaller"><b>Sample:</b></div>
                                                <div style="font-size: smaller; color: blue; word-wrap: break-word; word-break: break-all;">The configuration returned will always be in the same format
     of the parameters above.</div>
                                    </td>
            </tr>
                                <tr>
                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="return-"></div>
                    <b>before</b>
                    <a class="ansibleOptionLink" href="#return-" title="Permalink to this return value"></a>
                    <div style="font-size: small">
                      <span style="color: purple">list</span>
                                          </div>
                                    </td>
                <td>always</td>
                <td>
                                                                        <div>The configuration prior to the model invocation.</div>
                                                                <br/>
                                            <div style="font-size: smaller"><b>Sample:</b></div>
                                                <div style="font-size: smaller; color: blue; word-wrap: break-word; word-break: break-all;">The configuration returned will always be in the same format
     of the parameters above.</div>
                                    </td>
            </tr>
                                <tr>
                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="return-"></div>
                    <b>commands</b>
                    <a class="ansibleOptionLink" href="#return-" title="Permalink to this return value"></a>
                    <div style="font-size: small">
                      <span style="color: purple">list</span>
                                          </div>
                                    </td>
                <td>always</td>
                <td>
                                                                        <div>The set of commands pushed to the remote device.</div>
                                                                <br/>
                                            <div style="font-size: smaller"><b>Sample:</b></div>
                                                <div style="font-size: smaller; color: blue; word-wrap: break-word; word-break: break-all;">[&#x27;ip route vrf vrf1 192.2.2.0/24 125.2.3.1 93&#x27;]</div>
                                    </td>
            </tr>
                                <tr>
                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="return-"></div>
                    <b>gathered</b>
                    <a class="ansibleOptionLink" href="#return-" title="Permalink to this return value"></a>
                    <div style="font-size: small">
                      <span style="color: purple">list</span>
                                          </div>
                                    </td>
                <td>When <code>state</code> is <em>gathered</em></td>
                <td>
                                                                        <div>The configuration as structured data transformed for the running configuration fetched from remote host</div>
                                                                <br/>
                                            <div style="font-size: smaller"><b>Sample:</b></div>
                                                <div style="font-size: smaller; color: blue; word-wrap: break-word; word-break: break-all;">The configuration returned will always be in the same format of the parameters above.</div>
                                    </td>
            </tr>
                                <tr>
                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="return-"></div>
                    <b>parsed</b>
                    <a class="ansibleOptionLink" href="#return-" title="Permalink to this return value"></a>
                    <div style="font-size: small">
                      <span style="color: purple">list</span>
                                          </div>
                                    </td>
                <td>When <code>state</code> is <em>parsed</em></td>
                <td>
                                                                        <div>The configuration as structured data transformed for the value of <code>running_config</code> option</div>
                                                                <br/>
                                            <div style="font-size: smaller"><b>Sample:</b></div>
                                                <div style="font-size: smaller; color: blue; word-wrap: break-word; word-break: break-all;">The configuration returned will always be in the same format of the parameters above.</div>
                                    </td>
            </tr>
                                <tr>
                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="return-"></div>
                    <b>rendered</b>
                    <a class="ansibleOptionLink" href="#return-" title="Permalink to this return value"></a>
                    <div style="font-size: small">
                      <span style="color: purple">list</span>
                                          </div>
                                    </td>
                <td>When <code>state</code> is <em>rendered</em></td>
                <td>
                                                                        <div>The set of CLI commands generated from the value in <code>config</code> option</div>
                                                                <br/>
                                            <div style="font-size: smaller"><b>Sample:</b></div>
                                                <div style="font-size: smaller; color: blue; word-wrap: break-word; word-break: break-all;">&quot;address_families&quot;: [
                        {
                            &quot;afi&quot;: &quot;ipv4&quot;,
                            &quot;routes&quot;: [
                                {
                                    &quot;dest&quot;: &quot;192.2.2.0/24&quot;,
                                    &quot;next_hops&quot;: [
                                        {
                                            &quot;admin_distance&quot;: 93,
                                            &quot;description&quot;: null,
                                            &quot;forward_router_address&quot;: null,
                                            &quot;interface&quot;: &quot;125.2.3.1&quot;,
                                            &quot;mpls_label&quot;: null,
                                            &quot;nexthop_grp&quot;: null,
                                            &quot;tag&quot;: null,
                                            &quot;track&quot;: null,
                                            &quot;vrf&quot;: null
                                        }
                                    ]
                                }
                            ]
                        }
                    ],
                    &quot;vrf&quot;: &quot;vrf1&quot;
                }
            ],
            &quot;running_config&quot;: null,
            &quot;state&quot;: &quot;rendered&quot;
        }</div>
                                    </td>
            </tr>
                        </table>
    <br/><br/>


Status
------




- This  is not guaranteed to have a backwards compatible interface. *[preview]*


- This  is :ref:`maintained by the Ansible Network Team <modules_support>`. *[network]*

Red Hat Support
~~~~~~~~~~~~~~~

More information about Red Hat's support of this  is available from this `Red Hat Knowledge Base article <https://access.redhat.com/articles/3166901>`_.




Authors
~~~~~~~

- Gomathi Selvi Srinivasan (@GomathiselviS)


.. hint::
    If you notice any issues in this documentation, you can `edit this document <https://github.com/ansible/ansible/edit/devel/lib/ansible/plugins//?description=%23%23%23%23%23%20SUMMARY%0A%3C!---%20Your%20description%20here%20--%3E%0A%0A%0A%23%23%23%23%23%20ISSUE%20TYPE%0A-%20Docs%20Pull%20Request%0A%0A%2Blabel:%20docsite_pr>`_ to improve it.


.. hint::
    Configuration entries for each entry type have a low to high priority order. For example, a variable that is lower in the list will override a variable that is higher up.
