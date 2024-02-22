# C4 Models

A C4 model is a common set of abstractions used to describe the static structure of a software system; these abstractions having four levels: **software system**, **containers**, **components** and **code**. **People** that use the software system.

The following diagrams use the C4 standard.

## C4 Model Legend

![C4Modelegend](../images/C4-legend)

## System Context Diagram

A **System Context** diagram provides a starting point, showing how the software system in scope fits into the world around it.[^](#expl) 
This diagram shows how the main users of MonitorMe interact with the system, and how it interacts with other systems.

![Context Diagram](../images/C4-system-context)

## Container Diagram

A Container diagram zooms into the software system in scope, showing the high-level technical building blocks.[^](#exp1) The following diagram breaks down the MonitorMe systems into functionalities, and shows how they interact with each other and how the users of the system interact with the functionality.

![Container Diagram](../images/C4-system-container)

## Component Diagrams

A **Component** diagram zooms into an individual container, showing the components inside it.[^](#expl)
The following diagrams break down the containers/functionality shown above further, into components which represent individually deployable services.

### Relevant ADRs

- [003 Database choices (metrics storage / config storage)
- [004 Separate Alert Domain from Metric Domain

### Alert Processing

The following diagram shows the individually deployable services in the Alert processing domain

![Component Diagram Alert](../images/C4-system-component-alert-processor)


#### Relevant ADRs

- [005 use a token based security through evry service call
- [010 We-will-use-an-adapted-query-language-for-realtime-data-or-bulk-data

### Metrics query and visualization

The following diagram shows the individually deployable services in the metrics query domain

![Component Diagram Metrics](../images/C4-system-component-query-viz)
