Deploying to Github Pages
=========================

We are going to deploy our site to Github Pages using Github Actions. To do this


#. **Actions and Workflows**

   

#. **Workflow for Building Site and Pushing**

   The workflow below can be used for building a sphinx site and pushing it to Github::

        name: Sphinx build

        on: push

        jobs:
        sphinx-build:
            runs-on: ubuntu-latest
            steps:
            - uses: actions/checkout@v2
            - name: Build HTML
              with:
                pre-build-command: "apt install -y pandoc"
              uses: ammaraskar/sphinx-action@0.4
            - name: Upload artifacts
              uses: actions/upload-artifact@v1
              with:
                name: html-docs
                path: docs/_build/html/
            - name: Deploy
              uses: peaceiris/actions-gh-pages@v3
              if: github.ref == 'refs/heads/main'
              with:
                github_token: ${{ secrets.GITHUB_TOKEN }}
                publish_dir: docs/_build/html

   Let's break down the steps:

   #. First, we checkout the repo.
   #. Next, we build the sphinx page. By default, it will install packages within ``docs/requirements.txt``, but we also need the container to install pandocs for everything to work.
   #. Next, we upload the built site.
   #. Deploy the site. 