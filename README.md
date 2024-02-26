# FusionLab-Ifc-Web-Viewer

1) 3D Web-based Model Viewer


Additional Packages Used for Ifc Web Viewer:


•	Three.js: A JavaScript library used for 3D rendering within the web browser.


•	Web-ifc: A JavaScript library for viewing and interacting with Industry Foundation Classes (IFC) files in web applications.


•	Vite: A build tool that provides a fast development server with hot module replacement (HMR) capability, enabling rapid development and efficient module bundling for production deployment.


•	OpenBIM-components: A collection of components and utilities for working with Building Information Modeling (BIM) data in web applications. 


![image](https://github.com/denizcandemirli/FusionLab-Ifc-Web-Viewer/assets/159064259/5a388d07-7911-49fd-a787-cfdde0fbe6f4)
![image](https://github.com/denizcandemirli/FusionLab-Ifc-Web-Viewer/assets/159064259/8750e92d-eb12-4092-8c84-6eec329e80f9)
Package.json Dependencies -  Project Folder

----------------------------------------------------------


These additional packages increases the functionality and development experience of the web application by providing special tools for working with BIM data, automating server restarts during development, and optimizing the build process for production deployment.


![image](https://github.com/denizcandemirli/FusionLab-Ifc-Web-Viewer/assets/159064259/5be48d53-29e1-499a-a9ef-df4ff947fc16)
Diagram of web application

![image](https://github.com/denizcandemirli/FusionLab-Ifc-Web-Viewer/assets/159064259/c89810e0-0f18-490e-8ca7-cc961fe201f3)
Home page of Ifc Web Viewer


----------------------------------------------------------


Implementation of the viewer


•	Canvas Setup: 


o	The HTML file contains a <div> element with the ID "ifcCanvas" where the 3D model viewer will be rendered. 
![image](https://github.com/denizcandemirli/FusionLab-Ifc-Web-Viewer/assets/159064259/e18157b9-712a-4549-a3ab-18d1ea1efa59)
Canvas Setup in HTML Page

•	JavaScript (index.js) Initialization: 

o	The JavaScript file imports necessary libraries such as Three.js and openbim-components for the Ifc Web Viewer.

o	 It initializes the components needed for the viewer, including scene, renderer, camera, and raycaster.

o	The init() method starts updating all components at 60 frames per second. 

o	The camera is positioned to look at a specific point in the scene. A grid is added to the scene for reference. 



![image](https://github.com/denizcandemirli/FusionLab-Ifc-Web-Viewer/assets/159064259/be9cbac3-2f24-41c7-aebd-a0e583f758d5)
Index.js of ifc web viewer

•	Toolbar Setup: 

o	A toolbar is created at the bottom of the viewer interface using openbim-components.

o	A button for loading an IFC model is added to the toolbar. 

o	Settings for the IFC loader, such as the path to the wasm file and optimization options, are configured.


•	Loading an IFC Model:


o	The loadIfcAsFragments() function fetches the IFC file and loads it into the viewer as fragments.


o	The loaded model is added to the scene. 

![image](https://github.com/denizcandemirli/FusionLab-Ifc-Web-Viewer/assets/159064259/bc294a7b-c518-450b-bc03-ae2e1babdae7)
Ifc Loading function

•	Exporting Fragments: 


o	An export button is added to the toolbar to export the loaded model as fragments.


o	The ‘exportFragments()’ function exports the fragments and saves them as a downloadable file.

•	Cleaning Memory:


o	A button is added to the toolbar to dispose of the loaded fragments from memory when no longer needed.

o	The ‘disposeFragments()’ function disposes of the fragments.


•	Download Function:


o	A utility function ‘download()’ is defined to facilitate file downloads.

![image](https://github.com/denizcandemirli/FusionLab-Ifc-Web-Viewer/assets/159064259/d842a6df-c240-4827-b2ca-107eed49c83b)

![image](https://github.com/denizcandemirli/FusionLab-Ifc-Web-Viewer/assets/159064259/fa72008c-5ff0-41d0-a936-92f0e951fe48)


Ifc Web Viewer in Web Application


#Conclusion


This implementation provides basic functionality for loading, viewing, exporting, and disposing of 3D models in the web-based viewer. Users can interact with the viewer through the provided toolbar controls. The viewer allows for the loading of IFC models, exporting fragments, and cleaning up memory.
To improve the functionality and user experience, additional features such as model swapping, camera controls, and interactive annotations could be implemented in future iterations of the viewer.

Limitations:


•	Express.js cannot be used with ifc web viewer components due to incompatibility issues. As a result, in the "Ifc Web Viewer" architecture, Vite is utilized for web-based deployment instead of Express.js.


•	The limitations of integrating Express.js with ifc web viewer components were communicated to the framework providers, and an error report was created in their GitHub section for further investigation and potential resolution.


![image](https://github.com/denizcandemirli/FusionLab-Ifc-Web-Viewer/assets/159064259/dfc166a8-5330-4686-9601-298142ddd5f5)

Error report on Framework provider’s GitHub Page


1.2)Summary of Achievements:


Throughout the implementation phase of our project, we have achieved significant milestones in the development of our web application and the integration of the IFC web viewer. 

These achievements include:

•	Successful Web Application Development: We have built a fully functional web application using Node.js and Express.js, providing a platform for users to access project information, participate digitally, and interact with BIM data.

•	Integration of IFC Web Viewer: We have successfully integrated an IFC web viewer into our application, enabling users to visualize 3D BIM models for further developments, directly within their web browsers.

•	Implementation of Viewer Controls: User controls within the IFC web viewer, such as loading, exporting, and disposing of 3D models, have been implemented. 

1.3)Further Developments:


•	Integration of React.js: Transitioning from traditional HTML-based rendering to a React.js-based frontend framework can significantly effects the modularity, performance, and maintainability of our web application.


•	Implementing Location-Based Commenting: Enhancing the IFC web viewer with location-based commenting functionality can provide users with the ability to annotate specific areas of the 3D model and collaborate effectively on design reviews and project discussions. 


•	Optimization with MongoDB: Leveraging MongoDB as our backend database solution can provide scalability, flexibility, and performance for data storage and management.





