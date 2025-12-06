🚘 ParkScope – Detecting Free Street Parking Spots from a Single Image
AI-Based Parking Spot Detection using YOLO + Inpainting
⭐ Overview

מציאת חניה ברחוב היא משימה יומיומית מתסכלת. פרויקט ParkScope בונה מערכת שמזהה מקומות חניה פנויים בתמונת רחוב יחידה — ללא מידע חיצוני, ללא חיישנים וללא נתונים היסטוריים.

המערכת משתמשת ב:

זיהוי רכבים קיימים

מחיקה חכמה (Inpainting) של הרכבים

יצירת תוויות (Labels) אוטומטיות של חניות פנויות

אימון מודל YOLO לגילוי חניות בתמונת רחוב אמיתית

🎯 Project Goal

Train an object detection model that identifies free parking spots in street-level images.

כלומר — הפלט הוא:

Bounding boxes של מקומות חניה פנויים

🧩 System Pipeline
 Street Image → Car Detection (YOLO) → Inpainting → Label Generation → Train YOLO → Detect Free Spots

📚 Dataset

הדאטה של ParkScope מורכב משני מקורות:

1️⃣ Real Images

KITTI Dataset – תמונות רחוב אמיתיות מצולמות ממצלמת רכב.
משמשות כבסיס לבניית הדאטה.

2️⃣ Auto-Generated Training Data

נוצר בתהליך אוטומטי:

מפעילים YOLO כדי לזהות רכבים בתמונה.

מוחקים את הרכבים באמצעות Diffusion-based Inpainting או כלי inpainting אחר.

הרקע המשוחזר מגלה את האזורים המועמדים לחניה פנויה.

מייצרים תוויות (bounding boxes) למקומות החניה האלו.

🏗️ Data Generation Pipeline
✔️ Car Detection

YOLO מזהה bounding boxes של כל הרכבים.

✔️ Inpainting

המודל "מוחק" את הרכב ומשחזר את שפת המדרכה באופן ריאליסטי.

✔️ Auto-labeling

אזורי המדרכה שנחשפו לאחר מחיקת הרכב מתויגים כ:

Free Parking Spot

כך נבנה דאטה מתויג ללא עבודה ידנית.

🔧 Data Augmentation

כדי להגדיל את עמידות המודל נוספו:

שינויי תאורה (יום/ערב/צללים)

שינויי בהירות וקונטרסט

טשטוש, רעש

חיתוכים אקראיים (Random Crop)

🧠 Model
✔️ YOLO (v8/v9) – Parking Spot Detector

זהו המודל העיקרי והיחיד בפרויקט.
הוא מאומן לזהות חניה פנויה בתמונה באמצעות הדאטה שנוצר.

🏋️ Training Process

יצירת סט אימון מלא הכולל:

תמונות Inpainting

תוויות Bounding Boxes

חלוקה:

Train / Validation / Test

אימון YOLO לאיתור חניה פנויה.

ניתוח ביצועים ושיפור המודל.

📏 Evaluation Metrics

הערכת הביצועים מתבצעת באמצעות:

mAP@50 – מדד הצלחה כלל-מערכתי

Precision & Recall

דוגמאות איכותיות (visual examples)

📈 Results

(הוסף תמונות, דוגמאות Inpainting, תוצאות YOLO וכו׳ כשהן יהיו מוכנות)

📁 Repository Structure

(להוסיף בהתאם לתיקיות שיש לך — אם תרצה, אבנה לך מבנה קלאסי ל-MLOps)

👤 Team

Lior Yanwo
