# Iot World Forum (IoTWF)

**7 layer IoT architecture reference model**

Layers:
	1. Physical Devices and Controllers
	2. Connectivity
	3. Edge Computing
	4. Data Accumulation
	5. Data Abstraction
	6. Application
	7. Collaboration and Processes

### Layer 1: Physical Devices and Controllers
- This layer includes various endpoints that send and receive information.
- Size of "things" can vary from microscopic sensors to giant machines in a factory
- Primary function is generating data and being capable of being queried and/or controlled over a network.

### Layer 2: Connectivity
- Important function of this layer is the *reliable* and *timely transmission of data*
	- This includes transmission between Layer 1 devices and the network, and between the network and information processing that occurs at Layer 3

### Layer 3: Edge Computing
- The emphasis is on data reduction and converting network data flows into information that is ready for storage and processing by higher layers.
- One of the basic principle of this reference model is:
	- Information processing is initiated early and as close to the edge of the network as possible.

### Layer 4: Data Accumulation
- Captures data and stores it so it is usable by application when necessary.
- Converts event-based data to query-based processing

### Layer 5: Data Abstraction
- Reconcile multiple data formats and ensures consistent semantics from various sources.
- Confirms that the data set is complete and consolidates data into one place or multiple data stores using virtualizaiton

### Layer 6: Application
- Interprets data using software applications
- Applications may monitor, control, and provide reports based on the analysis of the data

### Layer 7: Collaboration and Process
- Consumes and shares the application information
- Collaboration on and communicating IoT information often requries multiple steps, and it is what makes IoT useful.
- This layer can change business processes and delivers the benefits of IoT.