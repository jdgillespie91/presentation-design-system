Create a technical architecture overview presentation for new engineers joining the platform team.

Slide 1: Title slide - "Platform Architecture Overview" for new engineer onboarding.

Slide 2: High-level system diagram overview. We have three main layers:
- Client layer: React web app, iOS/Android mobile apps
- API layer: GraphQL gateway, REST API for legacy integrations
- Data layer: PostgreSQL (primary), Redis (caching), Elasticsearch (search)

Slide 3: The API Gateway in detail:
- Built on Node.js with Apollo Server
- Handles authentication via JWT tokens
- Rate limiting: 1000 req/min for free tier, 10000 for paid
- Deployed on AWS ECS with auto-scaling

Slide 4: Database architecture:
- PostgreSQL 15 on RDS (Multi-AZ)
- Read replicas in US-East and EU-West
- Redis cluster for session storage and caching
- Daily backups retained for 30 days

Slide 5: Key services overview:
- auth-service: User authentication and authorization
- billing-service: Stripe integration, subscription management
- notification-service: Email (SendGrid), push (Firebase), SMS (Twilio)
- analytics-service: Event ingestion, aggregation pipelines

Slide 6: Development workflow:
- GitHub for source control
- CI/CD via GitHub Actions
- Staging environment mirrors prod at 10% scale
- Feature flags via LaunchDarkly

Slide 7: Where to find more info - links to internal docs, Slack channels (#platform-help), and who to ask (list the platform team leads).
