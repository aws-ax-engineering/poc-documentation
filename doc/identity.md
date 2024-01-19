<div align="center">
	<p>
		<img alt="AWS Logo" src="https://raw.githubusercontent.com/amex-engineering/static/main/images/aws-logo.png?sanitize=true" width=150 />
    <br />
	</p>
  <h3>legato engineering platform poc</h3>
  <h5>1.2 Identity and Authorization</h5>
</div>
<br />


![bootstrap](https://img.shields.io/badge/document-EarlyDraft-yellow.svg?style=for-the-badge&logo=markdown)  

Identity and authorization is a _solve-for-first_ issue, with repercussions across a platform product implementation.    

IDP is itself a capability that will need to be made available to platform users as well as incorporated into the platform. Effective productization of engineering platform capabilities requires the abstraction of the platform user's identity from the underlying infrastructure IAM capabilities; as you are experiencing right now as you read this document on GitHub. Your identity integration with GitHub is not built around direct or SSO integration with their infrastructure providers IAM capability. Customer identity within GitHub is within an Abstraction layer.  

If you are going to deliver a self-serve experience for internal consumers of a delivery infrastructure platform, how will you enable those internal teams to self-manage team creation and membership? When a team adds a team member, how will that team member automatically have access to all of the team resources?  

Obviously AMEX has idp capabilities. As the poc will not have access with those resources we will not be able to demonstrate the developer experience using those  same resources. Instead, we will make use of an auth0.com free-tier tenant, not as a recommendation or requirement in any sense, but only to support poc functionality with the assuming that any future work to implement any of the poc capabilities would be through the use of actual AMEX identity resources.  

<hr>  

[<kbd> <br> Home <br> </kbd>](../README.md)
