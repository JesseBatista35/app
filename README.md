Skip to main content
Azure DevOps
projetos
/
Caixa
/
Pipelines
/
SISGF-frontend
/
15.0.0.50
Search


Caixa

Overview

Boards

Repos

Pipelines
Pipelines
Environments
Releases
Library
Task groups
Deployment groups
Portal Infra

Test Plans

Artifacts
Project settings

Jobs in run #15.0.0.50
Executando Build S2I Binary

View raw log

Uploading finished
build.build.openshift.io/sisgf-frontend-417 started
Adding cluster TLS certificate authority to trust store
Receiving source from STDIN as archive ...
failed to watch file "/var/log/pods/build-images-ads_sisgf-frontend-417-build_d0af0226-0f6f-4d84-96e6-bd0ec00eebbc/git-clone/0.log": no space left on deviceAdding cluster TLS certificate authority to trust store
Adding cluster TLS certificate authority to trust store
failed to watch file "/var/log/pods/build-images-ads_sisgf-frontend-417-build_d0af0226-0f6f-4d84-96e6-bd0ec00eebbc/sti-build/0.log": no space left on deviceF1123 11:27:54.788644   87576 helpers.go:119] error: The build build-images-ads/sisgf-frontend-417 status is "Failed"
##[error]Bash exited with code '255'.
##[warning]RetryHelper encountered task failure, will retry (attempt #: 1 out of 1) after 1000 ms
Generating script.
========================== Starting Command Output ===========================
/usr/bin/bash /opt/ads-agent/_work/_temp/16d77595-995b-42d4-a48d-79d669f32c40.sh
+ echo okd4_nprd
+ egrep -q '^(okd4|ocp)'
+ buildconfig=sisgf-frontend
+ oc start-build sisgf-frontend --from-dir=/opt/ads-agent/_work/11840/a --follow --wait=true -n build-images-ads -v=5
I1123 11:27:56.023975   87627 repository.go:424] Executing git show -s HEAD --format=%H%n%an%n%ae%n%cn%n%ce%n%B
I1123 11:27:56.025910   87627 repository.go:484] Error executing command: exit status 128
Uploading directory "/opt/ads-agent/_work/11840/a" as binary input for the build ...
I1123 11:27:56.026038   87627 tar.go:217] Adding "/opt/ads-agent/_work/11840/a" to tar ...
I1123 11:27:56.026337   87627 tar.go:312] Adding to tar: /opt/ads-agent/_work/11840/a/.s2i as .s2i
I1123 11:27:56.026861   87627 tar.go:312] Adding to tar: /opt/ads-agent/_work/11840/a/.s2i/bin as .s2i/bin
I1123 11:27:56.026993   87627 tar.go:312] Adding to tar: /opt/ads-agent/_work/11840/a/.s2i/bin/assemble as .s2i/bin/assemble
I1123 11:27:56.027093   87627 tar.go:312] Adding to tar: /opt/ads-agent/_work/11840/a/.s2i/bin/run as .s2i/bin/run
I1123 11:27:56.027243   87627 tar.go:312] Adding to tar: /opt/ads-agent/_work/11840/a/sisgf-frontend.zip as sisgf-frontend.zip

Uploading finished
I1123 11:27:57.462199   87627 helpers.go:201] server response object: [{
  "metadata": {},
  "status": "Failure",
  "message": "build sisgf-frontend-418 failed: BuildPodEvicted: Pod The node had condition: [DiskPressure]. ",
  "reason": "BadRequest",
  "code": 400
}]
F1123 11:27:57.462217   87627 helpers.go:119] Error from server (BadRequest): build sisgf-frontend-418 failed: BuildPodEvicted: Pod The node had condition: [DiskPressure]. 
##[error]Bash exited with code '255'.
Finishing: Executando Build S2I Binary
Row 2. Clickable
