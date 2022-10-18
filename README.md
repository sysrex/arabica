# arabica



edit the celestia-node entrypoint for the docker conainter


```bash

#!/bin/bash

set -e

if [ "$1" != 'celestia' ]; then
    ./celestia "${NODE_TYPE}" init

    exec ./"$@" "--"
fi

exec ./"$@" "--"

```