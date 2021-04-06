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
For Monte Carlo side 
````html
cmsRun OpenDataTreeProducerOptimized_mcPAT_2011_cfg.py
````
then output is below, i changed the message logger in _cfg.py file so every event seen in the screen. 

````html
...........................................................................
.......................................................................
Begin processing the 9105th record. Run 1, Event 3776547, LumiSection 11410 at 06-Apr-2021 08:00:50.154 GMT
Begin processing the 9106th record. Run 1, Event 3776548, LumiSection 11410 at 06-Apr-2021 08:00:50.159 GMT
Begin processing the 9107th record. Run 1, Event 3776549, LumiSection 11410 at 06-Apr-2021 08:00:50.165 GMT
Begin processing the 9108th record. Run 1, Event 3776550, LumiSection 11410 at 06-Apr-2021 08:00:50.172 GMT
Begin processing the 9109th record. Run 1, Event 3776551, LumiSection 11410 at 06-Apr-2021 08:00:50.176 GMT
06-Apr-2021 08:01:30 GMT  Closed file root://eospublic.cern.ch//eos/opendata/cms/MonteCarlo2011/Summer11LegDR/QCD_Pt-80to120_TuneZ2_7TeV_pythia6/AODSIM/PU_S13_START53_LV6-v1/00000/005D4394-1FB7-E311-91F4-002590593878.root

TrigReport ---------- Event  Summary ------------
TrigReport Events total = 10000 passed = 10000 failed = 0

TrigReport ---------- Path   Summary ------------
TrigReport  Trig Bit#        Run     Passed     Failed      Error Name
TrigReport     1    0      10000      10000          0          0 p

TrigReport -------End-Path   Summary ------------
TrigReport  Trig Bit#        Run     Passed     Failed      Error Name

TrigReport ---------- Modules in Path: p ------------
TrigReport  Trig Bit#    Visited     Passed     Failed      Error Name
TrigReport     1    0      10000      10000          0          0 goodOfflinePrimaryVertices
.......
TrigReport ---------- Module Summary ------------
TrigReport    Visited        Run     Passed     Failed      Error Name
TrigReport      10000      10000      10000          0          0 goodOfflinePrimaryVertices

TimeReport ---------- Event  Summary ---[sec]----
TimeReport CPU/event = 0.007931 Real/event = 0.042656

TimeReport ---------- Path   Summary ---[sec]----
TimeReport             per event          per path-run 
TimeReport        CPU       Real        CPU       Real Name


TimeReport -------End-Path   Summary ---[sec]----
TimeReport             per event       per endpath-run 
TimeReport        CPU       Real        CPU       Real Name


TimeReport ---------- Modules in Path: p ---[sec]----
TimeReport             per event      per module-visit 
TimeReport        CPU       Real        CPU       Real Name
TimeReport   0.001082   0.007029   0.001082   0.007029 goodOfflinePrimaryVertices
TimeReport   0.001026   0.009413   0.001026   0.009413 hltFilter

TimeReport ---------- Module Summary ---[sec]----
TimeReport             per event        per module-run      per module-visit 
TimeReport        CPU       Real        CPU       Real        CPU       Real Name
TimeReport   0.001082   0.007029   0.001082   0.007029   0.001082   0.007029 goodOfflinePrimaryVertices
TimeReport   0.001026   0.009413   0.001026   0.009413   0.001026   0.009413 hltFilter

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
end of the run root file generated.

````html
cms-opendata cms-opendata 2.8M Apr  6 08:01 OpenDataTree_mc.root
````
This example is working. 


