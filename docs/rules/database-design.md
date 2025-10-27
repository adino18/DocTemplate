# TravelFollower - Quy Tắc Thiết Kế Database

## Luồng xử lý Database Development

### 1. Design Phase
- Design schema theo business requirements
- Define relationships và constraints
- Plan indexes cho performance

### 2. Implementation Phase
- Create migration files
- Run migrations trên development
- Test với sample data

### 3. Deployment Phase
- Review migration scripts
- Run migrations trên staging
- Deploy đến production

## Quy định bắt buộc

### Schema Design
- Sử dụng UUID cho primary keys
- Add created_at, updated_at timestamps
- Use soft deletes với deleted_at
- Define foreign key constraints

### Migration Rules
- Migration filename: `YYYYMMDD_HHMMSS_description.sql`
- Migrations phải có rollback script
- Test migrations trên development trước
- Review migrations trước khi deploy

### Performance Rules
- Add indexes cho foreign keys
- Add composite indexes cho common queries
- Use partial indexes cho specific conditions
- Monitor query performance

## Workflow

### Database Change Process
1. **Design**: Create ER diagram → Get approval
2. **Migration**: Write migration → Test locally
3. **Review**: Code review migration → Test on staging
4. **Deploy**: Run migration → Verify data

### Tables Structure
```sql
-- Primary key pattern
id UUID PRIMARY KEY DEFAULT gen_random_uuid()

-- Timestamps pattern
created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
updated_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
deleted_at TIMESTAMP WITH TIME ZONE

-- Foreign key pattern
user_id UUID REFERENCES users(id) ON DELETE CASCADE
```

### Index Strategy
```sql
-- Foreign key indexes
CREATE INDEX idx_locations_user_id ON locations(user_id);

-- Composite indexes
CREATE INDEX idx_visits_user_date ON visits(user_id, visit_date DESC);

-- Partial indexes
CREATE INDEX idx_active_users ON users(id) WHERE is_active = true;
```

## Data Integrity Rules
- Use foreign key constraints
- Add check constraints cho data validation
- Use triggers cho complex validation
- Implement proper cascading deletes

---

*AI Agent phải tuân thủ quy định này khi thay đổi database schema.*