Github workflow details here:<br>

1. Create a OIDC provider in AWS for github<br>
   Provider type: OpenID Connect<br>
   Provider url: https://token.actions.githubusercontent.com<br>
   Audience: sts.amazonaws.com<br>
   <img width="1536" height="101" alt="image" src="https://github.com/user-attachments/assets/4abc4acb-46e9-4de7-8433-a98eb6843ae9" /><br>

2. Assign an exsiting role to it or if created new then following should be its Trust policy:<br>
   <img width="1536" height="632" alt="image" src="https://github.com/user-attachments/assets/f8e91bda-2197-4a46-8d24-5addc9768bb5" /><br>

3. Add secrets like AWS_ACCOUNT_ID, AWS_REGION, ECR_REPO etc to github secrets<br>
   <img width="1076" height="461" alt="image" src="https://github.com/user-attachments/assets/2a6fad77-d3e1-435c-b20e-6f2b68812891" /><br>

4. Write the github workflow in project root directory under .github/workspace (Example write app.yml file in .github/workspace/app.yml)<br>

5. Go to Actions tab in repo and run the workspace.<br>
   <img width="1907" height="767" alt="image" src="https://github.com/user-attachments/assets/1f5a864f-02a9-4e5a-b44c-13ce37d23488" /><br>
