# Testing Virtual Machine
Testing Virtual Machine and CMSSW 
- Oracle virtual Box 6.1.16 for Windows and 
- CMS-OpenData-1.5.3 downloaded. Then instructions on **[CMS 2011 Virtual Machines: How to install](http://opendata.cern.ch/docs/cms-virtual-machine-2011 )** is used. Every step works fine and finally use the **cmsRun** for 100 events. 
````html
CMS Shell > cmsRun demoanalyzer_cfg.py
````   
and counting the events 
````html
%MSG-w LocalFileSystem::initFSList():  (NoModuleName) 05-Apr-2021 12:50:19 GMT  pre-events
Cannot read '/etc/mtab': Invalid argument (error 22)
%MSG
05-Apr-2021 12:50:22 GMT  Initiating request to open file root://eospublic.cern.ch//eos/opendata/cms/Run2011A/ElectronHad/AOD/12Oct2013-v1/20001/001F9231-F141-E311-8F76-003048F00942.root
05-Apr-2021 12:50:25 GMT  Successfully opened file root://eospublic.cern.ch//eos/opendata/cms/Run2011A/ElectronHad/AOD/12Oct2013-v1/20001/001F9231-F141-E311-8F76-003048F00942.root
Begin processing the 1st record. Run 166782, Event 340184599, LumiSection 309 at 05-Apr-2021 12:50:40.539 GMT
Begin processing the 2nd record. Run 166782, Event 340185007, LumiSection 309 at 05-Apr-2021 12:50:40.540 GMT
Begin processing the 3rd record. Run 166782, Event 340187903, LumiSection 309 at 05-Apr-2021 12:50:40.540 GMT
Begin processing the 4th record. Run 166782, Event 340227487, LumiSection 309 at 05-Apr-2021 12:50:40.540 GMT
Begin processing the 5th record. Run 166782, Event 340210607, LumiSection 309 at 05-Apr-2021 12:50:40.541 GMT
Begin processing the 6th record. Run 166782, Event 340256207, LumiSection 309 at 05-Apr-2021 12:50:40.541 GMT
Begin processing the 7th record. Run 166782, Event 340165759, LumiSection 309 at 05-Apr-2021 12:50:40.541 GMT
Begin processing the 8th record. Run 166782, Event 340396487, LumiSection 309 at 05-Apr-2021 12:50:40.541 GMT



````   
