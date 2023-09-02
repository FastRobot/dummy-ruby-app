# dummy-ruby-app
a simple bundle/rake driven ruby app for demo purposes

Buildkite runs `rake test` on any push. 

We expect the buildkite-demo repo's pipeline to clone and build this app, then run various rake tasks as proof. 

I started using rbenv because I was defaulting to a late ruby (3.0.6) but it was a PITA with the very ad-hoc agent I was using to run the jobs. Were I running the buildkite agent on its own docker host, I'd just use the image based build and not bother configuring the host each time. But as its a throwaway agent, I'm using an unprivileged docker container as an agent, running ubuntnu20.04 and not further containing each run/build. But the point is that this is a pretty typical ruby app with a bundle build and a rake interface.

