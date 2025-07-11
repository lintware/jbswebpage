# Projects Management

This directory contains the JSON data files for the JBS website projects.

## projects.json

The `projects.json` file contains all project data that is dynamically loaded into the projects page. This makes it easy for developers to add, remove, or modify projects without touching the HTML code.

### Structure

```json
{
  "projects": [
    {
      "id": "unique-project-id",
      "title": "Project Title",
      "client": "Client Name",
      "period": "Project Period",
      "status": "ongoing|completed",
      "categories": ["category1", "category2"],
      "gradient": "from-jbs-purple to-jbs-blue",
      "jobScope": [
        "Job scope item 1",
        "Job scope item 2"
      ],
      "manpower": ["Role 1", "Role 2", "Role 3"],
      "clientFullName": "Full Client Name (optional)"
    }
  ],
  "categories": [
    {
      "id": "category-id",
      "name": "Category Display Name",
      "description": "Category description"
    }
  ]
}
```

### Adding a New Project

1. Open `content/projects.json`
2. Add a new project object to the `projects` array
3. Include all required fields:
   - `id`: Unique identifier (use kebab-case)
   - `title`: Project title
   - `client`: Client name
   - `period`: Project timeline
   - `status`: "ongoing" or "completed"
   - `categories`: Array of category IDs
   - `gradient`: Tailwind gradient classes
   - `jobScope`: Array of job scope items
   - `manpower`: Array of manpower roles

### Available Gradients

- `from-jbs-purple to-jbs-blue`
- `from-jbs-blue to-jbs-magenta`
- `from-jbs-magenta to-jbs-purple`

### Available Categories

- `sdm`: SDM Projects
- `maintenance`: Daily Maintenance
- `construction`: Construction
- `ongoing`: Ongoing Projects

### Example Project

```json
{
  "id": "new-project",
  "title": "New Project Name",
  "client": "Client Company Pte Ltd",
  "period": "Jan-Dec 2025",
  "status": "ongoing",
  "categories": ["construction", "ongoing"],
  "gradient": "from-jbs-purple to-jbs-blue",
  "jobScope": [
    "Install and assemble pipes, valves, and equipment",
    "Perform welding works with safety protocols",
    "Clean tanks and vessels",
    "Ensure equipment integrity"
  ],
  "manpower": ["Mechanical Fitters", "Technicians", "Supervisors"]
}
```

### Removing a Project

Simply delete the project object from the `projects` array in the JSON file.

### Modifying a Project

Edit any field in the project object. The changes will be reflected on the website immediately after saving the JSON file.

## Benefits

- **Easy Management**: No need to edit HTML code
- **Consistent Structure**: All projects follow the same format
- **Dynamic Loading**: Projects load automatically from JSON
- **Filter Support**: Categories are automatically generated
- **Maintainable**: Clear separation of data and presentation 