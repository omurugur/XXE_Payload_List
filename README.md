<h2>XML External Entity Vulnerability Payload List</h2>

<b>Overview:</b>

An XML External Entity attack is a type of attack against an application that parses XML input. This attack occurs when XML input containing a reference to an external entity is processed by a weakly configured XML parser. This attack may lead to the disclosure of confidential data, denial of service, server side request forgery, port scanning from the perspective of the machine where the parser is located, and other system impacts.

The XML 1.0 standard defines the structure of an XML document. The standard defines a concept called an entity, which is a storage unit of some type. There are a few different types of entities, external general/parameter parsed entity often shortened to external entity, that can access local or remote content via a declared system identifier. The system identifier is assumed to be a URI that can be dereferenced (accessed) by the XML processor when processing the entity. The XML processor then replaces occurrences of the named external entity with the contents dereferenced by the system identifier. If the system identifier contains tainted data and the XML processor dereferences this tainted data, the XML processor may disclose confidential information normally not accessible by the application. Similar attack vectors apply the usage of external DTDs, external stylesheets, external schemas, etc. which, when included, allow similar external resource inclusion style attacks.

Attacks can include disclosing local files, which may contain sensitive data such as passwords or private user data, using file: schemes or relative paths in the system identifier. Since the attack occurs relative to the application processing the XML document, an attacker may use this trusted application to pivot to other internal systems, possibly disclosing other internal content via http(s) requests or launching a CSRF attack to any unprotected internal services. In some situations, an XML processor library that is vulnerable to client-side memory corruption issues may be exploited by dereferencing a malicious URI, possibly allowing arbitrary code execution under the application account. Other attacks can access local resources that may not stop returning data, possibly impacting application availability if too many threads or processes are not released.

Note that the application does not need to explicitly return the response to the attacker for it to be vulnerable to information disclosures. An attacker can leverage DNS information to exfiltrate data through subdomain names to a DNS server that he/she controls.

<b>Reference:</b>

XML External Entity point_right https://www.owasp.org/index.php/XML_External_Entity_(XXE)_Processing


<h3>Cloning an Existing Repository ( Clone with HTTPS )</h3>
<pre><code>
root@slife:~# git clone https://github.com/omurugur/xxe-payload-list.git
</code></pre>
<h3>Cloning an Existing Repository ( Clone with SSH )</h3>
<pre><code>
root@slife:~# git clone git@github.com:omurugur/xxe-payload-list.git
</code></pre>

<h3>Contact :</h3>

<h5>Mail : omurugur12@gmail.com </h5>

<h5>Linkedin  : https://www.linkedin.com/in/omurugur-sibergüvenlik/ </h5>

<h5>GitHub  : https://github.com/omurugur </h5>

<h5>Donate!</h5>
</p>
Support the authors:


<h5>LiberaPay:</h5>

<noscript><a href="https://liberapay.com/slife/donate"><img alt="Donate using Liberapay" src="https://liberapay.com/assets/widgets/donate.svg"></a></noscript>
