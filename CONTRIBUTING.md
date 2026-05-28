# Contributing to AkshaMart

Thank you for your interest in contributing to AkshaMart! This document provides guidelines and instructions for contributing.

## Code of Conduct

Be respectful, inclusive, and professional in all interactions.

## Getting Started

### Prerequisites
- Node.js 20+
- PostgreSQL 15+
- Redis 7+
- Docker & Docker Compose

### Setup Development Environment

```bash
# Clone repository
git clone https://github.com/vrahmdevtiwari/aksha-mart.git
cd aksha-mart

# Install dependencies
npm install

# Setup environment
cp .env.example .env.local

# Start services
docker-compose up -d

# Run migrations
npm run db:migrate

# Seed data
npm run db:seed

# Start development
npm run dev
```

## Development Guidelines

### Branch Naming
- Feature: `feature/description`
- Bugfix: `fix/description`
- Documentation: `docs/description`
- Chore: `chore/description`

### Commit Messages

Use conventional commits:

```
<type>(<scope>): <subject>

<body>

<footer>
```

Types:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation
- `style`: Formatting
- `refactor`: Code refactoring
- `perf`: Performance improvement
- `test`: Tests
- `chore`: Build/config changes

### Code Style

- Use TypeScript
- Follow ESLint rules
- Format with Prettier
- Write descriptive variable names
- Add comments for complex logic

### Testing

```bash
# Run tests
npm run test

# Unit tests
npm run test:unit

# E2E tests
npm run test:e2e

# Coverage
npm run test:coverage
```

Minimum coverage: 80%

## Pull Request Process

1. Create feature branch
2. Make changes
3. Run tests: `npm run test`
4. Lint code: `npm run lint`
5. Format code: `npm run format`
6. Commit changes
7. Push to fork
8. Create pull request
9. Ensure CI passes
10. Request review

## Pull Request Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing
Describe testing performed

## Checklist
- [ ] Tests pass
- [ ] Code linted
- [ ] Documentation updated
- [ ] No breaking changes
```

## Project Structure

- `packages/backend/` - NestJS backend
- `packages/frontend/` - Next.js frontend
- `packages/admin/` - Admin dashboard
- `packages/shared/` - Shared types
- `infrastructure/` - Deployment configs
- `docs/` - Documentation

## Security

For security issues, email security@aksha-mart.com instead of creating public issues.

## Questions?

Create an issue or contact: support@aksha-mart.com
