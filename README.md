# JMeter-template

## Prerequisites

1. Make sure to have all the following plugins installed:
- Plugins manager: https://jmeter-plugins.org/wiki/PluginsManager/
- Custom thread groups: https://jmeter-plugins.org/wiki/ConcurrencyThreadGroup/
- 3 basic graphs: https://jmeter-plugins.org/wiki/ResponseTimesOverTime/
- Throughput Shaping Timer: https://jmeter-plugins.org/wiki/ThroughputShapingTimer/
- Dummy Sampler: https://jmeter-plugins.org/wiki/DummySampler/
2. Environment variables must be edited to have `{JMeter folder}/bin` added to the `PATH`.

## Running the tests

:exclamation::exclamation::exclamation: GUI should be used only for setting up and debugging tests :exclamation::exclamation::exclamation: 

 Tests **must be executed using via CLI** using the following command:  
> **jmeter -n -t {tests_file.jmx} -l {samples_report_filename.csv} -e -o output**  
- -n - tells JMeter to run in non-GUI mode.  
- -t - specifies the path to source .jmx script to run.  
- -l - --logfile <argument> the file to log samples to  
- -e - generate report dashboard after load test  
- -o - --reportoutputfolder <argument> output folder for report dashboard  

