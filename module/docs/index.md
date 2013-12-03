``parameters``: Custom config options
=====================================

The ``parameters`` module allows you to have custom configuration options your app can access via
``forge.config.modules.parameters.config``.

Use this module to pass data to your app at build-time so that your code can access that data at run-time. For example, you might use this to pass a "debug": true setting that causes more logging to be generated in a debug build:

	if (forge.config.modules.parameters.config.debug) {
		forge.logging.log("Extra logging when debug parameter is true");
	}

##Config options

Parameters
:	This should be a JSON object which contains the extra parameters you want to make available in your app. E.g.
	
		{
			{
				"myOption": "myData"
			}
		}

	You can then access this using `forge.config.modules.parameters.config.myOption`.
