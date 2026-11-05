Banking Mobile User Interface Dataset (BMUID)
The Banking Mobile User Interface Dataset (BMUID) is a domain-specific multimodal dataset designed to support research in mobile user interface understanding, visual interface analysis, semantic interpretation, user-intent recognition, navigation prediction, and adaptive interface personalization. Unlike general-purpose mobile user interface datasets, BMUID focuses specifically on banking application interfaces and represents diverse digital banking operations, including user authentication, account management, fund transfers, bill payments, mobile recharges, card management, loan services, investments, and customer support.
The dataset is intended to provide a comprehensive representation of banking mobile interfaces through visual screenshots, textual information, UI component structures, spatial arrangements, semantic labels, and navigation relationships. Each interface screen can be analyzed based on its visual appearance, functional elements, textual content, and associated banking operation. These characteristics support multimodal learning approaches that integrate computer vision, natural language processing, spatial understanding, and intelligent decision-making.
The BMUID-10K dataset is described as comprising approximately 10,000 annotated banking interface screens, covering diverse interface designs, layouts, components, and functional categories. It provides a research foundation for developing intelligent mobile applications capable of understanding interface structures, recognizing user objectives, predicting navigation sequences, and generating adaptive user interface recommendations.

Dataset Characteristic	Description
Dataset Name	Banking Mobile User Interface Dataset
Abbreviation	BMUID
Dataset Version	BMUID-10K
Domain	Mobile Banking Applications
Data Type	Multimodal UI Data
Primary Data	Mobile UI Screenshots
Visual Information	Interface layouts, icons, buttons, cards, and images
Textual Information	OCR-extracted interface text
Structural Information	UI components and spatial coordinates
Semantic Information	Screen categories and functional descriptions
Intent Information	Banking-related user objectives
Navigation Information	Screen transitions and workflow relationships
Research Applications	UI understanding, classification, prediction, and personalization
The dataset can be represented using multiple information categories that collectively describe the characteristics of each banking interface.
Data Type	Description	Research Purpose
UI Screenshot	Original banking application screen image	Visual feature extraction
OCR Text	Text extracted from the interface	Textual semantic understanding
Bounding Boxes	Coordinates of individual UI elements	Spatial understanding
Component Labels	Buttons, icons, cards, and input fields	UI component recognition
Screen Category	Functional classification of the interface	Screen classification
User Intent	Expected objective of the user	Intent recognition
Previous Screen	Interface visited before the current screen	Navigation context
Next Screen	Expected subsequent interface	Screen prediction
Navigation Path	Sequence of screens associated with a task	Workflow analysis
Task Label	Banking operation being performed	Task identification
Context Metadata	Relevant interaction and task information	Context-aware analysis
Layout Variant	Alternative arrangements of interface elements	Adaptive UI research
These information categories enable researchers to investigate relationships between visual interface structures, textual semantics, functional components, and navigation behaviour.
Banking Screen Categories
BMUID can be organized into 20 major banking interface categories to support systematic classification and functional analysis.
Class ID	Banking Screen Class	Example Content
SC01	Login	Username, password, biometric login
SC02	OTP Verification	OTP entry and verification
SC03	Dashboard	Account overview and shortcuts
SC04	Account Summary	Account balance and details
SC05	Transaction History	Previous transactions
SC06	Fund Transfer	Money transfer options
SC07	Beneficiary Management	Add and manage beneficiaries
SC08	Amount Entry	Transfer amount input
SC09	Transaction Confirmation	Transaction review and confirmation
SC10	Bill Payment	Electricity, water, and utility payments
SC11	Mobile Recharge	Mobile recharge services
SC12	QR Payment	QR scanning and payment
SC13	Card Management	Debit and credit card controls
SC14	Loan Services	Loan information and applications
SC15	Investment Services	Deposits and investment options
SC16	Notifications	Banking alerts and notifications
SC17	Customer Support	Chat and customer assistance
SC18	Profile	Personal account preferences
SC19	Security Settings	PIN and security controls
SC20	General Settings	Application preferences
The classification structure covers major banking operations and provides a basis for evaluating automated screen recognition and functional interface understanding.
UI Component Annotation Classes
The UI component annotation structure identifies individual visual elements and their corresponding functional roles within banking application interfaces.
Component ID	UI Component	Description
C01	Button	Interactive action button
C02	Text	Labels, headings, and descriptions
C03	Icon	Graphical interface symbol
C04	Image	Illustrations and visual content
C05	Input Field	Text, number, and password entry
C06	Card	Grouped banking information
C07	Navigation Bar	Primary and bottom navigation
C08	Menu	Navigation and action menu
C09	List	Transaction and account entries
C10	Checkbox	Selection control
C11	Radio Button	Single-choice selection
C12	Toggle Switch	Enable or disable settings
C13	Dropdown	Expandable selection control
C14	QR Code/Scanner Region	QR-based payment interface
C15	Dialog/Popup	Modal messages and confirmations
Each identified component can be represented using a bounding-box coordinate structure:
\[ B_i=(x_min,y_min,x_max,y_max ) \]
where \(x_min \) and \(y_min \)dicate the top-left coordinates, while \(x_max \) and \(y_max \)present the bottom-right coordinates of the identified interface element.
Component-level annotations support object detection, spatial relationship analysis, interface segmentation, and functional element recognition.
User Intent Classification
User-intent classification identifies the probable objective associated with a banking interface. BMUID can support the following 15 major intent categories.
Intent ID	User Intent	Example Objective
INT01	Login to Account	Access a banking account
INT02	Check Account Balance	View available balance
INT03	View Transactions	Examine transaction history
INT04	Transfer Money	Transfer funds
INT05	Add Beneficiary	Register a beneficiary
INT06	Pay Bill	Pay utility bills
INT07	Recharge Mobile	Recharge a mobile number
INT08	Make QR Payment	Complete QR-based payment
INT09	Manage Cards	Block, activate, or control cards
INT10	Apply for Loan	Explore or apply for loans
INT11	View Investments	Examine investment products
INT12	Contact Support	Obtain banking assistance
INT13	Update Profile	Modify profile information
INT14	Change Security Settings	Update security preferences
INT15	Logout	Exit the banking application
These intent categories enable researchers to investigate the relationship between interface characteristics and the functional objectives of users.
Dataset Sample Distribution
For experimental organization, the BMUID-10K dataset can be structured into the following functional groups.

Category Group	Number of Samples	Percentage
Authentication Interfaces	800	8%
Dashboard and Account Management	1,500	15%
Fund Transfer Interfaces	1,800	18%
Payment and Recharge Interfaces	1,500	15%
Card Management	800	8%
Loans and Investments	1,000	10%
Transaction and Notification Interfaces	900	9%
Profile and Security	900	9%
Customer Support and Settings	800	8%
Total	10,000	100%
This distribution provides greater representation to fund transfer, account management, and payment interfaces because these operations generally involve multiple interaction stages. Class imbalance should be examined before model training. Researchers can apply stratified sampling, class-weighted loss functions, and suitable augmentation techniques to improve learning performance.
Training, Validation, and Testing Split
For machine learning and deep learning experiments, a recommended division of the BMUID-10K dataset is presented below.
Dataset Partition	Percentage	Number of Screens
Training	70%	7,000
Validation	15%	1,500
Testing	15%	1,500
Total	100%	10,000

The training subset is used to learn visual, textual, and semantic representations. The validation subset supports hyperparameter optimization and model selection, whereas the testing subset is used for independent performance evaluation. For navigation prediction and interface personalization experiments, partitioning should preferably be performed at the application, interface-template, or workflow-family level. This reduces data leakage caused by highly similar screenshots appearing across different subsets.
Dataset Collection and Annotation Methodology
The preparation and annotation of banking interface data can be organized into the following stages.
Step 1: Banking UI Collection
Collect banking application screenshots representing authentication, account management, money transfers, bill payments, transactions, and other banking operations. Data should originate from authorized, licensed, or appropriately generated resources.
Step 2: Image Preprocessing
Standardize screenshot dimensions, image formats, and resolution while preserving interface layouts and textual readability.
Step 3: OCR-Based Text Extraction
Apply Optical Character Recognition (OCR) to extract headings, labels, descriptions, button captions, navigation text, and other visible interface information.
Step 4: UI Component Identification
Identify individual interface elements, including buttons, icons, cards, menus, input fields, and navigation bars. Assign component labels and corresponding bounding-box coordinates.
Step 5: Semantic Annotation
Assign screen categories, functional descriptions, and user-intent labels according to the visual and textual characteristics of each interface.
Step 6: Navigation Relationship Identification
Establish relationships between consecutive screens based on their corresponding banking workflows.
Step 7: Contextual and Layout Annotation
Associate relevant task context, component positions, layout variations, and interface characteristics to support adaptive interface research.
Step 8: Dataset Quality Verification
Verify screenshot quality, OCR accuracy, component annotations, category assignments, intent labels, and navigation consistency. Remove duplicate and incorrectly annotated samples.
10. Research Applications of BMUID
The BMUID dataset can support several research directions in intelligent mobile interface analysis.
Research Area	Description
UI Component Recognition	Automatic identification of interface elements
Mobile Screen Classification	Classification of banking screens
Semantic UI Understanding	Interpretation of interface meaning and functionality
User Intent Prediction	Recognition of probable user objectives
Next-Screen Prediction	Prediction of subsequent interface screens
Navigation Flow Analysis	Understanding multi-stage banking workflows
UI Layout Understanding	Analysis of component positions and relationships
Adaptive UI Personalization	Generation of context-aware interface arrangements
Multimodal Learning	Integration of visual, textual, and spatial information
Intelligent Interface Automation	Understanding and automating interface-related tasks

The major advantages of BMUID include:
	Domain-Specific Representation: Focuses on mobile banking interfaces and their functional characteristics.
	Multimodal Information: Supports the integration of visual, textual, spatial, and semantic information.
	Functional Diversity: Covers multiple banking operations and interface categories.
	Semantic Understanding: Provides a foundation for understanding the meaning and functionality of UI components.
	Intent Recognition: Supports research into identifying user objectives from interface information.
	Navigation Analysis: Enables the investigation of screen transitions and banking workflows.
	Adaptive Interface Research: Supports the development of context-aware and personalized interface systems.
	Deep Learning Applications: Can be investigated using computer vision, NLP, multimodal transformers, and other machine learning architectures.
Dataset Limitations and Research Considerations
For reliable and reproducible research, the following considerations should be addressed:
	Annotation Availability: Verify whether OCR text, bounding boxes, component labels, and intent annotations are available for each sample.
	Sample Verification: Confirm the actual number of unique screenshots before reporting the final dataset size.
	Class Distribution: Calculate the actual number of samples belonging to each screen category.
	Navigation Ground Truth: Validate previous-screen and next-screen relationships against actual workflows.
	Data Privacy: Remove personal names, account numbers, financial details, and other sensitive information.
	Generalization: Evaluate performance across different interface templates and application designs.
	Reproducibility: Document preprocessing methods, annotation guidelines, dataset partitions, and experimental configurations.
Conclusion 
The Banking Mobile User Interface Dataset (BMUID) provides a domain-specific multimodal data foundation for research in intelligent mobile interface understanding and analysis. By incorporating banking application screenshots and associated visual, textual, structural, semantic, and navigational information, the dataset supports a broad range of research applications, including UI component recognition, screen classification, semantic interpretation, user-intent prediction, navigation analysis, and adaptive interface personalization. Its banking-oriented functional categories provide opportunities to investigate the relationship between interface structures and user objectives in complex mobile application environments. Furthermore, BMUID can facilitate the development and evaluation of advanced artificial intelligence approaches integrating computer vision, natural language processing, multimodal representation learning, and intelligent decision-making. Consequently, the dataset offers a useful research resource for exploring next-generation intelligent, context-aware, and adaptive mobile user interfaces.

