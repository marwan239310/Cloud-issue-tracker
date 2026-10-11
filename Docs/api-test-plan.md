Test ID
Request
Expected Result
T01
GET /api/issues
T02
200; JSON array returned.
POST valid title, description, priority
T03
201; complete created issue returned.
POST missing title
T04
400; VALIDATION_ERROR.
POST invalid priority = Critical
T05
400; VALIDATION_ERROR.
PATCH existing issue status =
Resolved
T06
PATCH status = Deleted
200; returned status is Resolved.
400; VALIDATION_ERROR.
T07
PATCH unknown issue ID
T08
404; ISSUE_NOT_FOUND.
GET when no issues exist
T09
200; empty JSON array.
Send unexpected extra server-owned
fields
Server ignores/rejects according to
contract; client cannot choose
authoritative id/status/createdAt.
