https://github.com/kolinrr/openshift-adv/settings/actions/runners/new?arch=x64&os=linux

# Create a folder
$ mkdir actions-runner && cd actions-runner
# Download the latest runner package
$ curl -o actions-runner-linux-x64-2.322.0.tar.gz -L https://github.com/actions/runner/releases/download/v2.322.0/actions-runner-linux-x64-2.322.0.tar.gz

# Optional: Validate the hash
$ echo "b13b784808359f31bc79b08a191f5f83757852957dd8fe3dbfcc38202ccf5768  actions-runner-linux-x64-2.322.0.tar.gz" | shasum -a 256 -c
# Extract the installer
$ tar xzf ./actions-runner-linux-x64-2.322.0.tar.gz

# Generate new Classic token

# Create the runner and start the configuration experience
$ ./config.sh --url https://github.com/YOUR-LOGIN-NAME/openshift-adv --token INSERT-YOUR-TOKEN

# Last step, run it!
$ ./run.sh