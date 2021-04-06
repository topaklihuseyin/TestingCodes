# CMS Jet Tuple production 2011 (performance optimized)
- Oracle virtual Box 6.1.16 for Windows and 
- CMS-OpenData-1.5.3 are used. For this example, instructions are explained at **[CMS Jet Tuple production 2011 (performance optimized)](https://github.com/cms-opendata-validation/2011-jet-inclusivecrosssection-ntupleproduction-optimized)**.  
````html
CMS Shell > cmsRun OpenDataTreeProducerOptimized_dataPAT_2011_cfg.py
````   
Number of events are fixed for 10000 events. The output is below  
````html
%MSG-w LocalFileSystem::initFSList():  (NoModuleName) 06-Apr-2021 07:15:14 GMT  pre-events
Cannot read '/etc/mtab': Invalid argument (error 22)
%MSG
06-Apr-2021 07:17:10 GMT  Initiating request to open file root://eospublic.cern.ch//eos/opendata/cms/Run2011A/Jet/AOD/12Oct2013-v1/20000/000D4260-D23E-E311-A850-02163E008D77.root
06-Apr-2021 07:17:13 GMT  Successfully opened file root://eospublic.cern.ch//eos/opendata/cms/Run2011A/Jet/AOD/12Oct2013-v1/20000/000D4260-D23E-E311-A850-02163E008D77.root
Begin processing the 1st record. Run 160578, Event 38142433, LumiSection 366 at 06-Apr-2021 07:17:33.579 GMT
Begin processing the 501st record. Run 160578, Event 39193217, LumiSection 376 at 06-Apr-2021 07:17:42.922 GMT
............................................................................................
Begin processing the 9001st record. Run 162822, Event 70883083, LumiSection 193 at 06-Apr-2021 07:20:31.956 GMT
Begin processing the 9501st record. Run 162822, Event 71541803, LumiSection 194 at 06-Apr-2021 07:20:41.803 GMT
06-Apr-2021 07:20:51 GMT  Closed file root://eospublic.cern.ch//eos/opendata/cms/Run2011A/Jet/AOD/12Oct2013-v1/20000/000D4260-D23E-E311-A850-02163E008D77.root

TrigReport ---------- Event  Summary ------------
TrigReport Events total = 10000 passed = 9408 failed = 592

......................................

TimeReport ---------- Module Summary ---[sec]----
TimeReport             per event        per module-run      per module-visit 
TimeReport        CPU       Real        CPU       Real        CPU       Real Name
TimeReport   0.000756   0.004267   0.000756   0.004267   0.000756   0.004267 goodOfflinePrimaryVertices
TimeReport   0.000066   0.000070   0.000066   0.000070   0.000066   0.000070 hltFilter

T---Report end!

=============================================

MessageLogger Summary

 type     category        sev    module        subroutine        count    total
 ---- -------------------- -- ---------------- ----------------  -----    -----
    1 fileAction           -s file_close                             1        1
    2 fileAction           -s file_open                              2        2

 type    category    Examples: run/evt        run/evt          run/evt
 ---- -------------------- ---------------- ---------------- ----------------
    1 fileAction           PostEndRun                        
    2 fileAction           pre-events       pre-events       

Severity    # Occurrences   Total Occurrences
--------    -------------   -----------------
System                  3                   3

````   
End of the run root file was generated. 

````html
cms-opendata cms-opendata 2.7M Apr  6 07:20 OpenDataTree_data.root
````


