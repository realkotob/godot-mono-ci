# godot-ci
Docker image to deploy Godot Engine games

## Docker Hub
https://hub.docker.com/r/barichello/godot-ci/

## Usage example
A `.gitlab-ci.yml` is included in this project as a usage example.<br>
After adapting the paths and names according to your project needs you will need the following **Variable** set in GitLab for this image to work:

|Variable|Description|Example|
|-|-|-|
|$REMOTE_URL | The `git remote` where the web export will be hosted (in this case GitHub), it should contain your [deploy/personal access token](https://github.com/settings/tokens)|`https://<github username>:<deploy token>@github.com/<username>/<repository>.git`

Others variables are set automatically by the `gitlab-runner`<br>
The included `gitlab-ci.yml` is set to only run the export jobs when you commit a new `git tag`, i suggest not using "." or "," in your tag's name since it messes with Godot's export system and will lead to failed jobs.

Check other usage examples in these following projects:<br>
- [`aBARICHELLO/GAMINE`](https://github.com/aBARICHELLO/gamine)<br>
- [`aBARICHELLO/game-off`](https://github.com/aBARICHELLO/game-off)
