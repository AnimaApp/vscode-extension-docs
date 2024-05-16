# FAQ

Frequently Asked Questions About Frontier by anima

1. What if the code component was updated?
   A: Frontier continuously synchronizes with your code and design files to stay updated. It automatically scans your codebase every time you open VS Code. Additionally, you can trigger a manual scan anytime using the command `Anima: Analyse codebase`.

2. Can Frontier detect libraries like MUI and AntD?
   A: Yes, Frontier can detect and seamlessly integrate with popular libraries such as MUI, AntD, and others if they are already part of your existing project. For projects that do not yet include these libraries, or to enhance detection in a new project, follow these steps:

3. Open the Library Project: Start by opening the project that contains the UI library (e.g., MUI, AntD) whose components you wish to use in VSCode.
4. Run the Anima Command: Execute `Anima: Export components Library Data` within the library project. This command scans the library and generates detailed component data, storing this information in a `.anima` folder created within the library project.
5. Copy the .anima Folder: After the `library.json` file is generated, copy the `.anima` folder from the library project to the root directory of the project where you intend to use these components.
6. Enable Anima Matching: Placing the `.anima` folder in your current project allows Anima to access the component data of the UI library. This setup lets Anima match these external library components to Figma designs, even if they are not originally part of your project’s codebase.

Note: Ensure that a `.anima` folder exists in your project directory or create one if necessary. This folder is essential for Anima to store and retrieve the component data needed for accurate matching.

By following these steps, you enable Anima to recognize and utilize components from external libraries effectively, enhancing the breadth of component matching and code generation capabilities in your projects.

3. What if the design was updated?
   A: If your Figma design undergoes changes, simply refresh the Figma URL scan using the refresh button in Frontier’s interface to update the component matches and suggestions.

4. Do we need to manually connect the code and design components?
   A: No, Frontier automatically handles the matching of design components to code components. While this process is automated to save you time, you have the option to manually override these matches if you prefer specific adjustments.

5. How can Frontier help me write code?
   A: Frontier speeds up your coding process by automatically generating code from Figma designs that integrate with your existing codebase. It provides structure suggestions, component matches, and implementation guidelines that adhere to your project’s coding conventions.

6. Does Frontier provide best practices in code? How do we ensure quality code generation?
   A: Frontier is designed to follow the coding practices and conventions found in your current codebase, ensuring that generated code not only fits seamlessly into your project but also upholds the standards you expect. This focus on adopting your project's specific coding styles helps maintain high code quality and consistency.

7. Can I use my custom `tailwind.config` file?
   A: Yes, you can incorporate your custom Tailwind configuration with Anima. When selecting Tailwind as your styling preference in the Conventions settings, you will find an input field to provide your existing `tailwind.config` file. Once specified, Anima will generate code that adheres to your existing Tailwind configurations, ensuring that the styling remains consistent with your project's design principles.
