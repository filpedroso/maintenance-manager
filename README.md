# Maintenance & Warehouse Management

This repository contains code developed for Trailhead’s **Apex Specialist** superbadge, focused on automating maintenance and warehouse operations in Salesforce.

## Overview

The code is organized into three main functionalities:

1. **Maintenance Request Automation**
2. **Warehouse REST Integration**
3. **Warehouse Sync Scheduling**

Each section includes core Apex classes, triggers, and test classes to support automated testing.

---

### 1. Maintenance Request Automation

- **Files**: `MaintenanceRequestHelper`, `MaintenanceRequestHelperTrigger`, `MaintenanceRequestHelperTest`
- **Functionality**:
  - **Trigger-Based Automation**: When a repair case is closed, a new maintenance case is created automatically.
  - **Maintenance Cycle Calculation**: Determines the shortest maintenance cycle across all equipment in the case.
  - **Testing**: Includes unit tests to validate trigger behavior and maintenance scheduling logic.

---

### 2. Warehouse REST Integration

- **Files**: `WarehouseCalloutService`, `WarehouseCalloutServiceMock`, `WarehouseCalloutServiceTest`
- **Functionality**:
  - **Queueable Apex**: Uses a queueable class to make a REST API GET call to check for updates in an external warehouse database.
  - **Data Processing**: Fetches, deserializes JSON data, and upserts relevant records into Salesforce.
  - **Mocking and Testing**: Includes a mock class for testing REST API calls and a comprehensive test class for the queueable behavior.

---

### 3. Warehouse Sync Scheduling

- **Files**: `WarehouseSyncSchedule`, `WarehouseSyncScheduleTest`
- **Functionality**:
  - **Schedulable Apex**: Schedules the `WarehouseCalloutService` to run at regular intervals.
  - **Testing**: Includes tests to verify the schedulable functionality and the integration with the warehouse service.

---

## Testing and Deployment

Each module includes test classes that follow best practices for Apex testing, ensuring robust code coverage and system reliability. Deploy these components using Salesforce CLI or through the Salesforce development environment.

--- 

### License

This project is for educational purposes within the Trailhead Apex Specialist superbadge context and is not intended for production use.
