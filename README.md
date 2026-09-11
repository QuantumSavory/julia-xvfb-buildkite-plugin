# julia-xvfb-buildkite-plugin

This plugin makes all julia instances run in xvfb (useful when you need opengl on a headless server).

The hooks run only on Linux. Other platforms use the agent's Julia executable and native display.

Each job creates a temporary Julia wrapper and removes it in the exit hook. Each Julia invocation uses `xvfb-run -a` to select an available display and clean up its own Xvfb server when the command exits. The plugin does not overwrite a shared launcher or stop other jobs' processes.

## Example

TODO

## Options

TODO
