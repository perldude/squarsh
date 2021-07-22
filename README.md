# squarsh

Building a url-shortener using AWS as an exercise.

## The Plan

I want to start small and simple and build up to needlessly complicated
so I can play with more things.

It will start off as your basic URL shortener,
with user-selectable expiration times.
Then I want to it to, if the "URL" doesn't have a protocol, throw up text.
Like a secret message.

## The Phases

### Simplicity with a Pipeline

This whole thing can pretty simply be done with a Lambda (or two).
So, do that first.
However, I do want this done in a pipeline.
Merging a PR should trigger testing and deployment.
We'll see if golang testing has gotten better since I last checked.

### Containers and Caching

Put stuff in containers, put the containers on EC2 instances,
and add their building into the pipeline.
Do some caching with CloudFront and put things behind ELB..

### At Scale

Now that things are working well, make things scalable for the millions of
requests per second that such a great idea will be attracting.
Put the containers in ECS and use Fargate for orchestration.
