:source: 


.. _arista.eos.eos_vlans_:


arista.eos.eos_vlans -- Manage VLANs on Arista EOS devices.
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++


.. contents::
   :local:
   :depth: 1


Synopsis
--------
- This module provides declarative management of VLANs on Arista EOS network devices.




Parameters
----------

.. raw:: html

    <table  border=0 cellpadding=0 class="documentation-table">
        <tr>
            <th colspan="2">Parameter</th>
            <th>Choices/<font color="blue">Defaults</font></th>
                            <th>Configuration</th>
                        <th width="100%">Comments</th>
        </tr>
                    <tr>
                                                                <td colspan="2">
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
                                            <div>A dictionary of VLANs options</div>
                                                        </td>
            </tr>
                                                            <tr>
                                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>name</b>
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
                                            <div>Name of the VLAN.</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>state</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">string</span>
                                                                    </div>
                                    </td>
                                <td>
                                                                                                                            <ul style="margin: 0; padding: 0"><b>Choices:</b>
                                                                                                                                                                <li>active</li>
                                                                                                                                                                                                <li>suspend</li>
                                                                                    </ul>
                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>Operational state of the VLAN</div>
                                                        </td>
            </tr>
                                <tr>
                                                    <td class="elbow-placeholder"></td>
                                                <td colspan="1">
                    <div class="ansibleOptionAnchor" id="parameter-"></div>
                    <b>vlan_id</b>
                    <a class="ansibleOptionLink" href="#parameter-" title="Permalink to this option"></a>
                    <div style="font-size: small">
                        <span style="color: purple">integer</span>
                                                 / <span style="color: red">required</span>                    </div>
                                    </td>
                                <td>
                                                                                                                                                            </td>
                                                    <td>
                                                                                            </td>
                                                <td>
                                            <div>ID of the VLAN. Range 1-4094</div>
                                                        </td>
            </tr>
                    
                                                <tr>
                                                                <td colspan="2">
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

    
    # Using deleted

    # Before state:
    # -------------
    #
    # veos(config-vlan-20)#show running-config | section vlan
    # vlan 10
    #    name ten
    # !
    # vlan 20
    #    name twenty

    - name: Delete attributes of the given VLANs.
      eos_vlans:
        config:
          - vlan_id: 20
        state: deleted

    # After state:
    # ------------
    #
    # veos(config-vlan-20)#show running-config | section vlan
    # vlan 10
    #    name ten


    # Using merged

    # Before state:
    # -------------
    #
    # veos(config-vlan-20)#show running-config | section vlan
    # vlan 10
    #    name ten
    # !
    # vlan 20
    #    name twenty

    - name: Merge given VLAN attributes with device configuration
      eos_vlans:
        config:
          - vlan_id: 20
            state: suspend
        state: merged

    # After state:
    # ------------
    #
    # veos(config-vlan-20)#show running-config | section vlan
    # vlan 10
    #    name ten
    # !
    # vlan 20
    #    name twenty
    #    state suspend


    # Using overridden

    # Before state:
    # -------------
    #
    # veos(config-vlan-20)#show running-config | section vlan
    # vlan 10
    #    name ten
    # !
    # vlan 20
    #    name twenty

    - name: Override device configuration of all VLANs with provided configuration
      eos_vlans:
        config:
          - vlan_id: 20
            state: suspend
        state: overridden

    # After state:
    # ------------
    #
    # veos(config-vlan-20)#show running-config | section vlan
    # vlan 20
    #    state suspend


    # Using replaced

    # Before state:
    # -------------
    #
    # veos(config-vlan-20)#show running-config | section vlan
    # vlan 10
    #    name ten
    # !
    # vlan 20
    #    name twenty

    - name: Replace all attributes of specified VLANs with provided configuration
      eos_vlans:
        config:
          - vlan_id: 20
            state: suspend
        state: replaced

    # After state:
    # ------------
    #
    # veos(config-vlan-20)#show running-config | section vlan
    # vlan 10
    #    name ten
    # !
    # vlan 20
    #    state suspend






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
                                                                        <div>The configuration as structured data prior to module invocation.</div>
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
                                                <div style="font-size: smaller; color: blue; word-wrap: break-word; word-break: break-all;">[&#x27;vlan 10&#x27;, &#x27;no name&#x27;, &#x27;vlan 11&#x27;, &#x27;name Eleven&#x27;]</div>
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
