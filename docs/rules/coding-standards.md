# TravelFollower - Chuẩn Mã Nguồn

## Luồng xử lý Code Development

### 1. Backend Development (Go)
- Tuân thủ Go conventions
- Sử dụng dependency injection
- Implement proper error handling

### 2. Frontend Development (Vue.js)
- Sử dụng Composition API
- TypeScript cho type safety
- Component-based architecture

### 3. Testing
- Unit tests cho business logic
- Integration tests cho APIs
- E2E tests cho user flows

## Quy định bắt buộc

### Go Standards
```go
// Import organization
import (
    "context"
    "time"
    "github.com/gofiber/fiber/v2"
    "github.com/travelfollower/internal/models"
)

// Function naming
func (s *LocationService) CreateLocation(ctx context.Context, req *CreateLocationRequest) (*models.Location, error) {
    // Implementation
}

// Error handling
if err != nil {
    return nil, fmt.Errorf("failed to create location: %w", err)
}
```

### Vue.js Standards
```vue
<template>
  <div class="location-card">
    <h3>{{ location.name }}</h3>
  </div>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'
import type { Location } from '@/types'

interface Props {
  location: Location
}

const props = defineProps<Props>()
</script>

<style scoped>
.location-card {
  @apply p-4 border rounded-lg;
}
</style>
```

### Database Standards
```sql
-- Table naming: plural, snake_case
CREATE TABLE locations (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    name VARCHAR(255) NOT NULL,
    created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);

-- Index naming: idx_table_column
CREATE INDEX idx_locations_user_id ON locations(user_id);
```

## Quality Requirements

### Code Coverage
- Backend: ≥ 80%
- Frontend: ≥ 80%
- Critical paths: ≥ 90%

### Performance
- API response time: < 200ms
- Database queries: < 100ms
- Frontend bundle size: < 1MB

### Security
- Input validation cho tất cả inputs
- Authentication cho protected endpoints
- No hardcoded secrets
- Proper error handling

## Tools Configuration

### Linting
- Go: golangci-lint
- Vue.js: ESLint + Prettier
- Pre-commit hooks required

### Testing
- Backend: Go testing + testify
- Frontend: Vitest + Vue Test Utils
- E2E: Cypress

---

*AI Agent phải tuân thủ chuẩn này khi viết code.*