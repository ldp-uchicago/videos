# Project Directory Structure

Proposed layout for `midway.rcc.uchicago.edu:/project/sgsg`:

    /lab    # GM Lab files

    /ldp

      /docs
        /subjects
          README.md       # desc of subject groupings
          group-1.md      # list of subj IDs in normally-developing group
          group-2.md      # list of subj IDs in brain-injured group
        /visits
          README.md       # desc of visit periods
          period-1.tsv    # list of period 1 visits
          period-2.tsv    # list of period 2 visits
          period-3.tsv    # list of period 3 visits
        /protocols        
          README.md       # desc of each period’s protocol w/ links to docs
          /period-1
            /spontaneous
            /stimuli      # we can symlink stimuli docs used across periods
          /period-2
            /spontaneous
            /stimuli
          /period-3
            /spontaneous
            /stimuli
          
      /resources          # all other non-video content goes in here
        /stimuli

      /videos             # all video content goes in here
        /visits
          /group-1        # normally-developing subjects
            /period-1       # home visits over 12 sessions
            /period-2       # KG to 4G (visits made 3 times each year)
            /period-3       # 5G to 9G
          /group-2        # brain-injured subjects
            /period-1
            /period-2
            /period-3
        /examples
          /gesture
          /speech         # empty for now
