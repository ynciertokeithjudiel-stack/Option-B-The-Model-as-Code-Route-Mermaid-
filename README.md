#My Enrollment Model
```mermaid
erDiagram
    STUDENT ||--o{ ENROLLMENT : "makes"
    SESSION ||--o{ ENROLLMENT : "receives"
    
    STUDENT {
        string student_id PK
        string name
        string email
    }
    SESSION {
        string session_id PK
        string course_name
        int capacity
    }
    ENROLLMENT {
        string enrollment_id PK
        string student_id FK
        string session_id FK
        date enrollment_date
    }
