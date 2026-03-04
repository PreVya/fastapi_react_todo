Github workflow details here:

1. Create a OIDC provider in AWS for github
   Provider type: OpenID Connect
   Provider url: https://token.actions.githubusercontent.com
   Audience: sts.amazonaws.com
   <img width="1536" height="101" alt="image" src="https://github.com/user-attachments/assets/4abc4acb-46e9-4de7-8433-a98eb6843ae9" />

2. Assign an exsiting role to it or if created new then following should be its Trust policy:
   <img width="1536" height="632" alt="image" src="https://github.com/user-attachments/assets/f8e91bda-2197-4a46-8d24-5addc9768bb5" />

3. Add secrets like AWS_ACCOUNT_ID, AWS_REGION, ECR_REPO etc to github secrets
   <img width="1076" height="461" alt="image" src="https://github.com/user-attachments/assets/2a6fad77-d3e1-435c-b20e-6f2b68812891" />

4. Write the github workflow in project root directory under .github/workspace (Example write app.yml file in .github/workspace/app.yml)
