# Using Ansible Facts to Make Decisions in Playbooks

Presenter: Will Boyd

---

**Ansible Facts** - Information about a host which ansible automatically gathers.

**Such as:**
  - Linux Distribution / OS
  - Hardware info
  - A lot more...

---

One way to use facts:
**To dynamically make decisions in your playbooks.**

---

**Scenario:** We want a playbook that can install apache on multiple hosts, some running Debian-based linux distros and some running CentOS-based distros.

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
  apt:
    name: apache2
    state: latest
</pre>
</td>
<td>
<pre style="box-shadow: none;">
- name: install apache
  yum:
    name: httpd
    state: latest
</pre>
</td>
</tr>
</table>

---

<table>
<tr><td /><td>**Debian (apt)**</td><td>**CentOS (yum)**</td></tr>
<tr>
<td>**Ansible task**</td>
<td>
<pre style="box-shadow: none;">
- name: install apache
  apt:
    name: apache2
    state: latest
</pre>
</td>
<td>
<pre style="box-shadow: none;">
- name: install apache
  yum:
    name: httpd
    state: latest
</pre>
</td>
</tr>
</table>

---

<table>
<tr><td /><td>**Debian (apt)**</td><td>**CentOS (yum)**</td></tr>
<tr>
<td>**Ansible task**</td>
<td>
<pre style="box-shadow: none;">
- name: install apache
  **package:**
    name: apache2
    state: latest
</pre>
</td>
<td>
<pre style="box-shadow: none;">
- name: install apache
  **package:**
    name: httpd
    state: latest
</pre>
</td>
</tr>
</table>

---

# Live demonstration

---
# That's it!

In the description below:

* Sample project source code on GitHub.
* Links to relevant Ansible documentation.