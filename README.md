# AAC²E

ASCII Schematics for [AC²E](https://github.com/matthschw/ace) circuits. Created
with [AACircuit](https://github.com/Blokkendoos/AACircuit).

## OP0

<p align="center">Generic Amplifier Symbol</p>

``` VDD
             |         
          |\ |         
          | \|
  INP ----+  + 
          |   \
          |    \
    B ----+ op0 >---- OUT
          |    /
          |   /
  INN ----+  +
          | /|
          |/ |
             |
            VSS 
```

## OP1

<p align="center">Miller Operational Amplifier</p>

```
  #------------------------------------------------------------.        
 VSS                       |                   |               |        
                    MPCM21 +-||             ||-+ MPCM22        |        
                           <-||             ||->               |        
                           +-||--o----------||-+               |        
                           |     |             |               |        
                           o-----'             |            ||-+ MPCS   
                           |                   |            ||->        
                           |                   o------------||-+        
                           |                   |               |        
                           |Y                 X|               |        
                           |                   |   RC_   CC||  |        
                           |                   o--|___|----||--o        
                           |                   |           ||  |        
                           |                   |               |        
                           |                   |               |        
                           |                   |               |        
                           |                   |               |   OUT  
                        ||-+ MND11       MND12 +-||            o----#   
                  INP   ||<-                   ->||   INN      |        
          B        #----||-+                   +-||----#       |        
          #                |        CM         |               |        
          |                '---------o---------'               |        
          |                          |                         |        
          o-----------.              |                         |        
          |           |              |                         |        
          |           |              |                         '        
   MNCM11 +-||        |           ||-+ MNCM12               ||-+ MNCM13 
          ->||        |           ||<-                      ||<-        
          +-||--------o-----------||-+            .---------||-+        
          |           '--------------)------------'            |        
 VDD      |                          |                         |        
  #-------o--------------------------o-------------------------'        
 
```

## OP2 and OP3

<p align="center">(Un-) Symmetrical Amplifier</p>

```
   #------------------o-------------o-------------o-------------.       
  VDD                 | MPCM222     |             |     MPCM212 |       
                      +-||       ||-+ MPCM221     +-||       ||-+       
                      <-||   Y   ||->             <-||   X   ||->       
                      +-||----o--||-+     MPCM211 +-||--o----||-+       
                      |       |     |             |     |       |       
                      |       |     |             |     |       |       
                      |       '-----o             o-----'       |       
                      |             |             |             |       
                      |             |             |             |       
       B              |             |             |             |       
       #              |          ||-+ MND11       +-||          |       
       |              |    INN   ||<-             ->||   INP    |       
       |              |     #----||-+       MND12 +-||----#     |       
       o------.       |             |     CM      |             |   OUT 
       |      |       |             '------o------'             o----#  
       |      |       |                    |                    |       
MNCM11 +-||   |       |                 ||-+ MNCM12             |       
       ->||   |       |                 ||<-                    |       
       +-||---o-------)-----------------||-+                    |       
       |              |                    |                    |       
       |              |                    |                    |       
       |              |                    |                    |       
       |              o------.             |                    |       
       |              |      |             |                    |       
       |              |      |             |                    |       
       |       MCNM31 +-||   |             |                 ||-+ MCNM32
       |              ->||   |  Z          |                 ||<-       
       |              +-||---o-------------)-----------------||-+       
  VSS  |              |                    |                    |       
   #---o--------------o--------------------o--------------------'       
```

## OP4

<p align="center">Symmetrical Amplifier with Cascodes</p>

```
  #--------------o---------o-----------o----------o-----------.         
                 |         |           |          |           |         
                 |  MPCM222+-||     ||-+MPCM221   +-||     ||-+         
                 |         <-||  Y  ||->          <-||  X  ||->         
                 |         +-||--o--||-+   MPCM211+-||--o--||-+MPCM212  
                 |         |     |     |          |     |     |         
                 |        V|     '-----o          o-----'     |W        
                 |         |           |          |           |         
            MPC1R+-|| MPC12+-||        |          |        ||-+MPC11    
                 <-||      <-||  R     |          |        ||->         
                 +-||-.    +-||--o-----)----------)--------||-+         
                 |    |    |     |     |          |           |         
                 o----o----)-----'     |          |           |         
                 |         |           |          |           |         
                 |         |           |          |           |         
                 |         |           |          |           |    OUT  
                 |         |        ||-+MND11     +-||        o-----#   
                 |         |  INN   ||<-          ->||   INP  |         
                 |         |   #----||-+     MND12+-||----#   |         
                 |         |           |   CM     |           |         
                 |         |           '----o-----'           |         
                 |         o----.           |                 |         
     B           |         |    |           |                 |         
     #           |   MNCM31+-|| |           |              ||-+MNCM32   
     |           |         ->|| |Z          |              ||<-         
     |           |         +-||-o-----------)--------------||-+         
     |           |         |                |                 |         
     |           |         |                |                 |         
     o-----.     |         |                |                 |         
     |     |     |         |                |                 |         
     +-||  |  ||-+MNCM12   |             ||-+MNCM13           |         
     ->||  |  ||<-         |             ||<-                 |         
     +-||--o--||-+         |         .---||-+                 |         
     |MNCM11-----)---------)---------'      |                 |         
  #--o-----------o---------o----------------o-----------------'         
```

## OP5

NA

## OP6

<p align="center">Miller Operational Amplifier without R and C</p>

```
   #----------------------o----------------o----------------------.     
  VDD                     |                |                      |     
                   MPCM21 +-||          ||-+ MPCM22               |     
                          <-||          ||->                      |     
                          +-||--o-------||-+                      |     
                          |     |          |                      |     
                          o-----'          |                      |     
                          |                |                   ||-+ MPCS
                          |                |                   ||->     
                          |                o-------------------||-+     
                          |                |                      |     
                          |                |                      |     
                          |                |                      |     
                          |Y              X|                 .----o     
                          |                |                 |M   |     
                          |                |              ||-+P   |     
                          |                |       MPR1   ||--C---o     
                          |                o---------+^+--||-+1   |     
                          |                |         |||     |    |     
         B                |                |         ===     '----o     
         #             ||-+ MND11    MND12 +-||        |          |     
         |        INP  ||<-                ->||  INN   |          |  OUT
         |         #---||-+                +-||---#    |          o---# 
         o------.         |      CM        |           |          |     
         |      |         '-------o--------'           |          |     
         o      |                 |                    |          |     
  MNCM11 +-||   |              ||-+ MNCM12             |MNCM13 ||-+     
         ->||   |              ||<-                    |       ||<-     
         +-||---o------'-------||-+--------------------|-------||-+     
         |                        |                    |          |     
   #-----o------------------------o--------------------o----------'     
  VSS                                                                   
```

## NAND0

<p align="center">Generic NOT Gate inverter Symbol</p>

```
      +-----+
      |  1  |
 A ---|     |O--- Q
      |     |
      +-----+
```

```
      |\
 A ---| >O--- Q
      |/
```

## NAND4

<p align="center">4 NAND Gate Inverter Chain</p>

```
VDD #---------o----------o----------o----------.                        
              |          |          |          |                        
              |          |          |          |                        
           ||-+ MP0   ||-+ MP1   ||-+ MP2   ||-+ MP3                    
           ||->       ||->       ||->       ||->                        
        .--||-+    .--||-+    .--||-+    .--||-+                        
        |     |    |     |    |     |    |     |                        
        |     '----)-----o----)-----o----)-----o----# O                 
        |          |          |          |     |                        
        |          |          |          |  ||-+ MN3                    
        |          |          |          |  ||<-                        
 I3 #---)----------)----------)----------o--||-+                        
        |          |          |                |                        
        |          |          |                |                        
        |          |          |                |                        
        |          |          |             ||-+ MN2                    
        |          |          |             ||<-                        
 I2 #---)----------)----------o-------------||-+                        
        |          |                           |                        
        |          |                           |                        
        |          |                           |                        
        |          |                        ||-+ MN1                    
        |          |                        ||<-                        
 I1 #---)----------o------------------------||-+                        
        |                                      |                        
        |                                      |                        
        |                                      |                        
        |                                   ||-+ MN0                    
        |                                   ||<-                        
 I0 #---o-----------------------------------||-+                        
                                               |                        
                                               |                        
VSS #------------------------------------------'                        
```

## ST1

<p align="center">Schmitt Trigger</p>

```
  VDD #-------------o------------------.                                
                    |                  |                                
                 ||-+ MP0              |                                
                 ||->                  |                                
            .----||-+                  |                                
            |       |                  |                                
            |       |          MP2     |                                
            |       o--------+^+-----. |                                
            |       |        |||     | |                                
            |       |        ===     | |                                
            |    ||-+ MP1      |     | |                                
            |    ||->          |     | |                                
            o----||-+          |     | |                                
            |       |          |     | |                                
            |       |          |     | |                                
    I #-----o       o---------o------)-)-----# O                        
            |       |        |       | |                                
            |       |        |       | |                                
            |    ||-+ MN1    |       | |                                
            |    ||<-        |       | |                                
            o----||-+        |       | |                                
            |       |        ===     | |                                
            |       |        |^|     | |                                
            |       o--------+|+-----)-'                                
            |       |          MN2   |                                  
            |       |                |                                  
            |    ||-+ MN0            |                                  
            |    ||<-                |                                  
            '----||-+                |                                  
                    |                |                                  
  VSS #-------------o----------------'                                  
```
