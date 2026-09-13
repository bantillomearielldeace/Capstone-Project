# COTS Monitor: Machine Learning-Based Detection and GIS Mapping of Crown-of-Thorns Starfish

## Overview

**COTS Monitor** is a machine learning-based monitoring system designed to detect, count, map, and monitor Crown-of-Thorns Starfish (COTS) using underwater images captured through GoPro cameras.

The system integrates:

- Machine learning-based image detection
- Underwater image preprocessing
- Automatic COTS counting
- Geographic Information System (GIS) mapping
- Mobile-based field data submission
- Expert validation
- Reef-zone infestation classification
- Alerts and recommended intervention measures
- Removal monitoring and evidence submission
- Analytics and report generation
- Role-based access control

The project focuses on supporting coral reef conservation and marine ecosystem monitoring, particularly in the Davao Gulf area, including locations near Samal and Panabo City.

## Project Objectives

The system aims to:

1. Develop and compare selected object detection models for detecting COTS in underwater images.
2. Develop a GoPro-assisted mobile/web monitoring platform.
3. Map detected COTS locations using GIS and GPS data.
4. Automatically count detected COTS individuals.
5. Support intervention planning, removal monitoring, and field reporting.
6. Generate analytics, visualizations, and reports for conservation decision-making.

## Main Features

### 1. Secure User Login

Authorized users can log in using their account credentials. The system supports role-based access for:

- **Administrator**
- **Expert**
- **Diver / Field Participant**

### 2. Underwater Image Upload

Divers or field participants can upload underwater images captured using GoPro cameras. Batch uploading is supported for multiple images collected during one monitoring activity.

### 3. Image Preprocessing

Uploaded images may undergo preprocessing techniques such as:

- Color correction
- Contrast enhancement
- Image quality improvement
- Other preprocessing techniques for underwater visibility challenges

### 4. AI-Based COTS Detection

The system processes uploaded images using selected object detection models. The proposed study identifies the following models for comparison:

- YOLOv8
- YOLOv11
- YOLO26

Model performance is evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Detection speed

### 5. Confidence-Based Validation

Detection results include confidence scores.

- High-confidence detections may be accepted automatically based on the system rules.
- Low-confidence detections are forwarded to an Expert for review.
- Only accepted or expert-validated records are used as official monitoring records.

### 6. GIS Mapping

Validated COTS detections are plotted on a GIS map using GPS coordinates from the mobile application.

The map can display:

- COTS detection locations
- Monitored reef zones
- Affected areas
- Infestation status
- Spatial distribution of COTS

### 7. Infestation Classification

Reef zones may be classified according to infestation level:

- Low
- Moderate
- High

The classification supports monitoring prioritization, alerts, and intervention planning.

### 8. Alerts and Intervention Support

The system generates alerts for reef zones with moderate or high infestation levels. It may also display recommended intervention measures after expert validation.

### 9. Removal Monitoring

Authorized field participants can submit removal records containing information such as:

- Removal quantity
- Location
- Date
- Supporting photographs or evidence
- Field observations
- Comments
- Validation status

Removal records preserve the history of intervention activities instead of deleting previous detection records.

### 10. Analytics and Reports

Administrators can view or generate:

- Detection statistics
- COTS population trends
- Infestation summaries
- GIS-based analytics
- Monitoring reports
- Removal summaries
- Intervention status reports
- Conservation monitoring summaries

## System Workflow

```text
GoPro Camera
    |
    v
Capture Underwater Images
    |
    v
Upload Images Through Mobile Application
    |
    v
Image Preprocessing
    |
    v
Machine Learning-Based COTS Detection
    |
    v
Confidence Score Evaluation
    |
    +------------------------------+
    |                              |
    v                              v
High-Confidence Detection     Low-Confidence Detection
    |                              |
    v                              v
Accepted Record              Expert Validation
    |                              |
    +--------------+---------------+
                   |
                   v
       Infestation Classification
                   |
                   v
            GIS Map Updating
                   |
                   v
          Alerts and Monitoring
                   |
                   v
       Removal Evidence Submission
                   |
                   v
          Expert Removal Review
                   |
                   v
          Reports and Analytics
```

## System Architecture

The proposed system consists of the following major components:

1. **GoPro Camera** – captures underwater images.
2. **Mobile Application** – allows field participants to log in, upload images, submit monitoring records, and provide removal evidence.
3. **Machine Learning Model** – detects and counts possible COTS in uploaded images.
4. **GIS Module** – maps validated detection locations using GPS coordinates.
5. **Expert Validation Module** – reviews low-confidence detections and removal evidence.
6. **Administrator Dashboard** – manages users, zones, alerts, records, reports, and system settings.
7. **Centralized Database** – stores user accounts, images, detections, locations, alerts, removal records, reports, and audit information.

## User Roles

### Administrator

The Administrator can:

- Manage user accounts and roles
- Monitor reef zones
- View GIS maps
- Review monitoring records
- Manage alerts
- Update zone status
- View analytics
- Generate and export reports
- Configure system settings

### Expert

The Expert can:

- Review AI-generated detection results
- Validate low-confidence detections
- Verify removal evidence
- Review monitoring records
- Help ensure data accuracy and reliability

### Diver / Field Participant

The Diver or Field Participant can:

- Log in to the mobile application
- Upload GoPro underwater images
- Submit monitoring data
- View detection results
- View affected reef zones
- Submit field notes
- Submit removal records
- Upload removal evidence
- Report ecological observations

## Data Stored

The system may store the following information:

- User accounts and roles
- Monitoring captures
- Uploaded underwater images
- GPS coordinates
- Date and time
- Reef zone information
- Estimated depth
- COTS detection counts
- Confidence scores
- Validation status
- Infestation level
- Alerts
- Removal records
- Removal evidence
- Field observations
- Reports and analytics
- Audit information

## Technology and Tools

The project is designed around the following technologies and tools:

- **Machine Learning:** YOLO-based object detection models
- **Image Acquisition:** GoPro underwater camera
- **Mobile Platform:** Flutter-based mobile application
- **GIS:** Geographic Information System mapping
- **Database:** Centralized database for monitoring and conservation records
- **Cloud Processing:** Cloud-based inference for uploaded images
- **Project Methodology:** Hybrid Waterfall and Agile approach
- **Framework:** PADIM — Planning, Analysis, Design, Implementation, and Maintenance

> Note: The exact programming language, database engine, cloud provider, and deployment configuration should be updated here once finalized by the development team.

## Project Methodology

The project follows a hybrid methodology combining Waterfall and Agile.

### Waterfall Activities

- Project planning
- Requirements definition
- Dataset preparation
- Initial system design
- Documentation

### Agile Activities

- Iterative development
- Model training and improvement
- Mobile application development
- GIS integration
- Testing and validation
- Usability improvements

## Scope and Limitations

### Scope

The system covers:

- Image-based COTS detection
- Automatic COTS counting
- Underwater image preprocessing
- GIS mapping
- GPS-based monitoring records
- Infestation classification
- Alerts
- Removal monitoring
- Expert validation
- Analytics and reporting

### Limitations

- The system processes uploaded images rather than continuous live video.
- Detection performance may be affected by turbidity, lighting, visibility, and image quality.
- GPS accuracy may vary in coastal areas.
- The system does not physically or automatically remove COTS.
- Removal activities remain the responsibility of authorized field personnel.
- The system does not predict COTS movement using oceanographic or environmental factors.
- Performance depends on available hardware, network connectivity, and system workload.

## Research Alignment

The project supports:

- **Sustainable Development Goal 14: Life Below Water**
- **DOST Harmonized National Research and Development Agenda**
- **DNSC Research, Development, and Extension Agenda**
- **CHED A.C.H.I.E.V.E. Agenda**

It contributes to coral reef conservation, marine biodiversity protection, environmental monitoring, and data-driven marine resource management.

## Project Team

- **Meariell Deace F. Bantillo**
- **Megan Creer**
- **Angel Lyhksine B. Mayor**

**Institution:** Davao del Norte State College  
**Program:** Bachelor of Science in Information Technology  
**Date:** August 2026

## Future Improvements

Possible future improvements include:

- Real-time underwater video detection
- Offline field data collection and synchronization
- More advanced underwater image enhancement
- Additional object detection models
- Predictive COTS movement analysis
- Improved GPS accuracy
- Citizen-science monitoring
- Expanded reef-zone coverage
- Integration with additional marine environmental datasets

## Status

This project is a capstone research and development project. Features, technologies, model versions, and deployment details may change during implementation and testing.

## License

This project is developed for academic and research purposes. Add the appropriate license here if the project will be publicly distributed.
