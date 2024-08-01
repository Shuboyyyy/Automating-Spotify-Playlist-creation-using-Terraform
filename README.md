Spotify-Playlist-Creation-with-Terraform
Project Overview
This project involves using Terraform to create multiple Spotify playlists for different occasions like morning, evening, party night, etc. Terraform will be used to automate the creation and management of these playlists.

Prerequisites
Terraform Installed: Ensure Terraform is installed on your machine.
Docker Installed: Make sure Docker is installed and running.
Spotify Account: You need a Spotify account (without premium access)
Spotify Developer Account: Register and create an application to get the Client ID and Client Secret.
Spotify Provider for Terraform: Install and configure the Spotify provider for Terraform.
VS Code Editor: Recommended for editing Terraform files.
Steps to Complete the Project

Creating Terraform Code Start by setting up your Terraform project. Create a new directory for your Terraform project and navigate to it in your terminal. Create a file named main.tf.
Define Provider In main.tf, define the Spotify provider: provider "spotify" { api_key = "?" }
3. Need API Key
To interact with Spotify's API, you need a Client ID and Client Secret.

4. Start with App Creation
Go to the Spotify Developer Dashboard.
Log in with your Spotify account.
Click on "Create an App".
image
Fill in the required details and create the app.

Name	Description
My Playlist through Terraform	Create multiple Spotify playlists using Terraform.
*Redirect URIs: http://localhost:27228/spotify_callback
image
5. Enter Details
Create a file named .env to store your Spotify application's Client ID and Secret:

SPOTIFY_CLIENT_ID=<your_spotify_client_id>
SPOTIFY_CLIENT_SECRET=<your_spotify_client_secret>

6. Run the Spotify Auth App and Get the API Key
Make sure Docker Desktop is running, and start the authorization proxy server:

image
image

You should get “Authorization Successful” Message.

Continue Creating Terraform Code
Initialize and Apply Terraform Configuration Initialize the Terraform configuration: terraform init
​Apply the Terraform configuration: terraform apply

11. Verify Playlists on Spotify
After applying the Terraform configuration, log in to your Spotify account and verify that the playlists have been created and populated with the specified tracks.

Conclusion
By following these steps, you can automate the creation and management of multiple Spotify playlists using Terraform. This approach not only saves time but also ensures consistency across your playlists. Customize the playlists and tracks as per your preference to suit different occasions.
