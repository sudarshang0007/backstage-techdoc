# Catalog Configuration in Backstage

The Backstage catalog is used to manage and register entities such as services, APIs, and websites.

---

## 📄 Basic Catalog Entity Configuration

Here’s an example of a `catalog-info.yaml` for a simple service:

```yaml
apiVersion: backstage.io/v1alpha1
kind: Component
metadata:
  name: my-service
  description: "My sample service in Backstage"
  annotations:
    backstage.io/techdocs-ref: dir:.
spec:
  type: service
  owner: team-a
  lifecycle: production
```

## Key fields

- `apiVersion` - The Backstage API version.
- `kind` - The type of entity (Component, API, Resource, etc.).
- `metadata` - Contains metadata about the entity.
- `spec` - Defines details about the entity.

## Annotations for TechDocs

```yaml
annotations:
  backstage.io/techdocs-ref: dir:.
```

## 🛠️ Registering Entities in Backstage

Navigate to the Create button in Backstage.
Select Register an existing component.
Provide the URL to your catalog-info.yaml file.
Click Analyze and then Import.

## 🎯 Catalog Entity Types

- `Component` – Represents a service or system.
- `API` – Describes APIs that the component exposes.
- `Resource` – Represents databases, storage, or other external resources.

## 🔄 Updating Catalog Entities

To update an entity:

- Modify the catalog-info.yaml file.
- Push the changes to your repository.
- Autobahn will automatically sync the changes.


---

✅ **Done!**  
You can now generate and integrate these docs with TechDocs in Backstage. Let me know if you need help with anything else! 🚀
