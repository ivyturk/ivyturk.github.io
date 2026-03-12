[Home](/README.md) // [Publications](/publications.md) // [Academic and Employment History](/my_history.md) // [Teaching Experience](/teaching.md) // [Project Ideas](./project_ideas.md)

Notice: I've had multiple affiliations with different project lengths, but most ideas here can be adjusted to fit these varying timescales. The suggested timescale for some projects is indicated with [N months], for example [3] indicates a three month project.

# Tool Creation
* Designing and implementing novel safety tools to aid those experiencing various types of interpersonal harms.
  * [6] Mobile phone lockdown and cleanup. Goal is to provide a single-use tool that identifies harmful applications and processes, excessive or unauthorised access, suspicious files, etc and either removes or greatly restricts their capabilities. This project could take inspiration from e.g. [iOS Lockdown Mode](https://support.apple.com/en-gb/105120) or [chroot (application) jails](https://www.redhat.com/en/blog/set-linux-chroot-jails)
  * [3-6] Evidence gathering tools. Goal is an application which provides secure storage of information and media even if the device itself is compromised (e.g. domestic abuse scenarios where the partner has access to the phone). Our prior work on vault apps is [here](https://www.usenix.org/system/files/soups2024-geeng.pdf) as possible inspiration. Possible extensions could look into ensuring digital evidence is admissible in court, or at least providing integrity and authenticity.
  * Covert information sharing tools. Simple implementations [3] could set up a private channel for communications with trusted third parties, or extended versions [6] could implement either existing crypto protocols for secure (+anonymous?) comms or have a go at designing your own and attempting to break it. Extensions could include authenticating endpoints are not compromised (e.g. shared phones) or designing a system for police or NGO contact.
* Any prototype implementation with evaluation for novel privacy and safety tools. Some suggestions might be
  * Location privacy and spoofing, building off of novel suggestions from our [unwanted trackers research](https://dl.acm.org/doi/10.1007/978-3-031-43033-6_9) or other contexts.
  * Shared access home systems (such as IoT networks) and compartmentalisation, designing for multiple superuser environments and/or allowing for delegation of access controls while considering adversarial scenarios
  * Abuse escape planning tools.
* Any sufficiently distinct clone of an existing security or safety tool, such as website scanning, port scanning, malware identification etc. Sufficiently different implies you cannot copy an open-source tool, such as by writing in a different language or using your own methodology for the same goal.

# System Evaluation
* [3] Evaluating any existing tools (ideas above) for safety, security, usability.
  * [3] Usability: Either run a usability study with established methods (heuristic evaluation/Nielson principles, cognotive walkthrough, talk-aloud or task-based user studies) or design an evaluation scenario to test usability, such as our past gameified research on [trackers](https://dl.acm.org/doi/pdf/10.1145/3688459.3688477) and [IoT](https://www.usenix.org/conference/soups2025/presentation/turk).
  * [3] Safety: Explore the potential misuse of tools using threat modelling and similar methods. Suggested to build off of the [HARMS framework](https://arxiv.org/abs/2502.07116).
  * Security: Break things (see disclaimer below) to identify security issues with deployed tools. Likely to be more of a red teaming/bug bounty style approach than formalised project, although I got away with that for my own [master's thesis](https://www.cl.cam.ac.uk/~kst36/documents/meng-dissertation.pdf).

# Breaking Things
Disclaimer: Permissible hacking methods, tools, and objectives vary widely by jurisdiction. We must both be well aware of the legality justifications of any of the following ideas before commencing a project.
Do not attempt to hack anything you do not own and/or have permission to work on. Use of VMs for software or own devices for hardware is strongly advised.
* Security analysis of any device or software of interest, with express permission and law checking.
* Creation of opaque-box security tools
  * Packet capture and analysis. Think [WireShark](https://www.wireshark.org/) or [Ettercap](https://github.com/Ettercap/ettercap) tailored to your chosen communication method.
  * Fuzzing or similar blind-probing tools.
  * Anything that doesn't require reverse engineering, as it is illegal in Germany (but permissible in specific scenarios in the UK for example)
* Malware or phishing detection.
* Creation of scanning tools
  * [6] Web vulnerability scanning to identify SQLi, command and code injection, XSS, CSRF, etc
  * Misconfiguration scanning tools
  * [3] Port scanning e.g. [Nmap](https://nmap.org/) or extensions looking at firewall probing etc
  * Repository scanning for API keys, passwords, secrets etc 
