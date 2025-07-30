# FeatureVotingApp Resources

## Demo Video

Watch my demo video to see FeatureVotingApp in action:

[📹 FeatureVotingApp Demo Video](https://www.loom.com/share/0d7d2cec223d443394136d4d11cd6998?sid=6c975da2-0f80-41e2-9cd2-f425a3b9b9bd)

## Screenshots

<img width="1919" height="1032" alt="image" src="https://github.com/user-attachments/assets/1fc3b7e2-18dd-4cac-ab42-67e011cbaa6b" />

<img width="1919" height="1031" alt="image" src="https://github.com/user-attachments/assets/36c12895-82df-4585-9b3d-00ca2690d7f8" />

## Backend Structure

### Database Structure (dev.db)
```
backend/
├── prisma/
│   ├── dev.db                    # SQLite database file (12KB)
│   └── schema.prisma             # Prisma schema definition
```

**Database Schema:**
```sql
-- Table: features
CREATE TABLE features (
  id    TEXT PRIMARY KEY DEFAULT (uuid()),
  title TEXT NOT NULL,
  votes INTEGER DEFAULT 0
);
```

### Environment Configuration (.env)
```
backend/
├── .env                          # Environment variables file
```

**Environment Variables:**
```env
DATABASE_URL="file:./dev.db"
```

### Complete Backend Tree Structure
```
backend/
├── .env                          # Environment variables
├── .gitignore                    # Git ignore rules
├── package.json                  # Node.js dependencies
├── yarn.lock                     # Yarn lock file
├── tsconfig.json                 # TypeScript configuration
├── nodemon.json                  # Nodemon configuration
├── download-swagger.js           # Swagger download script
├── README.md                     # Backend documentation
├── SETUP.md                      # Setup instructions
├── logs/                         # Application logs directory
├── node_modules/                 # Node.js dependencies
├── prisma/
│   ├── dev.db                   # SQLite database
│   └── schema.prisma            # Database schema
├── src/
│   ├── config/
│   │   └── swagger.ts           # Swagger configuration
│   ├── middleware/
│   │   ├── requestLogger.ts     # Request logging middleware
│   │   └── validation.ts        # Validation middleware
│   ├── routes/
│   │   └── features.ts          # Feature routes
│   ├── schemas/
│   │   └── feature.ts           # Feature validation schemas
│   ├── utils/
│   │   └── logger.ts            # Logging utilities
│   └── server.ts                # Main server file
└── tests/
    ├── api.test.js              # API tests
    ├── openapi.test.js          # OpenAPI tests
    ├── validation.test.js       # Validation tests
    └── test-runner.js           # Test runner
```
