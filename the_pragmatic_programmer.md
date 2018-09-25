### By:
* Andrew Hunt
* David Thomas

# Chapter 1
* take responsibility for yourself and your actions

## Take Responsibility
* responsibility is something you actively agree to
* you have the right not to take responsibility for an impossible situation
* make call based on ethics and judgement
* when you make a mistake admit it:
  1. honestly
  2. try to offer options
* do not:
  1. blame
  2. make excuses
* Run conversation through your head:
  1. what is the other person likely to say?
  2. will they ask "have you tried this?"
  3. how will your respond?
  4. before you go is there anything you can try?
* Do not say it cannot be done: explain what can be done to salvage the situation
* Do not be afraid to ask for help
> Provide Options do not Make Excuses

## Software Entropy
* "software rot"
> Don't live with broken windows
* "broken windows": bad designs, wrong decisions, poor code
* fix a "broken window" ASAP
* if you don't have time to fix a "broken window" then board it up
  1. take SOME action
  2. biggest source of rot: neglect

## Putting out Fires
* bad code perpetuates bad code

## Stone Soup & Boiled Frogs
* make them think it's their idea
* You want to do A
  1. doing A will involve delays, committees, resistance (start-up fatigue)
  2. work out what you can reasonable ask for
  3. develop it well
  4. show people and let them marvel
  5. (pretend it's not important) "It would be better if we added X"
  6. make people request you add what you want to add
> Be a catalyst for change
* Stone Soup Villagers
  1. lesson about focusing too tightly
  2. things creep up on us
> Remember the Big Picture
* review what is going on around you

## Good Enough Software
* write software that's "good enough"
* "good enough": all systems meet their user's requirements for success
> Make Quality a Requirement Issue
* great software today is preferable to perfect software tomorrow
* know when to stop
  1. don't spoil a program through overembellishment and over-refinements

## Your Knowledge Portfoloio
* knowledge and experience are your most important assets
* "expiring assets" can quickly become obsolete
* knowledge portfolio
  1. invest regularly - as a habit
  2. diversification is the key to long term success
  3. balance between conservative and high-risk high-reward investments
  4. buy low and sell high
  5. review and rebalance periodically
* building your portfolio:
  1. invest regularly
  2. diversify the tech you're comfortable with
  3. manage risk - don't put all your technical eggs in one basket
  4. buy low sell high - early adopters can really pay off

## Goals
* learn at least one new language a year
* read a technical book each quarter
* read nontechnical books
* take classes
* participate in local user groups
* experiment with different environments
* stay current
* get wired - look for content on the web

## Opportunities
* don't stop there - take the times you have something you don't know as a challenge and research
* don't let it rest - find someone who has the answer
* plan ahead: have something to read on hand at all times

## Critical Thinking
* think critically about what you consume (avoid zealous dogma)
* what source you have found may not be the best source

## Guru Tricks
* know exactly what you want to ask
* be specific
* be polite
* check for answer again after composing the question
* use a meaningful subject line
* be patient

## Communicate
* communication is important (having good ideas won't matter if you can't communicate them)
* know what you want to say
* plan what you want to say (outline)
* ask yourself: does this get across what you're trying to say?

## Know your audience
* plan around your target audience
* make an appropriate pitch

## Choose your moment (don't pitch at a bad time)
* make your content relevant in time & content
* WISDOM
  1. ( W )hat do you want them to learn
  2. what is their ( I )nterest in what you've got to say?
  3. how ( S )ophisticated are they?
  4. how much ( D )etail do they want?
  5. Whom do you want to ( O )wn the information?
  6. how can you ( M )otivate them to listen to you?

## Choose a style
* ask what style is preferred
* communicate your needs

## Make it look good
* poor presentation can ruin a good idea
* learn to set page headers and footers
* check spelling (2 times)

## Involve your audience
* get feedback
* pick brains

## Be a Listener
* listen to people
* encourage people to talk by asking questions
* turn meetings into discussions

## Get back to people
* always respond to emails, voicemails, etc.
* even if it's just a "I'll get back to you later"

> It's both what you want to say and how you say it

# Chapter 2: A Pragrmatic Approach
* Index
  1. evils of duplication - don't duplicate knowledge
  2. orthogonality - don't split one piece of knowledge across multiple systems
  3. reversibility - insulate projects from changing environments
  4. tracer bullets - style of development that allows you to gather requirements, test, designs, implement code
  5. prototypes and post-it notes
  6. domain languages
  7. estimating

## Evils of Duplication
* collect, organize, maintain, harness knowledge
* knowledge is not stable
* instability leads to lots and lots of maintenance
* maintenance is a routine part of the development process
* the only way to develop software reliably: DRY - every piece of knowledge must have a single unambiguous source

> Do not repeat yourself

## How does duplication arise?
* imposed - duplication was "required"
* inadvertent - did not realize it was happening
* impatient - duplication was easier
* interdeveloper - multiple people duplicate a piece of information

## Imposed
* multiple representations of info
  1. simple filter or code generator
* documentation in code
  1. comments use for high level explanations
  2. comments become out of date and untrustworthy
  3. documentation falls behind code
  4. automate documenation updates
* language issues
  1. hard to work around
  2. use header files to document
  3. use implementation files to document nitt-gritty details

## Inadvertent Duplication
* can be subtle
* where possible always use accessor functions to read and write the attributes of objects

## Impatient Duplication
* "short cuts make for long delays"
* "discipline required to spend time up front to save pain later"

## Interdeveloper Duplication
* high level - have a clear design and strong technical leader and well understood division of labor
* solution - encourage active and frequent communication
* appoint a project librarian to facilitate the exchange of knowledge
* centralize routines and scripts
* read the docs

> Make it easy to reuse

## Orthogonality
* computing - "independence" or "decoupling"
* two ore more things are orthogonal if changes in one do not affect any of the others
* helicopter controls are not orthogonal
* benefits:
  1. design components are self-contained, independent, with single defined purpose
  2. increased productivity
  3. reduced risk
* gain productivity
  1. rduce development and testing time
  2. promotes reuse
  3. mathematically more efficient
* reduced risk
  1. diseased code isolated
  2. reduce fragility
  3. better tested
  4. not tied to platform or product
* project teams
  1. orthogonality reduces conflict

## Design
* cooperating modules
* layers of abstraction
  1. reduces runaway dependencies
* test - if you dramatically change the requirements behind a particular function, how many modules are affected? Should be one.
* don't rely on properties of things you can't control

## Toolkits and Libraries
* take care to preserve orthogonality as you introduce 3rd party toolkits/libraries
* when you bring in a toolkit as yourself if it breaks orthogonality (introduces changes that shouldn't be there)
* aspect-oriented programming (AOP)
  1. implement logging orthogonality to the thing being logged

## Coding
* keep code decoupled - write "shy" code
  1. modules that don't rely on other modules
  2. changes done by object
* avoid global data
* avoid similar functions

## Testing
* orthogonality -> easier testing
* module-level is easeir than integration testing
* difficulty of testing can indicate a lack of orthogonality
* bug fix: change one module or multiple? -> does fix cause other problems?

## Documentation
* orthogonality in documentation
* true orthogonal documentation can change apperance drastically and not effect content

## Living with Orthogonality
* closely related to DRY

## Reversibility
> There are no final decisions

## Flexible Architecture
* flexibility in architecture, deployment, and vendor integration
* keep decisions "soft"

## Tracer Bullets
* immediate feedback
* quick, visible, repeatable
*
