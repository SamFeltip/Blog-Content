---
tags:
  - technology/programming
---


How can I use table storage for forms?

## Questions

PK: form
RK: questionId

## Question answers

PK: form
RK: QAid

Value

## Form comments

PK: UserFormId
FK: CommentId

QuestionId
Timestamp
Commenter userId 
Comment
Status: open/pending/resolved

# Queries

- Open a form and fill in details
	- Form
	-  questions for a form
	-  QAs for a form and user
- Review a user form fill in
	- Form
	- Questions for a form
	- QAs for a form
- Get all user details for a form
	- Form
	- Questions for a form
	- QAs for a form (all users)
- Forms for a user
	- UserForms for a user
	- 

---
## prompt

looks like openapi zod client does not include schemas in lists when using --group-strategy=tags