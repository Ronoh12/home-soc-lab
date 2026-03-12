# Failed Login Investigation

## Objective
Investigate failed authentication attempts recorded in Windows Security logs.

## Evidence Source
Windows Security Event Log

## Relevant Event
Event ID: 4625  
Meaning: An account failed to log on.

## Observations

Multiple failed authentication attempts were generated using the `runas` command.

Attempted account:
fakeuser

Failure reason:
Unknown user name or bad password

Logon Type:
2 (Interactive logon attempt)

## Investigation Steps

1. Generated failed login attempts using runas command.
2. Queried Windows Security logs for Event ID 4625.
3. Reviewed authentication failure details.
4. Identified attempted username and failure reason.

## Security Significance

Event ID 4625 may indicate:

- Incorrect user credentials
- Unauthorized login attempts
- Brute force attack attempts
- Misconfigured authentication systems

## Conclusion

The captured logs demonstrate how failed login attempts appear in Windows Security Event logs. This investigation illustrates how SOC analysts detect and analyze authentication failures.