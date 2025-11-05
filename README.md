# Driver Documentation Contribution Guide

This guide explains how to add new driver documentation, including details on file structure, image placement, and how custom CSS ensures consistent styling. This project aims to provide a comprehensive and easily navigable resource for various drivers.

## 1. Adding New Drivers

Each driver entry consists of two files: a Markdown (`.md`) file for the main content and a YAML (`.yaml`) file for metadata, particularly the manufacturer information.

### File Structure

All driver documentation should reside within `src/content/docs/drivers/`.
Organize drivers by category:

```
src/content/docs/drivers/
├── Mounts/
│   ├── EQMod.md
│   └── EQMod.yaml
├── Cameras/
│   ├── ZWO.md
│   └── ZWO.yaml
└── ...
```

*   **Category Directory**: Create a directory for the driver's category (e.g., `Mounts`, `Cameras`).
*   **Driver Files**: Inside the category directory, create two files for each driver:
    *   `<DriverName>.md`: Contains the main documentation content.
    *   `<DriverName>.yaml`: Contains additional metadata, primarily the manufacturer.

### Markdown (`.md`) File Example

The Markdown file should include frontmatter with `title`, `category`, `description` and `thumbnail` (optional).

```markdown
---
title: EQMod
category: Mounts
description: The EQMod description.
thumbnail: /images/drivers/Mounts/EQMod.png
---

# EQMod Driver

This is the documentation for the EQMod driver. It provides details on installation, configuration, and usage.

## Installation

Follow these steps to install EQMod...

## Usage

Here's how to use the EQMod driver with your mount...
```

*   **`title`**: The name of the driver.
*   **`category`**: The category this driver belongs to (e.g., `Mounts`, `Cameras`). This should match the directory name.
*   **`thumbnail`**: (Optional) The path to the driver's thumbnail image. If not provided, a default path will be used.

### YAML (`.yaml`) File Example

The YAML file should contain the `manufacturer` field. This is crucial for organizing drivers by manufacturer.

```yaml
manufacturer: Sky Watcher
```

*   **`manufacturer`**: The name of the manufacturer for this driver. This will be used to group drivers on manufacturer-specific pages.

## 2. Image Guidelines

To maintain a consistent look and feel across the documentation, please adhere to the following image guidelines. Custom CSS is applied to ensure all images are scaled correctly.

### Driver Thumbnails

*   **Path**: `/public/images/drivers/<Category>/<DriverTitle>.webp`
    *   Example: `/public/images/drivers/Mounts/EQMod.webp`
*   **Format**: Must be `.webp`.
*   **Recommended Size**: 200x200 pixels
*   **Styling**: Images are styled with `width: 200px; height: 200px; object-fit: contain;`. This means images will be scaled down or up to fit within these dimensions while maintaining their aspect ratio.

### Manufacturer Logos

*   **Path**: `/public/images/manufacturers/<ManufacturerName>.webp`
    *   Example: `/public/images/manufacturers/Sky Watcher.webp`
*   **Format**: Must be `.webp`.
*   **Recommended Size**: 200x200 pixels
*   **Styling**: Images are styled with `width: 200px; height: 200px; object-fit: contain;`.

## 3. Markdown Features

This project supports GitHub-flavored Markdown, including special callout blocks for highlighting important information. These callouts are rendered with custom styling to draw attention to specific content.

### Callout Blocks

You can use various types of callout blocks to emphasize different kinds of information:

*   **Note**: For general information or tips.
    ```markdown
    > [!NOTE]
    > This is a note.
    ```
*   **Tip**: For helpful advice.
    ```markdown
    > [!TIP]
    > This is a tip.
    ```
*   **Important**: For crucial information.
    ```markdown
    > [!IMPORTANT]
    > This is important information.
    ```
*   **Warning**: For potential issues or cautions.
    ```markdown
    > [!WARNING]
    > This is a warning.
    ```
*   **Caution**: For serious warnings or critical information.
    ```markdown
    > [!CAUTION]
    > This is a caution.
    ```

These callouts help improve the readability and clarity of the documentation by visually separating important sections.

## Contribution

We welcome contributions from the community! If you have new driver documentation to add, or improvements to existing ones, please follow this guide. Your contributions help make this resource more valuable for everyone.
