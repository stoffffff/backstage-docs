# What are techdocs ?
#### TechDocs is Backstage’s "docs-like-code" solution.<br>

It allows engineers to write documentation in Markdown files that live directly inside their service's source code repository. Backstage then automatically fetches, transforms, and renders those files into a beautiful, centralized documentation site within the portal.<br>

#### The utility:<br>

Centralization: No more hunting through Confluence, Notion, or READMEs across 100 different repos. All docs are in one place.<br>
Ownership: Since the docs live in the code repo, the same developers who write the code maintain the documentation.<br>
Automation: It uses a "build once, view anywhere" approach—typically using MkDocs under the hood to generate the final HTML.<br>

#### Hands-on example:<br>
#### STEP 1️⃣<br>
In ***app.config.yaml*** file, the following config tells Backstage how to handle the documentation of components.<br>

![alt text](screenshots/techdocs1.png)

#### What does that mean ?<br>
#### builder: "local": The Backstage backend is responsible for "preparing" the docs (fetching the Markdown files from your Git provider) whenever a user tries to view them.<br>

#### generator: runIn: "docker": To convert Markdown to HTML, Backstage will spin up a Docker container (usually spotify/techdocs) containing MkDocs. This keeps your host machine clean but requires Docker to be installed on the server.<br>

#### publisher: type: "local": Once the HTML is generated, it is stored on the local file system of the Backstage server rather than a cloud bucket (like S3 or GCS).<br>

### IMPORTANT:<br>
- This is best for: Local development, small teams, or "Proof of Concept" (PoC) setups.<br>
- This is not ideal for Production.<br>
- The config in the screenshot above is the default one that you will find if you download Backstage from their official git repository.<br> 

#### STEP 2️⃣<br>

