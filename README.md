# face_recognition_project




#  Face Recognition Attendance System

This is a Python-based **automated student attendance system** that uses real-time **facial recognition** to detect and mark attendance. The system uses a webcam to recognize faces and logs the data into a CSV file. A Streamlit dashboard is included to view the daily attendance visually.

---

##  Features

- Real-time face detection and recognition via webcam  
- Attendance logged automatically with name and timestamp  
- Stores data securely in daily CSV files  
- Live dashboard using Streamlit for attendance monitoring  
- Simple CLI-based face registration  
- Attendance reset feature for easy data management  

---

## Technologies Used

- **Python**  
- **OpenCV**  
- **NumPy**  
- **face_recognition** (via `sklearn` + `KNN`)  
- **Streamlit**  
- **CSV** for logging  
- **win32com.client** (for speech synthesis on Windows)  

---

## 🗂️ Project Structure

```bash
├── Attendance/                # Stores daily CSV files for attendance
├── data/                     # Stores Haar cascade and serialized face/name data
│   ├── haarcascade_frontalface_default.xml
│   ├── names.pkl
│   ├── faces_data.pkl
├── background.png            # UI background for OpenCV window
├── add_faces.py              # Script to register new faces and names
├── test.py                   # Face recognition & attendance logging
├── clear.py                  # Clears all saved faces and names
├── app.py                    # Streamlit dashboard to view attendance
├── README.md                 # This file
````

---

## 🧠 How It Works

### 1. **Face Registration**

Run `add_faces.py` to add a new user's face to the system.

* Captures 100 face samples via webcam.
* Stores flattened data in `faces_data.pkl` and names in `names.pkl`.

```bash
python add_faces.py
```

---

### 2. **Attendance System**

Run `test.py` to start the face recognition and attendance logging.

* Detects and recognizes faces in real-time.
* On pressing **`O`**, it logs the recognized name with timestamp into `Attendance/Attendance_<date>.csv`.

```bash
python test.py
```

---

### 3. **Clear Database**

Use `clear.py` to reset all saved face data.

```bash
python clear.py
```

---

### 4. **Streamlit Dashboard**

Visualize attendance using a simple live-updating dashboard.

```bash
streamlit run app.py
```

---

## 📊 Output

* Attendance is saved as `.csv` in the `Attendance/` folder.
* Files are named like: `Attendance_24-06-2025.csv`
* Columns: `NAME`, `TIME`

---

## ⚠️ Requirements

Install dependencies using:

```bash
pip install opencv-python numpy streamlit pandas scikit-learn pywin32
```

---

## 📝 Future Enhancements

* GUI for adding/removing users
* Database integration (SQLite/MySQL)
* Email/SMS notification
* Admin dashboard with charts & analytics

---

## 🙋‍♂️ Author

**Shanmugapriyan B**
Full Stack Developer | IT Student
📧 [shanmugapriyan063@gmail.com](mailto:shanmugapriyan063@gmail.com)
📞 7094308397
[LinkedIn](https://www.linkedin.com/in/shanmugapriyan-b-462a0232a/)

---

## 📄 License

This project is for educational purposes only. Feel free to fork, modify, and improve