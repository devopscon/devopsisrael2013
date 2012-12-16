The 2013 Israel DevOps Summit 
=============================

```ruby
require 'speaker'
require 'israel'

module Israel
  module DevOps
    def call_for_papers(speaker, subject)
      # Speakers, please apply for the call for papers if you have talks on the subjects of Continuous 
      # Deployment, DevOps tooling and DevOps case studies, assuming you are available on Jan 15.
      apply(spekaer) if ["Continuous Deployment Case Studies", 
                         "DevOps tools", 
                         "DevOps Case Studies"].include(subject) 
                        and speaker.available?(Date.new(2013,1,15))
    end
    def apply(speaker)
      # We prefer github, but also settle for goo-ol emails
      if speaker.has_github?
        speaker.make_pull_request('/devopscon/devopsisrael2013')
      else
        speaker.send_mail('proposals@devopscon.com')
    end
  end
end
```

If you need it in plain English, here goes:

This repo provides means to propose speaking sessions for the 2013 Israel DevOps Summit. To submit a proposal, fork the repo, add a text file named `your-session.md` (there's a sample template named `sample-proposal.md` in this repo), and submit a pull request. Alternatively, if you're not into github, email your proposal to proposals@devopscon.com. In your email, make sure to specify the following:

- Session title
- Session abstract
- Speaker bio
- Any references for the speaker's record - videos, slide decks, etc.
