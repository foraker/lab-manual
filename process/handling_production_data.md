# The Sanctity of Production

When it comes to production data, the rule here at Foraker is simple: the only thing touching production data (database, assets, user content, etc…) should be production code.

Staging or beta instances or other non-production tools that have the power to modify data should NOT be talking to production data stores.

If there’s some sort of reason why this needs to occur in a specific project, talk with your manager. If a customer tries to push us in that direction because of cost or other, talk with your manager. If you’re currently working on a project where non-production code is talking to production data, let your manager know and we’ll determine if a change needs to be made.