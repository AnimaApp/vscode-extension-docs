# Preferences Settings

Accessing the Settings Menu

To customize how Frontier functions within your project, open the extension sidebar in VS Code and navigate to the `Preferences` section in the left panel. This area allows you to configure settings that tailor Frontier’s behavior to your project's specific requirements.

Sections within Preferences
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
    import Tooltip from './components/Tooltip';
    import Button from './components/Button';
    <Tooltip content="Click to submit your response" placement="top">
      <Button variant="primary" size="medium">
        Submit
      </Button>
    </Tooltip>
    
        - How Anima Applies This Pattern: Anima automatically generates a React component snippet that includes the `Button` wrapped in a `Tooltip`. This not only saves development time but also ensures that new UI elements are consistent with established user interface guidelines in your application.
    - Benefits:
        - Consistency: Ensure consistently across your application, maintaining a uniform user experience and development patterns. 
        - Efficiency: Quickly integrate Figma designs into code without having to manually replicate common patterns each time.
    - Note: This feature is considered experimental and might evolve based on user feedback and further development. While it aims to produce optimal results, outcomes may vary depending on the complexity and uniqueness of your project's codebase.

![](https://paper-attachments.dropboxusercontent.com/s_148F35C30B5AA5DBD3CF7F0BE129E64A727EF2862A4331D40B1BE7C9175F6C16_1714664571567_Screen+Shot+2024-05-02+at+18.42.47.png)

Applying Changes
Modifications to settings take immediate effect. Review and confirm your preferences to ensure that Anima behaves as expected within your development environment.
