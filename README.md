# Render hugo on Connect

## Render the site & add a Manifest in public

```
Rscript -e 'blogdown::new_site()'
# Change in config.yaml the path to rsconnect endpoint
# For example baseurl: /hugoreprex/
# or /content/483/

# Build
Rscript -e 'blogdown::build_site()'
cd public && Rscript -e 'rsconnect::writeManifest()' && cd ..
git add . 
git commit -m "rebuild"
git push
```

## On Connect

- Publish
- From Git 
- Select a branch 
- Select directory > Public
- Title 
- Deploy