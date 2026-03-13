# Project Management Plaform

### Database Migration
    `DB/migrations`
        `1.sql`
        `2.sql`
        `3.sql`
        dbmigrate

        what these tools do:
        goes through file in a sequential manner (timestamp)

        - up migration 
        - down migration (revert )

        why migration needed?
        1. Keeping track of database changes
        2. Rollback