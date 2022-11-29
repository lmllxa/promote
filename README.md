# promote


aws cloudformation deploy \ 
  --template-file cloudfront.yml \
  --stack-name production-distro
  --parameter-overrides PipelineID="mybucket678123"


# Four Jobs: create_and_deploy_front_end, get_last_deployment_id, promote_to_production, and clean_up_old_front_end

├── bucket.yml          # Creates a new bucket and bucket policy.       
├── cloudfront.yml      # Creates a Cloudfront Distribution that will connect to the existing ^ bucket.
├── error.html
├── index.html  
└── .circleci
    └── config.yml
