📌 Entities & Attributes 1️⃣ Gymnasium

gym_id (Primary Key) name address phone_number 2️⃣ Member

member_id (Primary Key) first_name last_name address date_of_birth gender gym_id (Foreign Key → Gymnasium) 3️⃣ Coach

coach_id (Primary Key) first_name last_name age specialty 4️⃣ Session

session_id (Primary Key) sport_type schedule max_members (Default: 20) 5️⃣ Member_Session (Many-to-Many Relationship Between Member & Session)

member_session_id (Primary Key) member_id (Foreign Key → Member) session_id (Foreign Key → Session) 6️⃣ Coach_Session (Many-to-Many Relationship Between Coach & Session)

coach_session_id (Primary Key) coach_id (Foreign Key → Coach) session_id (Foreign Key → Session) 📌 Relationships ✅ One Gymnasium can have many Members → (1 Gymnasium : ∞ Members) ✅ One Session can have up to 20 Members → (Many-to-Many: Session ↔ Members) ✅ One Session can have up to 2 Coaches → (Many-to-Many: Session ↔ Coaches) ✅ A Coach can lead multiple Sessions → (Many-to-Many: Coach ↔ Sessions)