# Synthetic-CMS-Minimum-Data-Set-MDS-dataset-with-all-codes-and-decodes
    Synthetic CMS Minimum Data Set(MDS) dataset with all codes and decodes                                                                                         
                                                                                                                                                                   
    The Minimum Data Set (MDS) is part of a federally mandated process for clinical assessment                                                                     
    of all residents in Medicare or Medicaid certified nursing homes. This process entails a                                                                       
    comprehensive, standardized assessment of each resident's functional capabilities and                                                                          
    health needs. Assessments are conducted by trained nursing home clinicians                                                                                     
    on all patients at admission and discharge,                                                                                                                    
     in addition to other time intervals (e.g., quarterly, annually, and when                                                                                      
    residents experience a significant change in status).                                                                                                          
                                                                                                                                                                   
    GitHub                                                                                                                                                         
    https://tinyurl.com/exueaav4                                                                                                                                   
    https://github.com/rogerjdeangelis/Synthetic-CMS-Minimum-Data-Set-MDS-dataset-with-all-codes-and-decodes                                                       
                                                                                                                                                                   
    Tools ( utl_b64decode here and on end of this message )                                                                                                        
    https://tinyurl.com/n8bea8tx                                                                                                                                   
    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories                                                                     
                                                                                                                                                                   
    macro utl_b64decode on end of this readme                                                                                                                      
                                                                                                                                                                   
      This work was done entirely without access to any CMS MDS data. I used published                                                                             
      meta data and some publications.  If the meta data is correct the MDS table should                                                                           
      be correct. Use at your own risk. Documentation is in the PDF and XLS folders.                                                                               
                                                                                                                                                                   
      The synthetic MDS can be used to develop programs.                                                                                                           
      The meta data can make it easy to add the decodes to real MDS data.                                                                                          
                                                                                                                                                                   
      I am moving more and more processing to R and Python. Some of the                                                                                            
      output below are in stata datasets. Stata data structures seem the closest to SAS datasets.                                                                  
      You will need to use SAS 'Proc import' to convert some output to SAS tables.                                                                                 
      R and Python can deal directly with the STATA data,                                                                                                          
                                                                                                                                                                   
      OUTPUT;                                                                                                                                                      
                                                                                                                                                                   
         1. Format catalog with all 634 MDS formats;                                                                                                               
                                                                                                                                                                   
         2. MDS Meta data used to create synthetic MDS file                                                                                                        
                                                                                                                                                                   
         3. A Synthetic MDS datasets in a Stata dataset and SAS table.                                                                                             
            Table has 1,466 columns, 831 original variables and 635 decodes (created from format catalog)                                                          
            The synthetic dataset has 32 observations but covers                                                                                                   
            at least one copy of the decodes.                                                                                                                      
                                                                                                                                                                   
            if the code variable was A1200_MRTL_STUS_CD                                                                                                            
            Then decode variable is A1200_MRTL_STUS                                                                                                                
                                                                                                                                                                   
            I drop the suffix, _CD, _NUM, _SW and _IND for the decoded variables.                                                                                  
            The format name in the catalog is the same as the full variable name.                                                                                  
                                                                                                                                                                   
         Example (Frequency analysis of Marital Status Scores)                                                                                                     
                                                                                                                                                                   
         proc freq data=syn;                                                                                                                                       
            tables A1200_MRTL_STUS_CD*A1200_MRTL_STUS / list;                                                                                                      
         run;quit;                                                                                                                                                 
                                                                                                                                                                   
         The FREQ Procedure                                                                                                                                        
                                                                                                                                                                   
         A1200_MRTL_  (note no CD suffix)                                                                                                                          
         STUS_CD      A1200_MRTL_STUS               Frequency                                                                                                      
         ------------------------------------------------------                                                                                                    
         -            - Not assessed/no information        4                                                                                                       
         1            1 Never married                      4                                                                                                       
         2            2 Married                            4                                                                                                       
         3            3 Widowed                            4                                                                                                       
         4            4 Separated                          4                                                                                                       
         5            5 Divorced                           4                                                                                                       
     any value not    UNKNOWN                              9   * catchall for any value not above                                                                  
       above                                                                                                                                                       
    /*                                                                                                                                                             
     _     _____                          _                                                                                                                        
    / |   |  ___|__  _ __ _ __ ___   __ _| |_ ___                                                                                                                  
    | |   | |_ / _ \| `__| `_ ` _ \ / _` | __/ __|                                                                                                                 
    | |_  |  _| (_) | |  | | | | | | (_| | |_\__ \                                                                                                                 
    |_(_) |_|  \___/|_|  |_| |_| |_|\__,_|\__|___/                                                                                                                 
                                                                                                                                                                   
    */                                                                                                                                                             
                                                                                                                                                                   
    1. Note GitHub does not support binary downloads, so                                                                                                           
       I have encoded the V5 transport file with base64 encoding(text).                                                                                            
       You may be able to clone the repo on your desktop and use the binary version directly.                                                                      
    /*                   _                                                                                                                                         
    (_)_ __  _ __  _   _| |_ ___                                                                                                                                   
    | | `_ \| `_ \| | | | __/ __|                                                                                                                                  
    | | | | | |_) | |_| | |_\__ \                                                                                                                                  
    |_|_| |_| .__/ \__,_|\__|___/                                                                                                                                  
            |_|                                                                                                                                                    
    */                                                                                                                                                             
        BASE 64 TEXT VERSION                                                                                                                                       
                                                                                                                                                                   
        You can programatically download the base64 encoded(text) file                                                                                             
                                                                                                                                                                   
        https://tinyurl.com/3t263zma file                                                                                                                          
        https://raw.githubusercontent.com/rogerjdeangelis/Synthetic-CMS-Minimum-Data-Set-MDS-dataset-with-all-codes-and-decodes/main/cntlin.b64                    
                                                                                                                                                                   
        BINARY VERSION (GitHub does not support programmatic downloads of binary data);                                                                            
        https://tinyurl.com/pa6exe34                                                                                                                               
        https://github.com/rogerjdeangelis/Synthetic-CMS-Minimum-Data-Set-MDS-dataset-with-all-codes-and-decodes/blob/main/ctlin.xpt                               
    /*                                                                                                                                                             
     _ __  _ __ ___   ___ ___  ___ ___                                                                                                                             
    | `_ \| `__/ _ \ / __/ _ \/ __/ __|                                                                                                                            
    | |_) | | | (_) | (_|  __/\__ \__ \                                                                                                                            
    | .__/|_|  \___/ \___\___||___/___/                                                                                                                            
    |_|                                                                                                                                                            
                                                                                                                                                                   
     a. Delete previous run outputs in SAS work folder if they exist, so your reruns do not use previous tables                                                    
     b. Programmatically download the Base64 encoded binary V5 xport file from GitHub with the cntlin table for proc fromat                                        
     c. Decode the BASE64(text) into a SAS V5 xport file                                                                                                           
     d. Use proc format to convert the V5 xport file to a SAS format a catalog with the 634 formats. Result is in work.formats.                                    
    */                                                                                                                                                             
                                                                                                                                                                   
        * BASE 64 VERSION;                                                                                                                                         
                                                                                                                                                                   
        * store all results in the SAS work folder;                                                                                                                
        %let _w=%sysfunc(pathname(work));                                                                                                                          
        %put &_w;                                                                                                                                                  
                                                                                                                                                                   
        * f:\wrk\_TDZTAGFS_1110_;                                                                                                                                  
                                                                                                                                                                   
        * incase you rerun;                                                                                                                                        
        %utlfkil(&_w/meta_dta.b64);                                                                                                                                
        %utlfkil(&_w\meta.dta);                                                                                                                                    
        %utlfkil(&_w/cntlin.xpt);  * delete the decoded version if you rerun;                                                                                      
                                                                                                                                                                   
        proc datasets lib=work nolist;                                                                                                                             
         delete meta;                                                                                                                                              
        run;quit;                                                                                                                                                  
        * dounload the BASE64 text file containg the V5 xport file;                                                                                                
        filename _bcot "&_w/cntlin.b64";                                                                                                                           
        proc http                                                                                                                                                  
           method='get'                                                                                                                                            
           url="https://tinyurl.com/3t263zma"                                                                                                                      
           out= _bcot;                                                                                                                                             
        run;quit;                                                                                                                                                  
                                                                                                                                                                   
        /*                                                                                                                                                         
        LOG                                                                                                                                                        
                                                                                                                                                                   
        NOTE: PROCEDURE HTTP used (Total process time)                                                                                                             
              real time           0.56 seconds                                                                                                                     
              user cpu time       0.01 seconds                                                                                                                     
        */                                                                                                                                                         
                                                                                                                                                                   
        * convert the base64 text file to a binary xpt file(macro on end of this readme);                                                                          
        %utl_b64decode(&_w/cntlin.b64,&_w/cntlin.xpt);                                                                                                             
                                                                                                                                                                   
        * create format catalog with 634 formats;                                                                                                                  
        libname xpt xport "&_w/cntlin.xpt";                                                                                                                        
        proc format cntlin=xpt.cntlin;                                                                                                                             
        run;quit;                                                                                                                                                  
        libname xpt clear                                                                                                                                          
                                                                                                                                                                   
    /*           _               _                                                                                                                                 
      ___  _   _| |_ _ __  _   _| |_                                                                                                                               
     / _ \| | | | __| `_ \| | | | __|                                                                                                                              
    | (_) | |_| | |_| |_) | |_| | |_                                                                                                                               
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                                                                              
                    |_|                                                                                                                                            
    */                                                                                                                                                             
        /* 634 formats  in WORK.FORMATS                                                                                                                            
        LOG                                                                                                                                                        
                                                                                                                                                                   
        NOTE: The infile "f:\wrk\_TD16908_T7610_/cntlin.b64" is:                                                                                                   
              Filename=f:\wrk\_TD16908_T7610_\cntlin.b64,                                                                                                          
              RECFM=V,LRECL=76,File Size (bytes)=1498878,                                                                                                          
                                                                                                                                                                   
        NOTE: The file "f:\wrk\_TD16908_T7610_/cntlin.xpt" is:                                                                                                     
              Filename=f:\wrk\_TD16908_T7610_\cntlin.xpt,                                                                                                          
              RECFM=F,LRECL=1,File Size (bytes)=0,                                                                                                                 
                                                                                                                                                                   
        NOTE: Detected Base64 Line Length of 76                                                                                                                    
        NOTE: 19217 records were read from the infile "f:\wrk\_TD16908_T7610_/cntlin.b64".                                                                         
              The minimum record length was 28.                                                                                                                    
              The maximum record length was 76.                                                                                                                    
        NOTE: 1095333 records were written to the file "f:\wrk\_TD16908_T7610_/cntlin.xpt".                                                                        
        NOTE: DATA statement used (Total process time):                                                                                                            
                                                                                                                                                                   
        4456   proc format cntlin=xpt.cntlin;                                                                                                                      
        NOTE: Format $A0050_TRANS_TYPE_CD has been output.                                                                                                         
        NOTE: Format $A0200_PRVDR_TYPE_CD is already on the library WORK.FORMATS.                                                                                  
        ... (635 formats)                                                                                                                                          
                                                                                                                                                                   
        NOTE: Format $Z0200C_STATE_SS_IND has been output.                                                                                                         
                                                                                                                                                                   
        ONE OF THE 634                                                                                                                                             
        ----------------------------------------------------------------------------                                                                               
        |               FORMAT NAME: $A1200_MRTL_STUS_CD LENGTH: 29                |                                                                               
        |   MIN LENGTH:   1  MAX LENGTH:  40  DEFAULT LENGTH:  29  FUZZ:        0  |                                                                               
        |--------------------------------------------------------------------------|                                                                               
        |START           |END             |LABEL                                   |                                                                               
        |----------------+----------------+----------------------------------------|                                                                               
        |-               |-               |- Not assessed/no information           |                                                                               
        |1               |1               |1 Never married                         |                                                                               
        |2               |2               |2 Married                               |                                                                               
        |3               |3               |3 Widowed                               |                                                                               
        |4               |4               |4 Separated                             |                                                                               
        |5               |5               |5 Divorced                              |                                                                               
        |**OTHER**       |**OTHER**       |UNKNOWN                                 |                                                                               
        ----------------------------------------------------------------------------                                                                               
                                                                                                                                                                   
       */                                                                                                                                                          
                                                                                                                                                                   
    /*___                     _              _       _                                                                                                             
    |___ \     _ __ ___   ___| |_ __ _    __| | __ _| |_ __ _                                                                                                      
      __) |   | `_ ` _ \ / _ \ __/ _` |  / _` |/ _` | __/ _` |                                                                                                     
     / __/ _  | | | | | |  __/ || (_| | | (_| | (_| | || (_| |                                                                                                     
    |_____(_) |_| |_| |_|\___|\__\__,_|  \__,_|\__,_|\__\__,_|                                                                                                     
     _                   _                                                                                                                                         
    (_)_ __  _ __  _   _| |_ ___                                                                                                                                   
    | | `_ \| `_ \| | | | __/ __|                                                                                                                                  
    | | | | | |_) | |_| | |_\__ \                                                                                                                                  
    |_|_| |_| .__/ \__,_|\__|___/                                                                                                                                  
            |_|                                                                                                                                                    
    */                                                                                                                                                             
    BASE 64 TEXT VERSION OF META DATA                                                                                                                              
                                                                                                                                                                   
    https://tinyurl.com/ywekapde                                                                                                                                   
    https://raw.githubusercontent.com/rogerjdeangelis/Synthetic-CMS-Minimum-Data-Set-MDS-dataset-with-all-codes-and-decodes/main/meta_dta.b64                      
                                                                                                                                                                   
    BINARY META DATA                                                                                                                                               
    https://tinyurl.com/ecrmydre                                                                                                                                   
    https://github.com/rogerjdeangelis/Synthetic-CMS-Minimum-Data-Set-MDS-dataset-with-all-codes-and-decodes/blob/main/meta.dta                                    
    /*                                                                                                                                                             
     _ __  _ __ ___   ___ ___  ___ ___                                                                                                                             
    | `_ \| `__/ _ \ / __/ _ \/ __/ __|                                                                                                                            
    | |_) | | | (_) | (_|  __/\__ \__ \                                                                                                                            
    | .__/|_|  \___/ \___\___||___/___/                                                                                                                            
    |_|                                                                                                                                                            
                                                                                                                                                                   
     a. Delete previous run outputs in SAS work folder if they exist, so your reruns do not use previous tables                                                    
     b. Programmatically download the Base64 encoded binary meta data saved in a STATA table.                                                                      
     c. Decode the BASE64(text) into a STATA table.                                                                                                                
     d. Use proc import to convert the STATA table to SAS table.                                                                                                   
    */                                                                                                                                                             
                                                                                                                                                                   
    * BASE 64 PROCESSING;                                                                                                                                          
                                                                                                                                                                   
    * work folder;                                                                                                                                                 
    %let _w=%sysfunc(pathname(work));                                                                                                                              
    %put &_w;                                                                                                                                                      
                                                                                                                                                                   
    * incase you rerun;                                                                                                                                            
    %utlfkil(&_w\meta_dta.b64);                                                                                                                                    
    %utlfkil(&_w\meta.dta);                                                                                                                                        
                                                                                                                                                                   
    proc datasets lib=work nolist;                                                                                                                                 
     delete meta;                                                                                                                                                  
    run;quit;                                                                                                                                                      
                                                                                                                                                                   
    * download base64 text file with meta data in a STATA table;                                                                                                   
    filename _bcot "&_w/meta_dta.b64";                                                                                                                             
    proc http                                                                                                                                                      
       method='get'                                                                                                                                                
       url="https://tinyurl.com/ywekapde"                                                                                                                          
       out= _bcot;                                                                                                                                                 
    run;quit;                                                                                                                                                      
                                                                                                                                                                   
    * decode into STATA table.;                                                                                                                                    
    %utl_b64decode(&_w\meta_dta.b64,&_w\meta.dta);                                                                                                                 
                                                                                                                                                                   
    * convert STATA table to SAS table;                                                                                                                            
                                                                                                                                                                   
    proc import out=meta file="&_w\meta.dta" replace;                                                                                                              
    ;run;quit;                                                                                                                                                     
                                                                                                                                                                   
    /*           _               _                                                                                                                                 
      ___  _   _| |_ _ __  _   _| |_                                                                                                                               
     / _ \| | | | __| `_ \| | | | __|                                                                                                                              
    | (_) | |_| | |_| |_) | |_| | |_                                                                                                                               
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                                                                              
                    |_|                                                                                                                                            
    */                                                                                                                                                             
                                                                                                                                                                   
    /*                                                                                                                                                             
    Only questions relating to MDS is enclosed. I do not have access                                                                                               
    to MDS. The synthetic data was created from published meta data and                                                                                            
    common sense?                                                                                                                                                  
                                                                                                                                                                   
    Teradata and Exadata use meta data to optimize program execution.                                                                                              
    With this meta data along with my Verification and Validation Macro you can                                                                                    
    outperform Exadata and Teradata when running from a inexpensive $800 Dell                                                                                      
    T7610 with 32 logical 3.4gz processors, dual 1 TB NVMe Drives and 128gb ram.                                                                                   
                                                                                                                                                                   
    Data Set Name        WORK.META   Observations          8,167,333                                                                                               
    Member Type          DATA        Variables             8                                                                                                       
    Engine               V9          Indexes               0                                                                                                       
                                                                                                                                                                   
    # Variable    Type Len Format Informat Label                                                                                                                   
                                                                                                                                                                   
    1 CONTEXT     Char   3 $3.    $3.      Datastore ie USRDS, CCW, ACS, CENSUS CCW_Oracle IDR_Teradata, SPSS, STATA..                                             
    2 SCHEMA      Char   3 $3.    $3.      Path, Relational Schema, Libname, Connection information                                                                
    3 TABLE       Char   9 $9.    $9.      Object Name level 1 usually a Table or  SAS                                                                             
                                           dataset but can format name, oracle table, SPSS, STATA ....                                                             
    4 VARIABLE    Char  30 $30.   $30.     Object name level 2 usually a variable but can be a code                                                                
                                           if Level 1 object name is a Format and question is Lookup                                                               
    5 QUESTION    Char  15 $15.   $15.                                                                                                                             
           TOP30FRQ BOT30FRQ MAX_MIN MEAN MISS_COUNT PCT_MISS STD Q1_Q3 INDEX PRIMARY_KEY                                                                          
           COUNT_DISTINCT TOT10 BOT10 OUTLIERS10 PSUEDO_CODE CODE_DECODE COMPRESS CRDATE                                                                           
           DATAREP DATAREPNAME DELOBS DESCRIPTION ENCODING ENCRYPT FILES FILESIZE FORMAT                                                                           
           FORMAT_TYPE INFORMAT LABEL LENGTH LIBNAME LOCATION MAXGEN MEMTYPE MODATE NLOBS                                                                          
           NOBS NOTES NOTNULL NPAGE NPOS NUM_CHARACTER NUM_NUMERIC NVAR OBSLEN PRECISION                                                                           
           REUSE SORTEDBY SOURCE TRANSCODE TYPE TYPELENGTH TYPEMEM CODEBOOK COMMENT                                                                                
           COMMENTS DESCRIPTION LONG_NAME SKEWNESS                                                                                                                 
                                                                                                                                                                   
    6 SUBCLASS    Char  12 $12.   $12.     Usually a classification variable for a crosstab with variable(Race)                                                    
                                           only applies to analysis data store                                                                                     
    7 SUBCLASSVAL Char  15 $15.   $15.     Usually classification value "Black"  for subclass(Race), if variable Gender                                            
                                           and subclass Race answer could be count of Black Males                                                                  
    8 ANSWER      Char 807 $807.  $16000.  ANSWER                                                                                                                  
                                                                                                                                                                   
                                                                                                                                                                   
     WORK.META total obs=6,649                                                                                                                                     
                                                                                                                                                                   
     Obs CONTEXT    SCHEMA      TABLE      VARIABLE                  QUESTION             SUBCLASS        SUBCLASSVAL                                              
                                                                                                                                                                   
       1   MDS       MDS      **TABLE**    **VARIABLE**              MDS_PATH           **SUBCLASS**    **SUBCLASSVAL**                                            
       2   MDS       MDS      MDS_2022     A0050_TRANS_TYPE_CD       COMMENTS           **SUBCLASS**    **SUBCLASSVAL**                                            
                                                                                                                                                                   
       3   MDS       MDS      MDS_2022     A0050_TRANS_TYPE_CD       MDS_CODE_DECODE    **SUBCLASS**    **SUBCLASSVAL**                                            
                                                                                                                                                                   
       4   MDS       MDS      MDS_2022     A0050_TRANS_TYPE_CD       MDS_DESCRIPTION    **SUBCLASS**    **SUBCLASSVAL**                                            
       5   MDS       MDS      MDS_2022     A0050_TRANS_TYPE_CD       MDS_LABEL          **SUBCLASS**    **SUBCLASSVAL**                                            
       6   MDS       MDS      MDS_2022     A0050_TRANS_TYPE_CD       MDS_LENGTH         **SUBCLASS**    **SUBCLASSVAL**                                            
       7   MDS       MDS      MDS_2022     A0050_TRANS_TYPE_CD       MDS_LONG_NAME      **SUBCLASS**    **SUBCLASSVAL**                                            
       8   MDS       MDS      MDS_2022     A0050_TRANS_TYPE_CD       MDS_SEQUENCE       **SUBCLASS**    **SUBCLASSVAL**                                            
       9   MDS       MDS      MDS_2022     A0050_TRANS_TYPE_CD       MDS_TYPE           **SUBCLASS**    **SUBCLASSVAL**                                            
                                                                                                                                                                   
     Obs ANSWER                                                                                                                                                    
                                                                                                                                                                   
       1 d:/rnl1                                                                                                                                                   
       2 replaced X0100 4/1/2012                                                                                                                                   
                                                                                                                                                                   
         ** NOTE YOU CAN BUILD THE 634 FORMATS EASILY FROM #3. NOTE THE '~' SEPARATOR **                                                                           
                                                                                                                                                                   
       3 1=Add a new record~2= Modify existing record~3=Inactivate existing record~^=Blank(skip pattern)                                                           
       4 This column identifies the type of record submitted.                                                                                                      
       5 A0050 Type of Record Code                                                                                                                                 
       6 1                                                                                                                                                         
       7 A0050_TRANS_TYPE_CD                                                                                                                                       
       8 50                                                                                                                                                        
       9 CHAR                                                                                                                                                      
                                                                                                                                                                   
    /*____    ____              _   _          _   _                      _                                                                                        
    |___ /   / ___| _   _ _ __ | |_| |__   ___| |_(_) ___   _ __ ___   __| |___                                                                                    
      |_ \   \___ \| | | | `_ \| __| `_ \ / _ \ __| |/ __| | `_ ` _ \ / _` / __|                                                                                   
     ___) |   ___) | |_| | | | | |_| | | |  __/ |_| | (__  | | | | | | (_| \__ \                                                                                   
    |____(_) |____/ \__, |_| |_|\__|_| |_|\___|\__|_|\___| |_| |_| |_|\__,_|___/                                                                                   
                    |___/                                                                                                                                          
     _                   _                                                                                                                                         
    (_)_ __  _ __  _   _| |_                                                                                                                                       
    | | `_ \| `_ \| | | | __|                                                                                                                                      
    | | | | | |_) | |_| | |_                                                                                                                                       
    |_|_| |_| .__/ \__,_|\__|                                                                                                                                      
            |_|                                                                                                                                                    
    */                                                                                                                                                             
                                                                                                                                                                   
    BAS64 TEXT VERSION                                                                                                                                             
    https://tinyurl.com/dapdd532                                                                                                                                   
    https://raw.githubusercontent.com/rogerjdeangelis/Synthetic-CMS-Minimum-Data-Set-MDS-dataset-with-all-codes-and-decodes/main/syn_dta.b64                       
                                                                                                                                                                   
    BINARY VERSION                                                                                                                                                 
    https://tinyurl.com/zepkzf4                                                                                                                                    
    https://github.com/rogerjdeangelis/Synthetic-CMS-Minimum-Data-Set-MDS-dataset-with-all-codes-and-decodes/blob/main/syn.dta                                     
    /*                                                                                                                                                             
     _ __  _ __ ___   ___ ___  ___ ___                                                                                                                             
    | `_ \| `__/ _ \ / __/ _ \/ __/ __|                                                                                                                            
    | |_) | | | (_) | (_|  __/\__ \__ \                                                                                                                            
    | .__/|_|  \___/ \___\___||___/___/                                                                                                                            
    |_|                                                                                                                                                            
                                                                                                                                                                   
     a. Delete previous run outputs in SAS work folder if they exist, so your reruns do not use previous tables                                                    
     b. Programatically download the Base64 encoded binary synthetic MDS data saved in a STATA table.                                                              
     c. Decode the BASE64(text) into a STATA table.                                                                                                                
     d. Use proc import to convert the STATA table to SAS table.                                                                                                   
     e. SAS does not seem to honor the variable lengths so go back to the meta data and use type from meta data.                                                   
     f. Remove formats an informats. I try to avoid ataching formats sttached to variables                                                                         
        because SAS uses the formats inconsistently                                                                                                                
        in various procs. Also the FDA requires decodes in the data.                                                                                               
    */                                                                                                                                                             
                                                                                                                                                                   
    * work folder;                                                                                                                                                 
    %let _w=%sysfunc(pathname(work));                                                                                                                              
    %put &_w;                                                                                                                                                      
                                                                                                                                                                   
    * incase you rerun;                                                                                                                                            
    %utlfkil(&_w\syn_dta.b64);                                                                                                                                     
    %utlfkil(&_w\syn.dta);                                                                                                                                         
                                                                                                                                                                   
    proc datasets lib=work nolist;                                                                                                                                 
     delete syn;                                                                                                                                                   
    run;quit;                                                                                                                                                      
                                                                                                                                                                   
    * download from GitHub.                                                                                                                                        
    filename _bcot "&_w/syn_dta.b64";                                                                                                                              
    proc http                                                                                                                                                      
       method='get'                                                                                                                                                
       url="https://tinyurl.com/dapdd532"                                                                                                                          
       out= _bcot;                                                                                                                                                 
    run;quit;                                                                                                                                                      
                                                                                                                                                                   
    * convert to STATA table;                                                                                                                                      
    %utl_b64decode(&_w\syn_dta.b64,&_w\syn.dta);                                                                                                                   
                                                                                                                                                                   
    * convert to SAS table;                                                                                                                                        
    proc import out=syndta file="&_w\syn.dta" replace;                                                                                                             
    ;run;quit;                                                                                                                                                     
                                                                                                                                                                   
    * adjust lengths to agree with meta data;                                                                                                                      
    * get type and length from meta data;                                                                                                                          
    proc sql;                                                                                                                                                      
      create                                                                                                                                                       
        table                                                                                                                                                      
          mtaTypLen as                                                                                                                                             
        select                                                                                                                                                     
           distinct                                                                                                                                                
             variable                                                                                                                                              
            ,question                                                                                                                                              
            ,answer                                                                                                                                                
       from                                                                                                                                                        
          meta /* create above */                                                                                                                                  
       where                                                                                                                                                       
          strip(question) in ("MDS_TYPE", "MDS_LENGTH")                                                                                                            
       order                                                                                                                                                       
          by variable, question                                                                                                                                    
    ;quit;                                                                                                                                                         
                                                                                                                                                                   
    /*                                                                                                                                                             
    Up to 40 obs MDX.MDX_100SYNMKEVARNAM total obs=1,662                                                                                                           
                                                                                                                                                                   
     Obs    VARIABLE                           QUESTION      ANSWER                                                                                                
                                                                                                                                                                   
       1    A0050_TRANS_TYPE_CD               MDS_LENGTH    1                                                                                                      
       2    A0050_TRANS_TYPE_CD               MDS_TYPE      CHAR                                                                                                   
       3    A0100A_NPI_NUM                    MDS_LENGTH    10                                                                                                     
       4    A0100A_NPI_NUM                    MDS_TYPE      CHAR                                                                                                   
    */                                                                                                                                                             
                                                                                                                                                                   
    * put type an length on each observation;                                                                                                                      
    proc transpose data=mtaTypLen out=NamXpo(drop=_name_);                                                                                                         
     by variable notsorted;                                                                                                                                        
    id question;                                                                                                                                                   
    var answer;                                                                                                                                                    
    run;quit;                                                                                                                                                      
                                                                                                                                                                   
    * create program to adjust lengths to match meta data;                                                                                                         
    data _null_;                                                                                                                                                   
     set NamXpo end=dne;                                                                                                                                           
     file "&_w/ats.txt";                                                                                                                                           
     if _n_=1 then put "data syn;attrib" /;                                                                                                                        
     select (mds_type);                                                                                                                                            
        when ('CHAR') cmd=catx(" ",variable,cats("length=",'$',mds_length));                                                                                       
        when ('NUM',"DATE") cmd=catx(" ",variable,cats("length=8"));                                                                                               
        otherwise;                                                                                                                                                 
     end;                                                                                                                                                          
     put cmd;                                                                                                                                                      
     if dne then put ";set syn;run;quit;";                                                                                                                         
    run;quit;                                                                                                                                                      
                                                                                                                                                                   
    * run program created above;                                                                                                                                   
    %inc "&_w/ats.txt";                                                                                                                                            
                                                                                                                                                                   
    * remove formats and inform\ats;                                                                                                                               
    proc datasets lib=work;                                                                                                                                        
     modify syn;                                                                                                                                                   
     format _all_;                                                                                                                                                 
     informat _all_ ;                                                                                                                                              
    run;quit;                                                                                                                                                      
                                                                                                                                                                   
    /*           _               _                                                                                                                                 
      ___  _   _| |_ _ __  _   _| |_                                                                                                                               
     / _ \| | | | __| `_ \| | | | __|                                                                                                                              
    | (_) | |_| | |_| |_) | |_| | |_                                                                                                                               
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                                                                              
                    |_|                                                                                                                                            
    */                                                                                                                                                             
                                                                                                                                                                   
    Data Set Name   WORK.SYN     Observations          32                                                                                                          
    Member Type     DATA         Variables             1466                                                                                                        
                                                                                                                                                                   
                                                                                                                                                                   
    Middle Observation(16 ) of syn - Total Obs 32                                                                                                                  
                                                                                                                                                                   
                                                                                                                                                                   
     -- CHARACTER --                                                                                                                                               
    A0050_TRANS_TYPE_CD              C    1       @                   A0050 Type of Record Code                                                                    
    A0100A_NPI_NUM                   C    10      1113281199          A0100A Facility National Provider Identifier (NPI)                                           
    A0100B_CMS_CRTFCTN_NUM           C    12      115163              A0100B Facility CMS Certification Number (CCN)                                               
    A0100C_STATE_PRVDR_NUM           C    15      111116999           A0100C State Provider Number                                                                 
    A0200_PRVDR_TYPE_CD              C    1       @                   A0200 Type of Provider                                                                       
    A0300A_STATE_PYMT_PRPSE_CD       C    1       @                   A0300A State Payment Assessment Purpose Code                                                 
    A0300B_STATE_PYMT_ASMT_TYPE_CD   C    1       5                   A0300B State Payment Assessment Type Code                                                    
    ...                                                                                                                                                            
    C0200_WORD_RPET_FIRST_ATMPT      C    29      3 Three             C0200 BIMS: Number of Words Repeated After First Attempt                                     
    C0300A_RPT_CRCT_YR               C    34      3 Correct           C0300A BIMS: Temporal Orientation - Able to Report Correct Year                              
    MDS_ITM_SBST                     C    51      NP Nursing Home     Item Subset Code (ISC)                                                                       
    ...                                                                                                                                                            
                                                                                                                                                                   
    -- NUMERIC --                                                                                                                                                  
    0900_BIRTH_DT                   N    8       -4383               A0900 Birth Date                                                                              
    1600_ENTRY_DT                   N    8       3998                A1600 Entry Date                                                                              
    1900_ADMSN_DT                   N    8       14561               A1900 Admission Date                                                                          
    2300_ASMT_RFRNC_DT              N    8       14622               A2300 Assessment Reference Date                                                               
    RCTN_NUM                        N    8       2200102             Correction Number                                                                             
    AC_PRVDR_INTRNL_ID              N    8       1234567890          Facility/Provider Internal ID                                                                 
    DS_ASMT_ID                      N    8       872327845           Encrypted MDS Assessment Internal                                                             
    J0400_PAIN_FREQ                 C    29      4 Rarely            J0400 Pain Assessment Interview: Pain Frequency Code                                          
                                                                                                                                                                   
                                                                                                                                                                   
    /*      __   _  _                                                                                                                                              
    | |__  / /_ | || |    _ __ ___   __ _  ___ _ __ ___                                                                                                            
    | `_ \| `_ \| || |_  | `_ ` _ \ / _` |/ __| `__/ _ \                                                                                                           
    | |_) | (_) |__   _| | | | | | | (_| | (__| | | (_) |                                                                                                          
    |_.__/ \___/   |_|   |_| |_| |_|\__,_|\___|_|  \___/                                                                                                           
                                                                                                                                                                   
    */                                                                                                                                                             
                                                                                                                                                                   
    %macro utl_b64decode(inp,out);                                                                                                                                 
                                                                                                                                                                   
       /*                                                                                                                                                          
       %let inp=d:/sd1/carsEnc.b64;                                                                                                                                
       %let out=d:/sd1/carsDec.zip;                                                                                                                                
       */                                                                                                                                                          
                                                                                                                                                                   
    data _null_;                                                                                                                                                   
      length b64 $ 76 byte $ 1;                                                                                                                                    
      infile "&inp" lrecl= 76 truncover length=b64length;                                                                                                          
      input @1 b64 $base64X76.;                                                                                                                                    
      if _N_=1 then putlog "NOTE: Detected Base64 Line Length of " b64length;                                                                                      
      file "&out" recfm=F lrecl= 1;                                                                                                                                
      do i=1 to (b64length/4)*3;                                                                                                                                   
        byte=byte(rank(substr(b64,i, 1)));                                                                                                                         
        put byte $char1.;                                                                                                                                          
      end;                                                                                                                                                         
    run;quit;                                                                                                                                                      
                                                                                                                                                                   
    %mend utl_b64decode;                                                                                                                                           
                                                                                                                                                                   
                                                                                                                                                                   
    /*              _                                                                                                                                              
      ___ _ __   __| |                                                                                                                                             
     / _ \ `_ \ / _` |                                                                                                                                             
    |  __/ | | | (_| |                                                                                                                                             
     \___|_| |_|\__,_|                                                                                                                                             
                                                                                                                                                                   
    */                                                                                                                                                             
                                                                                                                                                                   
                                                                                                
                                                                                                                                                      
                                                                                                                                                      
