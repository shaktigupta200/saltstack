# saltstack

<h3>Saltstack - <i> A Server Configuration Management Tool</i></h3><br />
<a href='https://docs.saltstack.com/en/latest'><img src='http://saltstack.com/wp-content/uploads/2014/12/saltStack_horizontal_dark_800x251.png' alt='salt-logo' height='40px' width='80px'/></a><br />
<b>What is SaltStack? </b><br />
Saltstack also called as 'salt' is an open source, python-based server configuration management tool and remote execution engine. Using the <a href='https://en.wikipedia.org/wiki/Infrastructure_as_Code'>Infrastruce as Code (IaC)</a> i.e. using machine-readable definition files file for configuration, approach of deployement and cloud management, salt competes with various server configuration tools like puppet, chef and ansible.<br />

<b>STARTING SALT</b>
<p>Salt functions on a master/minion topology. A master server acts as a central control bus for the clients, which are called minions. The minions connect back to the master.</p><br />
<table class="wikitable">
<tr>
<th>Tool Name</th>
<th>Released by</th>
<th>Method</th>
<th>Approach</th>
<th>Written in</th>
</tr>
<tr>
<th><a href="https://en.wikipedia.org/wiki/Ansible_(software)" title="Ansible (software)">Ansible Tower</a></th>
<td>Ansible (RedHat)</td>
<td>Push</td>
<td>Declarative &amp; Imperative</td>
<td><a href="https://en.wikipedia.org/wiki/Python_(programming_language)" title="Python (programming language)">Python</a></td>
</tr>
<tr>
<th><a href="https://en.wikipedia.org/wiki/CFEngine" title="CFEngine">CFEngine</a></th>
<td>CFEngine</td>
<td>Pull</td>
<td>Declarative</td>
<td>-</td>
</tr>
<tr>
<th><a href="https://en.wikipedia.org/wiki/Chef_(software)" title="Chef (software)">Chef</a></th>
<td>Chef</td>
<td>Pull</td>
<td>Imperative</td>
<td><a href="https://en.wikipedia.org/wiki/Ruby" title="Ruby">Ruby</a></td>
</tr>
<tr>
<th><a href="https://en.wikipedia.org/wiki/Otter_(software)" title="Otter (software)">Otter</a></th>
<td>Inedo</td>
<td>Push</td>
<td>Declarative &amp; Imperative</td>
<td>-</td>
</tr>
<tr>
<th><a href="https://en.wikipedia.org/wiki/Puppet_(software)" title="Puppet (software)">Puppet</a></th>
<td>Puppet</td>
<td>Pull</td>
<td>Declarative</td>
<td><a href="https://en.wikipedia.org/wiki/Ruby" title="Ruby">Ruby</a></td>
</tr>
<tr>
<th><a href="https://en.wikipedia.org/wiki/SaltStack" class="mw-redirect" title="SaltStack">SaltStack</a></th>
<td>SaltStack</td>
<td>Push and Pull</td>
<td>Declarative &amp; Imperative</td>
<td><a href="https://en.wikipedia.org/wiki/Python_(programming_language)" title="Python (programming language)">Python</a>
<p><br /></p>
</td>
</tr>
</table>

<h3>Salt Architecture</h3><br />
<img src='https://github.com/shaktigupta200/saltstack/blob/master/saltstack%20workflow.png' alt='salt architecture' />
<br/>
<h2>Installing Salt</h2>
<b>Bootstrap - Multi-Platform</b></br>
<p>Salt Bootstrap is a shell script that detects the target platform and selects the best installation method.<a href='https://docs.saltstack.com/en/latest/topics/tutorials/salt_bootstrap.html#supported-operating-systems' target="_blank">(Supported Platforms)</a>

<dl>
  <dt>On the Salt master</dt>
  <dd>$ curl -L https://bootstrap.saltstack.com -o install_salt.sh</dd>
  <dd>$ sudo sh install_salt.sh -P -M</dd>
  <dt>On the Salt minion</dt>
  <dd>$ curl -L https://bootstrap.saltstack.com -o install_salt.sh</dd>
  <dd>$ sudo sh install_salt.sh -P</dd>
</dl>
</p>
<br />
<h3>Setting Up salt master</h3><br />
Turning on the Salt Master is easy -- just turn it on! The default configuration is suitable for the vast majority of installations. The Salt Master can be controlled by the local Linux/Unix service manager:
<dl>
<dt>On Systemd based platforms (newer Debian, openSUSE, Fedora):</dt>
<dd>$ systemctl start salt-master</dd>
<dt>On Upstart based systems (Ubuntu, older Fedora/RHEL):</dt>
<dd>$ service salt-master start</dd>
<dt>On SysV Init systems (Gentoo, older Debian etc.):</dt>
<dd>$ /etc/init.d/salt-master start</dd>
<dt>Alternatively, the Master can be started directly on the command-line:</dt>
<dd>$ salt-master -d</dd>
<dt>The Salt Master can also be started in the foreground in debug mode, thus greatly increasing the command output:</dt>
<dd>$ salt-master -l debug</dd>
</dl>

