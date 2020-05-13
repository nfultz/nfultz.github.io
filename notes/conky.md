<!-- njnmdoc:  title="Conky"  -->
Conky is a lightweight but highly configurable system monitor app for linux.

It periodically outputs system usage data, typically to the desktop.

Global settings are set at the very beginning of the config file.

 <dl>

  <dt>update_interval<dt>

  <dd>How often to refresh</dd>

  <dt>output_to_console</dt>

  <dd>Write to stdout</dd>

</dl>

The output template gets filled in with data

[[conkyhttpd]] is a module that diverts conky's normal output to a web server.

Conky allows custom extensions through [[lua]] modules.

In the configuration section, you can load a module as well as set startup and shutdown callbacks:

    lua_load webconky.lua

    lua_startup_hook setup 5001

    lua_shutdown_hook cleanup


Then you can use lua functions in your template:

    ${lua sparkline}

