# Creating new components with Frontier

When a necessary component is not available in your codebase, Frontier allows you to create a new one directly from your Figma design. This feature is particularly useful for implementing unique design elements that do not yet have corresponding code implementations in your project.

How to Create a New Component:

1. Initiate New Component Creation:
   - Navigate to the component matching interface and click on the “Generate a new Component” button to start the creation process.
2. Name Your Component:
   - Enter a name for your new component in the “Name” field. This name will be used for the component file and as the display name in your code.
3. Set the Component Path:
   - Specify the path where you want the new component files to be saved within your project structure. Typically, this would be within a directory like `src/components/`.
4. Download Assets (Optional):
   - Check the “Download assets” option if you want Frontier to automatically download and include any relevant assets (e.g., SVG, PNG) associated with the Figma component. This is useful for ensuring that all visual elements of the component are retained.
5. Generate the Component:
   - Click the “Generate” button. Frontier will create the necessary files for the component (e.g., `ComponentName.tsx`, `ComponentName.scss`) at the specified path, and include any chosen assets.
6. Code Integration:
   - Upon creation, Frontier automatically updates the code suggestions in your project to include an import statement for the new component, ensuring that it can be easily integrated and used in your project.
