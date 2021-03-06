:source: 


.. _arista.eos.eos_l2_interfaces_:


arista.eos.eos_l2_interfaces -- Manages Layer-2 interface attributes of Arista EOS devices
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++


.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module provides declarative management of Layer-2 interface on Arista EOS devices.




Parameters
----------

.. raw:: html

    <table  border=0 cellpadding=0 class="documentation-table">
        <tr>
            <th colspan="3">Parameter</th>
            <th>Choices/<font color="blue">Defaults</font></th>
                            <th>Configuration</th>
                        <th width="100%">Comments</th>
        </tr>
                    <tr>
                                                                <td colspan="3">
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
                                            <div>A dictionary of Layer-2 interface options</div>
                                                        </td>
            </tr>
                                                            <tr>
                                                    <td class="elbow-placeholder"></td>
                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>access</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">dictionary</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Switchport mode access command to configure the interface as a layer 2 access.</div>
                                                        </td>
            </tr>
                                                            <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>vlan</b>
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
                                            <div>Configure given VLAN in access port. It&#x27;s used as the access VLAN ID.</div>
                                                        </td>
            </tr>
                    
                                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>mode</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                    <div style="font-style: italic; font-size: small; color: darkgreen">added in 2.10</div>                </td>
                                <td>
                                                                                                                            <ul style="margin: 0; padding: 0"><b>Choices:</b>
                                                                                                                                                                <li>access</li>
                                                                                                                                                                                                <li>trunk</li>
                                                                                    </ul>
                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Mode in which interface needs to be configured.</div>
                                            <div>Access mode is not shown in interface facts, so idempotency will not be maintained for switchport mode access and every time the output will come as changed=True.</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>name</b>
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
                                            <div>Full name of interface, e.g. Ethernet1.</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                                <td colspan="2">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>trunk</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">dictionary</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Switchport mode trunk command to configure the interface as a Layer 2 trunk.</div>
                                                        </td>
            </tr>
                                                            <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>native_vlan</b>
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
                                            <div>Native VLAN to be configured in trunk port. It is used as the trunk native VLAN ID.</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>trunk_allowed_vlans</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">list</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>List of allowed VLANs in a given trunk port. These are the only VLANs that will be configured on the trunk.</div>
                                                        </td>
            </tr>
                    
                                    
                                                <tr>
                                                                <td colspan="3">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>state</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                            <ul style="margin: 0; padding: 0"><b>Choices:</b>
                                                                                                                                                                <li><div style="color: blue"><b>merged</b>&nbsp;&larr;</div></li>
                                                                                                                                                                                                <li>replaced</li>
                                                                                                                                                                                                <li>overridden</li>
                                                                                                                                                                                                <li>deleted</li>
                                                                                    </ul>
                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>The state of the configuration after module completion</div>
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

    
    ---

    # Using merged

    # Before state:
    # -------------
    #
    # veos#show running-config | section interface
    # interface Ethernet1
    #    switchport access vlan 20
    # !
    # interface Ethernet2
    #    switchport trunk native vlan 20
    #    switchport mode trunk
    # !
    # interface Management1
    #    ip address dhcp
    #    ipv6 address auto-config
    # !

    - name: Merge provided configuration with device configuration.
      eos_l2_interfaces:
        config:
          - name: Ethernet1
            trunk:
              native_vlan: 10
          - name: Ethernet2
            access:
              vlan: 30
        state: merged

    # After state:
    # ------------
    #
    # veos#show running-config | section interface
    # interface Ethernet1
    #    switchport trunk native vlan 10
    #    switchport mode trunk
    # !
    # interface Ethernet2
    #    switchport access vlan 30
    # !
    # interface Management1
    #    ip address dhcp
    #    ipv6 address auto-config
    # !

    # Using replaced

    # Before state:
    # -------------
    #
    # veos2#show running-config | s int
    # interface Ethernet1
    #    switchport access vlan 20
    # !
    # interface Ethernet2
    #    switchport trunk native vlan 20
    #    switchport mode trunk
    # !
    # interface Management1
    #    ip address dhcp
    #    ipv6 address auto-config
    # !

    - name: Replace device configuration of specified L2 interfaces with provided configuration.
      eos_l2_interfaces:
        config:
          - name: Ethernet1
            trunk:
              native_vlan: 20
              trunk_vlans: 5-10, 15
        state: replaced

    # After state:
    # ------------
    #
    # veos#show running-config | section interface
    # interface Ethernet1
    #    switchport trunk native vlan 20
    #    switchport trunk allowed vlan 5-10,15
    #    switchport mode trunk
    # !
    # interface Ethernet2
    #    switchport trunk native vlan 20
    #    switchport mode trunk
    # !
    # interface Management1
    #    ip address dhcp
    #    ipv6 address auto-config
    # !

    # Using overridden

    # Before state:
    # -------------
    #
    # veos#show running-config | section interface
    # interface Ethernet1
    #    switchport access vlan 20
    # !
    # interface Ethernet2
    #    switchport trunk native vlan 20
    #    switchport mode trunk
    # !
    # interface Management1
    #    ip address dhcp
    #    ipv6 address auto-config
    # !

    - name: Override device configuration of all L2 interfaces on device with provided configuration.
      eos_l2_interfaces:
        config:
          - name: Ethernet2
            access:
              vlan: 30
        state: overridden

    # After state:
    # ------------
    #
    # veos#show running-config | section interface
    # interface Ethernet1
    # !
    # interface Ethernet2
    #    switchport access vlan 30
    # !
    # interface Management1
    #    ip address dhcp
    #    ipv6 address auto-config
    # !

    # Using deleted

    # Before state:
    # -------------
    #
    # veos#show running-config | section interface
    # interface Ethernet1
    #    switchport access vlan 20
    # !
    # interface Ethernet2
    #    switchport trunk native vlan 20
    #    switchport mode trunk
    # !
    # interface Management1
    #    ip address dhcp
    #    ipv6 address auto-config
    # !

    - name: Delete EOS L2 interfaces as in given arguments.
      eos_l2_interfaces:
        config:
          - name: Ethernet1
          - name: Ethernet2
        state: deleted

    # After state:
    # ------------
    #
    # veos#show running-config | section interface
    # interface Ethernet1
    # !
    # interface Ethernet2
    # !
    # interface Management1
    #    ip address dhcp
    #    ipv6 address auto-config




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
                                                                        <div>The configuration as structured data after module completion.</div>
                                                                <br/>
                                            <div style="font-size: smaller"><b>Sample:</b></div>
                                                <div style="font-size: smaller; color: blue; word-wrap: break-word; word-break: break-all;">The configuration returned will always be in the same format of the parameters above.</div>
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
                                                                        <div>The configuration as structured data prior to module invocation.</div>
                                                                <br/>
                                            <div style="font-size: smaller"><b>Sample:</b></div>
                                                <div style="font-size: smaller; color: blue; word-wrap: break-word; word-break: break-all;">The configuration returned will always be in the same format of the parameters above.</div>
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
                                                <div style="font-size: smaller; color: blue; word-wrap: break-word; word-break: break-all;">[&#x27;interface Ethernet2&#x27;, &#x27;switchport access vlan 20&#x27;]</div>
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

- Nathaniel Case (@qalthos)


.. hint::
    If you notice any issues in this documentation, you can `edit this document <https://github.com/ansible/ansible/edit/devel/lib/ansible/plugins//?description=%23%23%23%23%23%20SUMMARY%0A%3C!---%20Your%20description%20here%20--%3E%0A%0A%0A%23%23%23%23%23%20ISSUE%20TYPE%0A-%20Docs%20Pull%20Request%0A%0A%2Blabel:%20docsite_pr>`_ to improve it.


.. hint::
    Configuration entries for each entry type have a low to high priority order. For example, a variable that is lower in the list will override a variable that is higher up.
