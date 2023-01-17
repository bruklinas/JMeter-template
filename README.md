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

### Running on a local machine
:exclamation: Make sure to disable all **Listeners** before executing the tests.

**Tests must be run be executing the following command in CLI**:  
> **jmeter -n -t {tests_file.jmx} -l {samples_report_filename.csv} -e -o {output_folder_name_for_HTML_report}**  
- -n - tells JMeter to run in non-GUI mode.  
- -t - specifies the path to source .jmx script to run.  
- -l - --logfile <argument> the file to log samples to  
- -e - generate report dashboard after load test  
- -o - --reportoutputfolder <argument> output folder for report dashboard  
 
 

## Extra notes
 
 In case you
 - need to use parameters or variables upfront - use **CSV data set configs**.
 - need to randomize/edit the request - use **Pre-processors**.
 - need to extract and store the result of the response - use **Post-processors**.
 - want to assert the response parameters - use **Assertions**.
 - want to add timeouts between requests, to imitate actual human-like UI flows - use **Timers**. 
