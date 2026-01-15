| HTTP Method | Endpoint       | Description                       | Request Body                                         | Response (Success) | Status Code |
| ----------- | -------------- | --------------------------------- | ---------------------------------------------------- | ------------------ | ----------- |
| GET         | /api/rooms     | ดึงรายการห้องทั้งหมด (filter ได้) | –   | `[ {room} ]`  | 200         |
| GET         | /api/rooms/:id | ดึงข้อมูลห้องเดียว                | –   | `{room}`           | 200         |
| POST        | /api/rooms     | สร้างห้องใหม่ (Staff)             | `{room_name, building, floor, capacity, facilities}` | `{room}`           | 201         |
| PUT         | /api/rooms/:id | แก้ไขข้อมูลห้อง (Staff)           | `{room_name, building, floor, capacity, facilities}` | `{room}`           | 200         |
| GET         | /api/bookings             | ดึงการจองทั้งหมด (Staff) | –                                                        | `[ {booking}, ... ]` | 200         |
| GET         | /api/bookings/my          | ดึงการจองของตัวเอง       | –                                                        | `[ {booking}, ... ]` | 200         |
| POST        | /api/bookings             | สร้างการจองใหม่          | `{room_id, booking_date, purpose}` | `{booking}`          | 201         |
| DELETE      | /api/bookings/:id         | ยกเลิกการจอง             | –                                                        | `{message}`          | 200         |
| PATCH       | /api/bookings/:id/approve | อนุมัติการจอง (Staff)    | `{status}`                                               | `{booking}`          | 200         |
| POST        | /api/auth/register | สมัครสมาชิก    | `{name, email, password, role}` | `{message}`           | 201         |
| POST        | /api/auth/login    | เข้าสู่ระบบ    | `{email, password}`             | `{message}`          | 200         |

     
