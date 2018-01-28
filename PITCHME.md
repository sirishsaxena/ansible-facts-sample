# Using Ansible Facts to Make Decisions in Playbooks

Presenter: Will Boyd

---

Ansible playbooks can be a powerful way to perform a **series of tasks.**

![Series](assets/img/series.png)

---

But sometimes you need something a little more complex, like the ability for a playbook to **make a decision** and act on it.

![Series](assets/img/decision.png)

---

**Scenario:** A playbook that can install a package on hosts with different linux distributions.

---

<table>
<tr><td /><td>**Debian (apt)**</td><td>**CentOS (yum)**</td></tr>
<tr>
<td>**Command Line**</td>
<td><pre style="box-shadow: none;">$ apt install apache2</pre></td>
<td><pre style="box-shadow: none;">$ yum install httpd</pre></td>
</tr>
<tr class="fragment">
<td>**Ansible task**</td>
<td>
<pre style="box-shadow: none;">
- name: install apache
  package:
    name: apache2
    state: latest
</pre>
</td>
<td>
<pre style="box-shadow: none;">
- name: install apache
  package:
    name: httpd
    state: latest
</pre>
</td>
</tr>
</table>

---

**Ansible Facts** - Information about a host which ansible automatically gathers. Facts can be referenced as variables within ansible.

**Such as:**
  - Linux Distribution / OS
  - Hardware info
  - A lot more...

---

# Live demonstration

---
# That's it!

In the description below:

* Sample project source code on GitHub.
* Links to relevant Ansible documentation.