# WhatNext Vision Motors - Salesforce Project

A comprehensive Salesforce application for managing vehicle inventory, orders, test drives, and dealer operations for Vision Motors.

## 📋 Overview

This Salesforce project provides a complete vehicle management solution including inventory tracking, order processing, test drive scheduling, and dealer assignment workflows. The system automates stock management and provides real-time alerts for various business processes.

## 🚗 Key Features

### Vehicle Management
- **Inventory Tracking**: Real-time stock quantity monitoring
- **Vehicle Registration**: Complete vehicle onboarding process
- **Stock Alerts**: Automated notifications when inventory reaches zero

### Order Processing
- **Order Validation**: Prevents orders when vehicles are out of stock
- **Automatic Stock Updates**: Decreases inventory when orders are confirmed
- **Batch Processing**: Scheduled processing of pending orders
- **Order Status Tracking**: Comprehensive order lifecycle management

### Test Drive Management
- **Test Drive Scheduling**: Customer test drive booking system
- **Email Notifications**: Automated alerts for test drive confirmations
- **Reminder System**: Follow-up notifications for scheduled test drives

### Dealer Operations
- **Dealer Assignment**: Automated assignment of vehicles to nearest dealers
- **Dealer Management**: Complete dealer relationship management

## 🏗️ Technical Architecture

### Custom Objects
- `Vehicle` - Vehicle inventory management
- `Vehicle Order` - Order processing and tracking
- `Vehicle_Dealer` - Authorized dealer management and assignment
- `Vehicle_Customer` - Customer profiles and relationship management  
- `Vehicle_Test_Drive` - Test drive scheduling and booking system
- `Vehicle_Service_Request` - Service request tracking and management

### Apex Classes
- **VehicleOrderTriggerHandler**: Business logic for order processing
- **VehicleOrderBatch**: Batch processing for pending orders
- **VehicleOrderBatchScheduler**: Automated scheduling of batch jobs

### Triggers
- **VehicleOrderTrigger**: Handles before/after insert and update events

### Flows & Processes
- Assign Near Dealer Flow
- Test Drive Reminder Flow
- Zero Stock Alert Process


## 📊 Key Business Processes

### Order Processing Flow
1. Customer places vehicle order
2. System validates vehicle availability
3. If in stock, order status set to "Confirmed"
4. Stock quantity automatically decremented
5. Out-of-stock orders are prevented with error message

### Batch Processing
- Runs scheduled jobs to process pending orders
- Confirms orders for available vehicles
- Updates stock quantities automatically
- Processes up to 50 orders per batch

### Stock Management
- Real-time inventory tracking
- Automatic stock updates on order confirmation
- Zero stock alerts and prevention mechanisms

## 📖 Documentation

For detailed documentation, refer to `WhatNext Vision Motors__Documentation.pdf`.


**Vision Motors** - Driving the future of vehicle management with Salesforce technology. 