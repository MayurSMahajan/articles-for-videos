# Self Hosting AppFlowy Cloud using EC2 instance - Updated on 28 Jan 2025

### Motivation

AppFlowy is rapidly developing with new updates. Therefore a lot of changes will occur in the process of self-hosting AppFlowy with EC2. I will try to this article with all the new changes as they occur. Therefore, this article should serve as an up-to-date reference for achieving our goal, that is to self host AppFlowy on EC2 instance. 

Thus I recommend you to always first read this article and then watch the video-tutorial and in case of a discrepancy, always stick with the steps mentioned in this article instead of the video.

> ✨ or star emoji indicates new updates in that step. 

> The official upgrade notes regarding self hosting can be found here: https://appflowy.com/docs/self-hosters-upgrade-notes

### Outline: 

Step 1: Amazon EC2 setup - same as the video

Step 2: Connect to your instance with SSH

Step 3: Setting up Docker

Step 4: Setting up AppFlowy Cloud server (New Updates) ✨

Step 4.3: Setting up OAuth with GitHub

Step 4.7: (Optional) Updating our EC2's inbound rule

Step 5: Setting up AppFlowy Client App

### Other updates: ✨

1. AppFlowy team has moved the admin frontend to `http://<public-ip/host>/console`, so that users can install Appflowy web on / `(http://<public-ip/host>`

---
### Updated Step 4 - Setting up AppFlowy Cloud Server ✨

1. Clone the latest AppFlowy repository
   `git clone https://github.com/AppFlowy-IO/AppFlowy-Cloud && cd AppFlowy-Cloud`
   
2. Make a new `.env` file and paste the contents of `deploy.env` into the `.env` file
   
3. In the video, we update `GOTRUE_EXTERNAL_GITHUB_REDIRECT_URI` to our domain name followed with `/gotrue/callback` path. New changes suggest that we directly update the 
   `FQDN` variable in the `.env` file. By doing this the `API_EXTERNAL_URL` will be set.

4. Finally all the steps related to pasting our `GOTRUE_EXTERNAL_GITHUB_CLIENT_ID` and `GOTRUE_EXTERNAL_GITHUB_SECRET` are the same. 

![how-will-env-file-look-like](https://github.com/user-attachments/assets/d657cd48-60bc-46e0-ad74-0fa65d3e95c7)


