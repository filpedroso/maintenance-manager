Code built in the context of Trailhead's Apex Specialist superbadge.

MaintenanceRequestHelper/ Trigger/ Test: class is triggered every time a repair case is closed and creates a new routine maintenance case based on the shortest maintenance cycle among the equipments involved in that case. Has also a trigger class and a Test

WarehouseCalloutService/ Mock/ Test: queueable Apex that calls a service via REST API's GET method to check for updates into external database, fetchs data if there are any, deserialises the JSON data, creates an object from it and upserts into database. Has a mock class for testing and a Test class.

WarehouseSyncSchedule/ Test: turns WarehouseCalloutService into schedulable Apex by calling it from a schedulable-implemented class. Has also its test.