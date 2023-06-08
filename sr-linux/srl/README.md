# Run the lab

From the current folder, deploy with containerlab

```bash
clab deploy
```

Start the web server by specifying the path to some templates (point to the shared template folder)

```bash
labctl serve -p ../../templates
```

## Send some configuration

Delete interfaces & default network instance (You can see the content of the **delete** script from the templates tab, the 4th tab in Config Engine)

[commit -l delete](config:)

Create some SRL ports!! (The compare/diff is optional, but you have to **commit** to move to the next step)

- [compare -l ports](config:)
- [commit -l ports](config:)

Enable ISIS as IGP in the default network instance

- [compare -l isis](config:)
- [commit -l isis](config:)

"Alternatively you can also configure the entire lab in one go \n\n[commit -l delete,ports,isis](config:)"

The route table reflects routes distributed by ISIS

[send -l show-route-table](config:)