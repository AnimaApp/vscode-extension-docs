# Preferences Settings

## Accessing the Settings Menu

To customize how Frontier functions within your project, open the extension sidebar in VS Code and navigate to the `Preferences` section in the left panel. This area allows you to configure settings that tailor Frontier’s behavior to your project's specific requirements.

## Sections within Preferences

The Preferences menu is divided into two sections:

1. Conventions
2. Enrichments

   ![](https://paper-attachments.dropboxusercontent.com/s_148F35C30B5AA5DBD3CF7F0BE129E64A727EF2862A4331D40B1BE7C9175F6C16_1714664531765_Screen+Shot+2024-05-02+at+18.42.09.png)

3. Conventions
   The Conventions section is automatically configured by Frontier based on an initial scan of your project, ensuring the generated code aligns with your existing frameworks, languages, and styling methods. Although preset by Frontier, you can customize these settings as needed.

![](https://paper-attachments.dropboxusercontent.com/s_148F35C30B5AA5DBD3CF7F0BE129E64A727EF2862A4331D40B1BE7C9175F6C16_1714664541842_Screen+Shot+2024-05-02+at+18.42.17.png)

2. Enrichments
   This section provides additional enhancements to the code generation capabilities. By toggling these features on or off, you can tailor how Anima interacts with your project's Figma designs and existing codebase. Here’s a breakdown of each feature:

- Components Reuse:
  - Description: This feature enables the reuse of existing code components within your project. When enabled, Anima scans your project’s code to find components that can be reused instead of creating new ones. This approach reduces redundancy and leverages your established coding efforts.
  - Example: Imagine you are developing a new feature that includes a user profile page, and you have a Figma design that includes user avatars, names, and contact information. If your codebase already contains a `UserProfile` component used elsewhere, Anima will identify this component and suggest reusing it within the new page. This reuse includes not just the component itself but also adapting its properties to fit the new context as defined by the design.
  - Benefits:
    - Efficiency: Decreases development time by reusing pre-existing components.
    - Consistency: Maintains a uniform look and feel across your application by reusing components.
    - Optimization: Reduces the overall size of your codebase by avoiding unnecessary duplication of code.
- Smart Code Scaffolding:
  - Description: This feature is designed to transform complex and unstructured Figma designs into clean, developer-friendly code. In Figma, designs often lack the hierarchical structure needed for efficient coding, with elements grouped in ways that serve visual presentation rather than functional separation. This feature intelligently reorganizes these designs into logical code structures.
  - Example: a Figma design might represent a webpage as a single section containing various elements like headers, carousels, and footers. While this may visually suffice, it can lead to bloated and hard-to-maintain code. Smart Code Scaffolding analyzes these designs and breaks them down into distinct components (such as `Header`, `Body`, `CarouselSection`, `Testimonials`, `Footer`), each encapsulated in its own module. This not only improves readability and maintainability but also aligns the code structure with common React development practices.
  - Benefits: This scaffolding ensures that the generated code is:
    - Modular: Each section of the design is translated into a separate, reusable component.
    - Readable: Reduces complexity by structurally organizing code according to logical divisions in the design.
  - Note: This feature is experimental and is continuously being improved. Results may vary based on the complexity of the design and the specificity of the coding standards in use.
- Usage Examples:
  - Description: This feature leverages common usage patterns detected within your project, to ensure the generated code not only matches the functional requirements of your Figma designs but also aligns with the established conventions of your existing codebase.
  - Example: In your project, buttons are often accompanied by tooltips to provide additional information to users. This common pattern has been identified by Anima through its usage analysis of your codebase. - Example of a common pattern identified in your project:
    ```
    import Tooltip from './components/Tooltip';
    import Button from './components/Button';
    <Tooltip content="Click to submit your response" placement="top">
      <Button variant="primary" size="medium">
        Submit
      </Button>
    </Tooltip>
    ```
        - How Anima Applies This Pattern: Anima automatically generates a React component snippet that includes the `Button` wrapped in a `Tooltip`. This not only saves development time but also ensures that new UI elements are consistent with established user interface guidelines in your application.
    - Benefits:
      - Consistency: Ensure consistently across your application, maintaining a uniform user experience and development patterns.
      - Efficiency: Quickly integrate Figma designs into code without having to manually replicate common patterns each time.
    - Note: This feature is considered experimental and might evolve based on user feedback and further development. While it aims to produce optimal results, outcomes may vary depending on the complexity and uniqueness of your project's codebase.

![](https://paper-attachments.dropboxusercontent.com/s_148F35C30B5AA5DBD3CF7F0BE129E64A727EF2862A4331D40B1BE7C9175F6C16_1714664571567_Screen+Shot+2024-05-02+at+18.42.47.png)

- Local components:
  - Description: This is used when you have local components in your project (i.e., components that are technically defined in the repo itself), which are UX components.
  - When to turn on? When you have local components that you would like to incorporate within the Figma implementation, turn this feature on.
  - When to turn off? If you are primarily using an external design system package, and you do not want to "pollute" your component library with irrelevant local componets.
- External components:

  - Description: This is used when you have external components in your projects that you want to incorporate into the figma design.
  - When to turn on? When your external packages are used as UX components that you would like to incorporate within your Figma implementation.
  - When to turn off? If the primary use of your project is to use local components (This includes "wrapped" external components), turn this off.

- Deep component detection:
  - Description: This means that when scanning, we not only rely on component usages, but actually parse every component to try and identify all of its props and variants.
  - When to turn on? When your component library contains components that haven't been used yet, but you are still interested in integrating them into the Frontier results.
  - When to turn off? If you have a lot of components, this might increase the number even further. Additionally, it may find irrelevant components that you have in your local or external components that you are interested in utilizing in your Figma design implementation. Finally, Deep component detection is resource intensive and may take too long or slow down your VScode while it's running.
  
    ***Note: before turning on Deep component detection, make sure that the relevant libraries are marked as depdendencies in your package.json and you have run "npm install" or "yarn install" recently***

### How do you reduce the amount of components to a more "reasonable" amount?

A large project could have thousands of components. In most cases, these components are irrelvant to the Figma placement, but they do slow down your system when we process them and match them. Other than turning off either local or external components, you have the option to fine tune which components you want to include or exclude.

- Local component filtering by paths (and glob patterns). In `enrichments.json`, you have the key `include`:

  ```json
  "include": [
    "src/**/*",
    "!public"
  ]
  ```

  This means that when scanning for components, we only search for usage patterns and components themselves in the included subdirectories. In this example, we'll search for components and component usages under the `src/` subdirectories, and exclude the `public` directory.

- External component filtering by package names. In enrichments.json, you have the key `packages`:
  ```json
  "packages": [
    "recharts",
    "!@mui/core"
  ]
  ```
  This means that when scanning for external components we include `recharts`, but ignore `mui`.

## Applying Changes

Modifications to settings take immediate effect. Review and confirm your preferences to ensure that Anima behaves as expected within your development environment.
