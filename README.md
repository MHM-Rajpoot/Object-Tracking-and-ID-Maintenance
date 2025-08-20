# Summer Research Internship 2025 – Computer Vision Projects  

## Overview  
This internship focused on exploring **Computer Vision**, **Object Detection**, and **Object Tracking** using state-of-the-art tools and models.  
The work was structured into weekly learning outcomes and practical implementations, covering the fundamentals of **OpenCV**, **YOLO**, **SAM**, and advanced **tracking algorithms** like DeepSORT, ByteTrack, and SORT.  

---

## Weekly Progress  

### Week 1: OpenCV Fundamentals  
- Learned the basics of OpenCV and its applications in computer vision.  
- Implemented video reading, displaying, and manipulation (including GIFs).  
- Applied basic image processing techniques: resizing, cropping, filtering.  
- Integrated OpenCV with NumPy, Matplotlib, and Seaborn for visualization.  

### Week 2: YOLO (You Only Look Once) for Object Detection  
- Studied YOLO architecture and how it differs from other detectors.  
- Trained and fine-tuned YOLO models on custom datasets.  
- Applied YOLO for real-world detection tasks (images & videos).  

### Week 3: SAM (Segment Anything Model) for Image Segmentation  
- Understood image segmentation fundamentals and the SAM architecture.  
- Implemented automatic mask generation for images.  
- Explored integration of SAM with detection and tracking tasks.  

### Week 4: Object Tracking with YOLOv8 + DeepSORT  
- Implemented object tracking and unique ID assignment.  
- Learned how DeepSORT maintains identities across video frames.  
- Applied the method to real-world video datasets.  

### Week 5: Object Tracking with YOLOv8 + ByteTrack  
- Implemented tracking using the lightweight ByteTrack algorithm.  
- Understood how ByteTrack optimizes efficiency while maintaining accuracy.  
- Applied YOLOv8 + ByteTrack to video datasets for performance tracking.  

### Week 6: Comparative Analysis – DeepSORT vs ByteTrack  
- Compared YOLOv8 + DeepSORT vs YOLOv8 + ByteTrack.  
- Evaluated performance metrics:  
  - **DeepSORT:** ID Switches, Fragmentation, Tracking Duration.  
  - **ByteTrack:** ID Switches, Fragmentation, Tracking Duration.  
  - **Cross-Algorithm Metrics:** Mean IoU, MOTA-like scores.  
- Identified strengths and weaknesses of each algorithm.  

### Week 7: SORT (Simple Online and Realtime Tracking)  
- Learned the fundamentals of SORT as a fast and lightweight tracker.  
- Implemented IoU-based detection-to-tracker assignment.  
- Explored tracker update rules (hits, no_losses, min_hits, max_age).  
- Compared SORT against DeepSORT and ByteTrack in speed and accuracy.
- Used SAM (Segment Anything Model) for Pig segmentation.

#### SORT Tracker Formula

**1. Intersection over Union (IoU)**

For a predicted bounding box \( B_{pred} \) and a detection box \( B_{det} \):

$$
IoU(B_{pred}, B_{det}) =
\frac{|B_{pred} \cap B_{det}|}{|B_{pred} \cup B_{det}| + \epsilon}
$$

Where:

- \( |B_{pred} \cap B_{det}| \) is the **intersection area**  
- \( |B_{pred} \cup B_{det}| \) is the **union area**  
- \( \epsilon \) is a small constant to avoid division by zero  

**2. Tracker Update Rule**

$$
\text{If } IoU(B_{trk}, B_{det}) \geq \theta
\;\;\Rightarrow\;\;
B_{trk} \leftarrow B_{det}, \;\; hits \mathrel{+}= 1, \;\; no\_losses = 0
$$

$$
\text{Else } \;\;\Rightarrow\;\; no\_losses \mathrel{+}= 1
$$

**3. Tracker Reset (Unmatched Detections)**

$$
B_{trk} \leftarrow B_{det}, \quad
hits = 1, \quad
no\_losses = 0
$$

**4. Output Condition**

A tracker is considered valid if:

$$
hits \geq min\_hits
\quad \text{ or } \quad
frame\_count \leq min\_hits
$$

---

## Skills & Tools Gained  
- **Computer Vision Frameworks:** OpenCV, SAM.  
- **Object Detection Models:** YOLOv8.  
- **Object Tracking Algorithms:** DeepSORT, ByteTrack, SORT.  
- **Data Visualization:** NumPy, Matplotlib, Seaborn.  
- **Performance Analysis:** IoU, ID switches, fragmentation, tracking duration, MOTA-like scores.  

---

## Key Takeaways  
- Gained hands-on experience in modern **object detection and tracking** techniques.  
- Understood trade-offs between **accuracy, robustness, and efficiency** across tracking algorithms.  
- Learned to integrate detection, segmentation, and tracking into complete **computer vision pipelines**.  

---

## Demo Output  
Here’s a sample tracking result from the internship:  

![Tracking Demo](/Output/OutputSAM.gif)  

[Demo 0](https://drive.google.com/file/d/1Is8TXBbEAfy34OH4U-M_h5iEg1UkN3wi/view?usp=sharing)
[Demo 1](https://drive.google.com/file/d/1ljR6NsSlq6iuCMYtU0cYqelMcAjOd65I/view?usp=sharing)

This internship provided a strong foundation in practical computer vision, preparing for advanced research and applications in real-world scenarios.
