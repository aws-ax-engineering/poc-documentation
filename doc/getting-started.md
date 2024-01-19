<div align="center">
	<p>
		<img alt="AWS Logo" src="https://raw.githubusercontent.com/amex-engineering/static/main/images/aws-logo.png?sanitize=true" width=150 />
    <br />
	</p>
  <h3>legato engineering platform poc</h3>
  <h5>1. poc engineering contributor getting started</h5>
</div>
<br />

### 1.1 setting up your AWS credentials

_pending_  

**Programmatic Credentials**  

_pending_  

### 1.2 POC Platform access  

_pending_  

### 1.3 Any other SaaS credentials

| Tool                | Access           | Tier                | org              | Comments                                |
|---------------------|:----------------:|:-------------------:|------------------|-----------------------------------------|
| github              | :wave:           | :free:              | amex-engineering | vcs, pipeline, registry                 |
| terraform cloud     | :wave:           | :free:              | amex-engineering | terraform state only (local mode)       |


:wave: = Ask another team member to invite you  
:free: = Free tier only  

### 1.4 github team name conventions

**Team:** core-team  

For poc engineering members or collaberators who are working on poc content.  

### 2.2 Repository naming conventions

| Prefix- or -Suffix     | Description                                        |
|------------------------|----------------------------------------------------|
| poc-aws-               | Infrastructure pipelines that manage core, cloud vendor specific platform domains |
| poc-api-               | Platform managegment APIs, not _cloud_ specific |
| poc-service-           | 3rd party services, self-managed by DI (Kiali, argocd, etc) |
| poc-kit-               | Language or custom resource Starter Kits<sup>†</sup> (psk-kit-java, psk-kit-orb, psk-kit-circleci-executor) |
| -action                | Custom github action |
| -runner                | Custom github runners (private or hosted) |
| -container             | Special purpose images (e.g., certificate-init-container) |
| poc-operator-          | Custom K8s operators |
| demo-                  | Example customer apps. Can include demo-_team_ where multi team interaction is being demonstrated |
| (no convention)        | Executables (e.g., cli), or other one-offs |

<sup>†</sup>language starterkits include many platform specific elements, such as ci/cd and observabaility  

### 1.5 app.terraform.io

url: `https://app.terraform.io/app/amex-engineering`  

Once you have access, generate a personal api token and add the credentials to your local environment:
```
$ cat <<EOF > ~/.terraformrc
credentials "app.terraform.io" {
  token = "your_personal_token_here"
}
```

The pipeline api token is available in secrets manager.  
```
poc/terraform-cloud/team-api-token
```

<hr>  

[<kbd> <br> Home <br> </kbd>](../README.md)
