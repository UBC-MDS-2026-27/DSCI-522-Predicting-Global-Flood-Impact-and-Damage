# Contributing

We welcome feedback, bug reports, suggestions and contributions to this data analysis project. Please follow our [Code of Conduct](CODE_OF_CONDUCT.md).

## Report a Bug or Suggest a Change
Create an associated issue in this repository. For a bug, illustrate the bug by describing how to reproduce it including at least one error message. For a suggestion, explain what you want to change and the reason.

## Set up environment
We use Docker to ensure that all contributors work in the same environment with same Python and package versions. Please follow the ["How to run the analysis" in README](README.md#how-to-run-the-analysis) (download and install the Docker, clone the repository and enter the project directory, create an SSH key and download the image).

The detailed instructions to run the analysis lies in [README](README.md).

## Working in the container
We use Positron to work inside the Docker container through SSH.

### Before your first connection
1. Install [Positron](https://positron.posit.co/download.html).
2. Check your Git configuration:
```bash
git config --global user.name
git config --global user.email
```
if either is missing, set it by:
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```
### Connect to the container
1. run the following while Docker Desktop opened: 
```bash
docker compose up -d
docker compose ps
```
Confirm that `analysis-env` is running.

2. Open Positron, open the Command Palette (`Cmd+Shift+P` on Mac, `Ctrl+Shift+P` on Windows). Type and run **Remote SSH: Show Remote Menu**, then pick **Connect to Host**.

3. Enter `root@localhost:2222`. If asks for the platform of the remote host,, select **Linux** as the remote platform and accept the SSH host fingerprint.

4.Open the Command Palette(same as step 2), select **Python: Select Interpreter**, then **Enter interpreter path...** and enter `/opt/venv/bin/python`.

5. To check, run `import sys; print(sys.executable)` in the Console. It should print `/opt/venv/bin/python`.

### After Using
When you are done, close the Positron window, then stop the container in a terminal on your computer:
```bash
docker compose down
```

### If you are not connecting
- **SSH key is missing:** Follow the SSH key setup instructions in the [README](README.md#how-to-run-the-analysis).
- **SSH key passphrase is requested:** Enter the passphrase you created for your SSH private key.

- **Positron cannot establish an SSH connection:** Check that the container is running with `docker compose ps`.

- **Remote host identification has changed**: you are using a new image. Run `ssh-keygen -R "[localhost]:2222"`, then connect again.

- **Port 2222 is already in use**: change the first `2222` in `docker-compose.yml` to another number (e.g. `2223`), and connect to that port instead.


More details in : [Working in a container over ssh with Positron](https://ubc-dsci.github.io/reproducible-and-trustworthy-workflows-for-data-science/lectures/containers-ssh-positron.html)


## Make a Change
Please make changes after creating your own branch:
```bash
git switch -c your-branch-name
```

## AI Policy
If you are using generative AI, please follow the AI policy below:
Every team member is responsible for understanding and checking any code or text they submit, whether or not AI helped write it. Pull requests and GitHub issues are opened by team members, never by an AI agent or chat bot. We may use AI agents to help double-check the code before merging pull requests, but ultimately it is human reviewers who make the final decisions and merge the pull requests. Contributors must keep track of their AI usage in their pull request, including the tool used, how it was used, representative prompts should be included.

