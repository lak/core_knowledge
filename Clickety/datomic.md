![](https://thumbs.gfycat.com/FatherlyGoldenGarpike-max-1mb.gif)

This is the detailed scope of work for migrating from PostgreSQL as our primary transactional database to Datomic.

- [x] Pitch: https://github.com/clicketycorp/documents/pull/344
**the work**
 - [x] incorporate datomic schema support into clickety-services application
 - [x] incorporate clojure.spec schema support into clickety-services application
 - [x] test-drive datomic user creation via tx-data / transaction functions in datomic ions
 - [x] enable CI for datomic code paths
     - [x] prep test suite for datomic CI
     - [x] create s3 bucket for private maven uploads (datomic.ions, datomic-dev-local)
     - [x] create bin/ script to run datomic CI
     - [x] use maven s3 repo for dev-local deps when appropriate
     - [x] create GitHub Actions workflow to run datomic CI (uses dev-local and s3 private maven repository)
     - [x] configure datomic CI to not block GitHub PR merges
 - [x] add datomic connection into context via pedestal interceptor for use by API resolvers / mutators
 - [ ] remove all deprecated schema endpoints / types / etc. (coordinate with Sandy)
 - [x] infrastructure
     - [x] destroy jpp infrastructure (currently paused)
     - [x] delete jpp pg instance 
     - [x] code to import production postgres to production datomic (note: we can delete and re-create datomic databases easily)
 - [x] write to datomic on interaction ingestion - https://github.com/clicketycorp/clickety-services/pull/493
     - [x] create interaction subtype data for a given interaction
     - [x] create interaction (non-subtype) data for a given interaction
     - [x] create handles and people
     - [x] ensure we rename people as we get better information
     - [x] create interaction-handles
     - [x] wire this into our normal email ingestion flow
     - [x] write to datomic on calendar ingestion
 - [x] feature flag users in postgres to read from datomic
 - [x] add function to check read feature flag and return datomic reads in resolvers
 - [ ] bring jpp code for API read queries (*ByGid) to clickety-services system
 - [x] implement self query
 - [ ] Graphql API Migrations
     - [ ] ApiKey
          - [ ] mutation/create-api-key
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/edit-api-key
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/revoke-api-key
              - [ ] mutation
              - [ ] response resolution          
          - [ ] query/api-key-by-gid
          - [ ] query/api-keys
     - [ ] Board
          - [ ] mutation/create-stack2
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/move-person-to-stack2
              - [ ] mutation
              - [ ] response resolution          
          - [ ] query/board-by-gid
     - [ ] ClicketyInteraction
          - [ ] query/clickety-interaction-by-gid
     - [ ] Followup
          - [ ] mutation/create-followup
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/edit-followup
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/resolve-followup
              - [ ] mutation
              - [ ] response resolution          
          - [ ] query/followup-by-gid
     - [ ] Group
          - [ ] mutation/copy-group
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/create-group
              - [x] mutation
                  - [x] flat groups support
                  - [ ] nested groups support
              - [ ] response resolution 
          - [ ] mutation/delete-group
              - [ ] mutation
              - [ ] response resolution
          - [ ] mutation/edit-group
              - [x] mutation
              - [ ] response resolution          
          - [ ] mutation/move-group-to-group
              - [ ] 🟢 mutation
              - [ ] response resolution          
          - [ ] mutation/move-people-to-group
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/move-person-to-group
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/remove-people-from-group
              - [ ] mutation
              - [ ] response resolution          
          - [ ] query/group-by-gid
          - [ ] query/groups
     - [ ] Handle
          - [ ] mutation/create-handle
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/move-handle-to-person
              - [ ] mutation
              - [ ] response resolution          
          - [ ] query/handle-by-gid
          - [ ] query/handle-lookup
          - [ ] query/handles
     - [ ] Interaction
          - [ ] query/interaction-by-gid
     - [ ] InteractionSummaryConnection
          - [ ] query/activity-feed-connection
          - [ ] query/interaction-summary-connection
     - [ ] Person
          - [ ] mutation/create-person
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/edit-person
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/merge-people
              - [ ] mutation
              - [ ] response resolution          
          - [ ] query/people-with-followups
          - [ ] query/person-by-gid
     - [ ] PersonComment
          - [ ] mutation/create-person-comment
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/delete-person-comment
              - [ ] mutation
              - [ ] response resolution          
          - [ ] query/person-comment-by-gid
     - [ ] PersonCommentConnection
          - [ ] query/person-comment-connection
     - [ ] PersonConnection
          - [ ] query/person-connection
     - [ ] SearchHit
          - [ ] query/search-all-summary
     - [ ] Service
          - [ ] query/service-by-gid
          - [ ] query/services
     - [ ] Stack
          - [ ] mutation/create-stack
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/delete-stack
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/edit-stack
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/move-person-to-stack
              - [ ] mutation
              - [ ] response resolution          
          - [ ] mutation/move-stack
              - [ ] mutation
              - [ ] response resolution          
          - [ ] query/stack-by-gid
     - [ ] Subscription
          - [ ] query/subscription-by-gid
          - [ ] query/subscriptions
     - [x] User
          - [x] query/self-user          
- [ ] followups
    - [ ] implement parallel writes first
    - [ ] implement reads
- [ ] search
    - [ ] add indexing into existing search index with new document_type names for datomic
    - [ ] call into existing search function (with new document_type names) for search results
- [ ] create user in datomic when creating in postgres
- [ ] Account deletion (postpone)
    - [ ] support string data encryption
    - [ ] use encryption as the means for account deletion
- [ ] Enable feature flag for clickety employees
- [ ] final import production postgres to production datomic (note: we can delete and re-create datomic databases easily)
- [x] Enable feature flag for clickety users


Related:
 - https://github.com/clicketycorp/jpp/issues/6
 - https://github.com/clicketycorp/jpp/issues/4
 - https://github.com/clicketycorp/jpp/pull/1
 - https://github.com/clicketycorp/jpp/pull/2
 - https://github.com/clicketycorp/jpp/pull/3
 - https://github.com/clicketycorp/jpp/pull/5
 - https://github.com/clicketycorp/jpp/pull/7
 - https://github.com/clicketycorp/jpp/pull/8
 - https://github.com/clicketycorp/jpp/pull/9
 - https://github.com/clicketycorp/jpp/pull/10
 - https://github.com/clicketycorp/jpp/pull/11
 - https://github.com/clicketycorp/jpp/pull/12
 - https://github.com/clicketycorp/jpp/pull/13
 - https://github.com/clicketycorp/jpp/pull/14
 - https://hackmd.io/9o2_bomXTkKUF9_0mBVPow

cc @clicketycorp/engineering

