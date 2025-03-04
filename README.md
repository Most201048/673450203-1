def calculate_grade_info(grades):
    """
    ฟังก์ชันนี้ใช้ในการคำนวณเกรดสูงสุด, ต่ำสุด, GPA และจำนวนคน
    :param grades: รายการของเกรดที่นักศึกษาได้รับ (เป็นจำนวนจริง)
    :return: ข้อมูลที่ประกอบด้วยเกรดสูงสุด, ต่ำสุด, GPA และจำนวนคน
    """
    
    if not grades:
        return None, None, None, 0
    
    # คำนวณเกรดสูงสุดและต่ำสุด
    highest_grade = max(grades)
    lowest_grade = min(grades)
    
    # คำนวณ GPA (สมมติว่า GPA คือ ค่าเฉลี่ยของเกรด)
    gpa = sum(grades) / len(grades)
    
    # จำนวนคน
    num_people = len(grades)
    
    return round(highest_grade, 2), round(lowest_grade, 2), round(gpa, 2), num_people

# ตัวอย่างการใช้งาน
grades = [3.5, 4.0, 2.7, 3.8, 3.1]
highest, lowest, gpa, num_people = calculate_grade_info(grades)

print(f"เกรดสูงสุด: {highest}")
print(f"เกรดต่ำสุด: {lowest}")
print(f"GPA: {gpa}")
print(f"จำนวนคน: {num_people}")
