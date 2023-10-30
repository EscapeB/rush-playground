# Symlink Demo

This is a simple demo project to show how to reproduce symbolic issues in rush deploy.

## Reproduce step

1. Create symlink

```bash
# Create a symlink outside Monorepo root, this symlink should inside dependencies' folder. 
# For example, we created a fake dependency named `dependency-with-error`, and create a python3 symlink in its folder.
ln -s /usr/bin/python3 node_modules/dependency-with-error/build/python3
```

2. Run rush deploy

```bash
rush deploy -p symlink-demo -t output --overwrite
```

