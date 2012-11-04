The 2013 Israel DevOps Summit 
=============================

```ruby
require 'speaker'
require 'israel'

module Israel
  module DevOps
    def call_for_papers(speaker, subject)
      # Speakers should apply for the call for papers if they have talks on the subjects of Continuous Deployment of DevOps tooling
      # Assuming they are available Jan 13.
      apply(spekaer) if ["Continuous Deployment Case Studies", "DevOps tools", "DevOps Case Studies"].include(subject) and speaker.available?(Date.new(2013,1,15))
    end
    def apply(speaker)
      # We prefer github, but also settle for goo-ol emails
      if speaker.has_github?
        speaker.make_pull_request('/devopscon/devopsisrael2013')
      else
        spekaer.send_mail('proposals@devopscon.com')
    end
  end
end
```

If you need it in plain English, here goes:

This repo provides means to propose speaking sessions for the 2013 Israel DevOps Summit. 
To submit a paper, you have one of two options: 
1. Create a text document in the format specified in the `sample-proposal.md` file located at the root of this repo. 
2. Email your proposal to propose@devopscon.com. In your email, make sure to specify the following: 

- Session title 
- Session abstract 
- Speaker bio 
- Any references for the speaker's record - videos, slide decks, etc. 
