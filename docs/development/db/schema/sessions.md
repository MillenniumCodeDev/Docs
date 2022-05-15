# sessions

## sessions Collection

| _id | empId | sessionId | sessionDate |
|-----|-------|-----------|-------------|

* _id: Unique ObjectId
* empId: Employee ObjectId
* sessionId: Session Id for user validation/login
* sessionDate: Initial date, valid up to 120 minutes (will be deleted by either a pm2 or cron job)