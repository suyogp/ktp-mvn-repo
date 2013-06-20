KTP Apps Artifact Repository
==============

##How to use this repository##
There's only two things to do:

resolvers += "ktpApps" at "https://github.com/KaplanTestPrep/ktp-mvn-repo/raw/releases/"

libraryDependencies += "name of your library"

##How to deploy in this repo##
Step 0) Clone this repository to your desired location (Ex. ~/repo)

<ol>
	<li> In the project you wish to publish, add the following lines to the build.sbt file or to the settings of the project:
		<pre><code>publishTo := Some(Resolver.file("file", new File("route/to/repo")) )</pre></code>
	</li>
	<li>Make sure your project version is up-to-date</li>
	<li>Execute the <code>publish</code> task in sbt. This will write all the artifacts in "route/to/repo"</li>
	<li>Navigate to "route/to/repo" and do a <code>git add .</code>, <code>git commit</code> and <code>git push</code>
</ol>
And that's it!
