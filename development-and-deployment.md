# How to develop and deploy the project?

1. Create a new GitHub repository based on the [HTML and Vanilla JS template repository](https://github.com/new?template_name=mits-html-and-vanilla-js-v1&template_owner=marketable-it-skills).
2. Create your solution in the `/src` folder.
3. When you push a commit to GitHub, an auto-deployment process will start according to the GitHub Actions defined in the repository (`.github` folder). During this process, a Docker image will be built and stored in the Github Container Registry.
4. Modify the following line in the `docker-compose.yml` according to your GitHub username and your repository name: `image: ghcr.io/<your-github-account>/<your-repo-name>:latest`. E.g if your repo name is `s17-ts2025-module_a-static-website-design-solution` and your Github account is `asdf2025`: `image: ghcr.io/asdf2025/s17-ts2025-module_a-static-website-design-solution:latest`
5. Start the Docker container using the `docker compose up -d` command.
6. Your deployment will be accessible at the [http://localhost](http://localhost) URL.

