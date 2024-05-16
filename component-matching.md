# Component Matching

Frontier's advanced component matching feature leverages intelligent algorithms to automatically identifying correspondences between your Figma designs and existing code components. This capability enhances efficiency and maintains consistency across your projects.

## How It Works

Frontier integrates your design and development environments by first scanning your project's code components when you open the extension and then matching these with your Figma designs

Getting Started with Component Matching

1. Open Frontier

- Initial Scan: As soon as you activate Frontier within VS Code, it scans your existing codebase to identify and catalog all available code components. This comprehensive scan ensures that Frontier is ready to match these components with your Figma designs accurately.

2. Provide a Link to Your Figma File
   To start the matching process, link your Figma design to Frontier:

- From the Left Panel: - Copy Link: Use `CMD + L` (Mac) or `CTRL + L` (Windows/Linux) on Figma to copy the link to your intended design.

  ![](https://paper-attachments.dropboxusercontent.com/s_A2EF4E71D8F89E0684E0A369FAC02F6CAA336672DC39C68D17CCD02808897CF0_1714663725416_Screen+Shot+2024-05-02+at+18.28.41.png)

- Paste Link: Navigate to the “Provide a Figma URL” section in the extension, paste the link, and click “View Code” to load your design.

- From the Right Panel: - Paste Link: After copying your Figma design link, paste it into the “Generated file” input field at the top of the panel.

  ![](https://paper-attachments.dropboxusercontent.com/s_A2EF4E71D8F89E0684E0A369FAC02F6CAA336672DC39C68D17CCD02808897CF0_1714663741672_Screen+Shot+2024-05-02+at+18.28.57.png)

3. Automatic Component Detection and Matching
   Once the Figma link is provided, Frontier begins its analysis:

- Design Scan: Identifying all the design components in the given Figma file.
- Matching Process: Matching these Figma components to the most appropriate existing code components cataloged during the initial scan.

  ![](https://paper-attachments.dropboxusercontent.com/s_A2EF4E71D8F89E0684E0A369FAC02F6CAA336672DC39C68D17CCD02808897CF0_1714663705010_Screen+Shot+2024-05-02+at+18.28.22.png)

4. Review Best Match Proposals

- Optimal Property Suggestions: For each matched component, Frontier suggests the best properties that align with the Figma design, ensuring functional and fidelity.

5. Override Option: If Frontier’s automatic suggestions don’t align with your needs, you can manually override the matches to select a different component. - How to Override: Access the override options in the right panel by selecting a component and choosing a different match or modifying properties.

   ![](https://paper-attachments.dropboxusercontent.com/s_A2EF4E71D8F89E0684E0A369FAC02F6CAA336672DC39C68D17CCD02808897CF0_1714921767998_Screen+Shot+2024-05-05+at+18.09.24.png)

---

Benefits of Component Matching

- Efficiency: Significantly reduces the time required to convert designs into code by leveraging existing components.
- Consistency: Ensures your UI components are consistent across different parts of your application by using a unified component library.

Component matching by Frontier effectively bridges the gap between design and development, automating routine coding tasks and allowing developers to focus on more complex aspects of application development.
