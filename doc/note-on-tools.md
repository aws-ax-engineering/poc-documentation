<div align="center">
	<p>
		<img alt="AWS Logo" src="https://raw.githubusercontent.com/amex-engineering/static/main/images/aws-logo.png?sanitize=true" width=150 />
    <br />
	</p>
  <h3>legato engineering platform poc</h3>
  <h5>1.4 A Note on Tools</h5>
</div>
<br />




Tools are not neutral components. A chosen tool will either enable or impede architectural and engineering quality.  

Tools are not a strategic capability. TCO includes the opportunity cost of what a team could otherwise be working on. In other words, use SaaS tools wherever architecturally appropriate options exist. The use of a qualified SaaS is one of the most accelerating strategies you can adopt, paying dividends on an ongoing basis.  

The statement, “It’s not about the tools” means only: No tool is going to solve for or remove the impact of your organizational challenges and culture.  

Suitability to a software-defined and domain-bounded implementation is a prerequisite for all tools and technologies.

### 1.3.1 General tool selection criteria

* Use small, focused tools that are exceptional in their implementation and interoperate well, over monolithic solutions. (One measure of _exceptional_ being, is an architecture designed clearly to be user-centric, with a roadmap based on real feedback.)  

* Use domain bounded tools and frameworks that can be implemented to enable low-friction changes to higher value alternatives as they become available. Domain-bounded implementation in this case refers to the degree of difficulty in changing the tool when a higher-value product comes along. Implement in such a way that the cost to change is relatively low and not a blocker to the adoption of alternative technologies.  

* Prefer solutions offered by qualified SaaS providers over self-managed options, being painfully honest about the actual costs of ownership.  

* Use or implement software that has an API.  
* The API should be easy to use and include functional examples.  
* The API should have all the functionality that the application provides.  
* The API should be accessible by more than one language and platform.  
* Coding around deficiencies in the product should be easier than recreating the product.  
* All data stored in the product should be readable and writeable by other applications.  
* For products that have authentication requirements, they should be able to authenticate and authorize from external, configurable sources. (In particular, they must integrate into the general AuthN/Z scheme of the overall platform, either natively or through custom integration.)
* Place a high value on the depth of community involvement and support.  

### 1.3.2 Tools and technologies used in the poc

For the most part, the poc is a demo of a user experiences related to engineering platforms built on AWS. Except where expressly highlighted, invidual tools may be selcted simply to demonstrate an implementation experience rather than as a recommendation around the general use of the tool. For example, while Hashi Vault is apparently a standard with AMEX, since the poc will not have access we will make use of AWS Secrets Manager. This is not a suggestion to the general use of SM but merely to facilitate progress on the poc.  

#### 1.3.2.1 Artifact stores

**terraform state**  

[terraform cloud](https://www.terraform.io). Access to a quality SaaS terraform state backend addresses a key infrastructure bootstrap challenge for fully software-defined lifecycle management. e.g., you do not need to bootstrap a state store.  

Refer to vendor [documentation](https://www.terraform.io/docs/cloud/index.html) for detailed questions.  

**secrets management**

AWS Secrets Manager  

For pipeline automation, will use [teller](https://github.com/tellerops/teller) for commandline interaction.  

**pipelines**

[github actions](https://github.com/features/actions)

**build-artifact stores**

[**github packages**](https://github.com/features/packages)  

continued...  

<hr>  

[<kbd> <br> Home <br> </kbd>](../README.md)
