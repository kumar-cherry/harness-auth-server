# Harness Auth Server Overview

## Common Module Usage
harness-auth-common module contains auth server protocol case classes which can be used via dependency:
```
"com.actionml" %% "harness-auth-common" % <version>
```

## Using local build

If you want to build Harness with a locally built `harness-auth-server`, which is the typical case since there is no tar published yet, do the following.

```
bash$ ./make-auth-server-distribution.sh 
bash$ sbt harnessAuthCommon/publish-local
```

This will put harness dependencies in the local .ivy2 cache so when you build harness you will not get missing dependencies. Harness does not need to run with the harness-auth-server (when not using authentication) but does have dependencies on the client API supplied by this build.

