# SAS
## Learn SAS
### 1. Suppose you want to access a data set that is stored in the SAS library C:\Myid\Patient\Data in the Windows operating environment.Write a statement to assign the libref Clinic to this library.
libname Clinic 'c:\Myid\Patient\Data'; <br>
### 2. Display Dataset
     proc datasets;
        contents data=sasuser._all_ nods;
     quit;
     proc contents data=sasuser._all_ nods;
     run;
### 3. Generate Data
data oranges:
     input variety $ flavor texture looks;
     /* total = flavor + texture + looks; */ 
     total = flavor + texture + looks;
     label total = 'Sum'
     cards;
navel 9 8 6
temple 7 7 7
valencia 8 9 9
mandarin 5 7 8 ;

