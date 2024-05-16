# Translate Figma Into Code

This section explains how Frontier utilizes existing code components from your project to generate code from Figma designs, enhancing development efficiency and ensuring consistency.

![](https://paper-attachments.dropboxusercontent.com/s_B22C287C6DA46EF27384CB49410B86378245D06B44B59D6052E7432F3F69E19F_1714640452960_Screen+Shot+2024-05-02+at+12.00.45.png)

## How It Works

When you provide Frontier with a Figma design, such as a signup form, Frontier doesn't start from scratch. Instead, it analyzes the design to determine which parts of the interface can be constructed using components that already exist in your codebase.

## Component Reuse Process

- Scan and Identify: Frontier scans the provided Figma design and identifies common UI elements like buttons, input fields, labels, and other reusable components
- Match with Existing Components: It then matches these design components with the corresponding code components from your project (for more info - +5. Component matching).
- Generate Implementation Suggestion: Rather than generating new code, Frontier assembles a suggested implementation using these pre-existing components. This includes setting up props, and any necessary wrappers to ensure the components fit within the context of the new design.
  ![](https://paper-attachments.dropboxusercontent.com/s_B22C287C6DA46EF27384CB49410B86378245D06B44B59D6052E7432F3F69E19F_1714663907323_Screen+Shot+2024-05-02+at+18.31.43.png)

---

## Benefits of Component Reuse

- Efficiency: Reduces the time needed to implement designs by using pre-built components.
- Consistency: Ensures uniformity across your application by reusing components.
- Maintainability: Enhances code maintainability by reducing redundancy and leveraging established coding standards.

## Practical Example

Scenario: Generating a signup form from a Figma design, that has design elements like inputs, buttons, and tags.

- Action: Frontier identifies these elements and matches them to `<Input>`, `<Button>` and <Tag> components from your existing codebase.
- Result: Frontier suggests an implementation that integrates these components, setting properties and layouts according to the design.

By effectively reusing components, Frontier facilitates faster development cycles, ensures consistency across interfaces, and optimizes the overall code quality. This process underscores Frontier’s capability to not just translate designs into code but to integrate intelligently within existing development frameworks.

![](https://paper-attachments.dropboxusercontent.com/s_B22C287C6DA46EF27384CB49410B86378245D06B44B59D6052E7432F3F69E19F_1714663937308_Screen+Shot+2024-05-02+at+18.32.13.png)
