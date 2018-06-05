# enti
|filed|type|
|----|-----|
|id_ente|INTEGER NOT NULL|            
|desc_ente|VARCHAR(150) NOT NULL|       
|testo|VARCHAR(255)|                

# fabbisogni_ateco_livello1 
|filed|type|
|----|-----|
|pk_livello1|CHAR(1) NOT NULL|            
|nome|VARCHAR(255)|    
|descrizione|MEDIUMTEXT|                  
|help|MEDIUMTEXT|          

Primary Key:
*pk_livello1*

# fabbisogni_ateco_livello2
|filed|type|
|----|-----|
|codice|VARCHAR(5) NOT NULL         
|pk_livello2| VARCHAR(5) NOT NULL         
|nome|VARCHAR(255)                
|descrizione|MEDIUMTEXT                  
|fk_livello1|CHAR(1)                     

Primary Key: *pk_livello2*                   

# fabbisogni_ateco_livello3                                        [table]
------------------------------------------------------------------------
  cod_ateco_livello1                VARCHAR(11) NOT NULL        
  cod_ateco_livello2                VARCHAR(111) NOT NULL       
  cod_ateco_livello3                VARCHAR(222) NOT NULL       
  descrizione                       VARCHAR(222) NOT NULL       



# fabbisogni_ateco_livello4                                        [table]
------------------------------------------------------------------------
  cod_ateco_livello1                VARCHAR(11) NOT NULL        
  cod_ateco_livello2                VARCHAR(111) NOT NULL       
  cod_ateco_livello3                VARCHAR(11) NOT NULL        
  cod_ateco_livello4                VARCHAR(222) NOT NULL       
  descrizione                       VARCHAR(222) NOT NULL       



# fabbisogni_ateco_livello5                                        [table]
------------------------------------------------------------------------
  cod_ateco_livello1                VARCHAR(11) NOT NULL        
  cod_ateco_livello2                VARCHAR(111) NOT NULL       
  cod_ateco_livello3                VARCHAR(222) NOT NULL       
  descrizione                       VARCHAR(222) NOT NULL       



# fabbisogni_ateco_professioni  
------------------------------------------------------------------------
  pk_professioni                    INTEGER NOT NULL            
  nome                              VARCHAR(255)                
  fk_livello6                       VARCHAR(255)                

Primary Key:
*pk_professioni*


# fabbisogni_competenze 
------------------------------------------------------------------------
  fk_livello5                       VARCHAR(9) NOT NULL         
  C1a                               DECIMAL(11,5) NOT NULL      
  C2a                               DECIMAL(11,5) NOT NULL      
  C3a                               DECIMAL(11,5) NOT NULL      
  C4a                               DECIMAL(11,5) NOT NULL      
  C5a                               DECIMAL(11,5) NOT NULL      
  C6a                               DECIMAL(11,5) NOT NULL      
  C7a                               DECIMAL(11,5) NOT NULL      
  C8a                               DECIMAL(11,5) NOT NULL      
  C9a                               DECIMAL(11,5) NOT NULL      
  C10a                              DECIMAL(11,5) NOT NULL      
  C11a                              DECIMAL(11,5) NOT NULL      
  C12a                              DECIMAL(11,5) NOT NULL      
  C13a                              DECIMAL(11,5) NOT NULL      
  C14a                              DECIMAL(11,5) NOT NULL      
  C15a                              DECIMAL(11,5) NOT NULL      
  C16a                              DECIMAL(11,5) NOT NULL      
  C17a                              DECIMAL(11,5) NOT NULL      
  C18a                              DECIMAL(11,5) NOT NULL      
  C19a                              DECIMAL(11,5) NOT NULL      
  C20a                              DECIMAL(11,5) NOT NULL      
  C21a                              DECIMAL(11,5) NOT NULL      
  C22a                              DECIMAL(11,5) NOT NULL      
  C23a                              DECIMAL(11,5) NOT NULL      
  C24a                              DECIMAL(11,5) NOT NULL      
  C25a                              DECIMAL(11,5) NOT NULL      
  C26a                              DECIMAL(11,5) NOT NULL      
  C27a                              DECIMAL(11,5) NOT NULL      
  C28a                              DECIMAL(11,5) NOT NULL      
  C29a                              DECIMAL(11,5) NOT NULL      
  C30a                              DECIMAL(11,5) NOT NULL      
  C31a                              DECIMAL(11,5) NOT NULL      
  C32a                              DECIMAL(11,5) NOT NULL      
  C33a                              DECIMAL(11,5) NOT NULL      
  C34a                              DECIMAL(11,5) NOT NULL      
  C35a                              DECIMAL(11,5) NOT NULL      



fabbisogni_denominazioni  
  id_denominazione                  INTEGER NOT NULL            
                                    auto-incremented            
  denominazione                     VARCHAR(255) NOT NULL       

Primary Key
*id_denominazione*                   



fabbisogni_fonti                                                 [table]
------------------------------------------------------------------------
  id_fonte                          INTEGER NOT NULL            
                                    auto-incremented            
  fonte                             VARCHAR(255) NOT NULL       
  data                              VARCHAR(15) NOT NULL        
  data_cnf                          VARCHAR(255) NOT NULL       

Primary Key

                                                           [primary key]
  id_fonte                          ascending                   



fabbisogni_menu                                                  [table]
------------------------------------------------------------------------
  id_menu                           INTEGER NOT NULL            
  desc_menu                         VARCHAR(100) NOT NULL       
  longdesc_menu                     LONGTEXT NOT NULL           



fabbisogni_professionali                                         [table]
------------------------------------------------------------------------
  cod_nup                           INTEGER                     
  variabile                         VARCHAR(3)                  
  id_menu                           INTEGER                     



fabbisogni_province                                              [table]
------------------------------------------------------------------------
  cod_regione                       VARCHAR(2) NOT NULL         
  cod_provincia                     VARCHAR(3) NOT NULL         
  denom_provincia                   VARCHAR(200) NOT NULL       
  sigla_provincia                   VARCHAR(2) NOT NULL         



fabbisogni_regioni                                               [table]
------------------------------------------------------------------------
  cod_regione                       VARCHAR(3) NOT NULL         
  denom_regione                     VARCHAR(150) NOT NULL       



fabbisogni_table                                                 [table]
------------------------------------------------------------------------
  id_fabbisogni_table               INTEGER NOT NULL            
                                    auto-incremented            
  "table"                           VARCHAR(255) NOT NULL       
  desc_table                        LONGTEXT NOT NULL           
  flag_cod_ateco                    INTEGER NOT NULL            
  flag_cod_nup                      INTEGER NOT NULL            

Primary Key

                                                           [primary key]
  id_fabbisogni_table               ascending                   



livello1                                                         [table]
------------------------------------------------------------------------
  pk_livello1                       CHAR(1) NOT NULL            
  nome                              VARCHAR(255)                
  descrizione                       MEDIUMTEXT                  
  help                              MEDIUMTEXT                  

Primary Key

                                                           [primary key]
  pk_livello1                       ascending                   

Indexes

sqlite_autoindex_livello1_1                               [unique index]
  pk_livello1                       unknown                     

idx_livello1_uno                                      [non-unique index]
  nome                              unknown                     



livello2                                                         [table]
------------------------------------------------------------------------
  pk_livello2                       VARCHAR(3) NOT NULL         
  nome                              VARCHAR(255)                
  descrizione                       MEDIUMTEXT                  
  fk_livello1                       CHAR(1)                     

Primary Key

                                                           [primary key]
  pk_livello2                       ascending                   

Indexes

idx_livello2_due                                      [non-unique index]
  nome                              unknown                     

sqlite_autoindex_livello2_1                               [unique index]
  pk_livello2                       unknown                     

idx_livello2_FULL2                                    [non-unique index]
  nome                              unknown                     
  descrizione                       unknown                     



livello3                                                         [table]
------------------------------------------------------------------------
  pk_livello3                       VARCHAR(5) NOT NULL         
  nome                              MEDIUMTEXT                  
  descrizione                       MEDIUMTEXT                  
  fk_livello2                       VARCHAR(3)                  

Primary Key

                                                           [primary key]
  pk_livello3                       ascending                   

Indexes

idx_livello3_tre                                      [non-unique index]
  nome                              unknown                     

sqlite_autoindex_livello3_1                               [unique index]
  pk_livello3                       unknown                     

idx_livello3_pk_livello3_2                            [non-unique index]
  pk_livello3                       unknown                     

idx_livello3_FULL3                                    [non-unique index]
  nome                              unknown                     
  descrizione                       unknown                     



livello4                                                         [table]
------------------------------------------------------------------------
  pk_livello4                       VARCHAR(7) NOT NULL         
  nome                              MEDIUMTEXT                  
  descrizione                       MEDIUMTEXT                  
  fk_livello3                       VARCHAR(5)                  

Primary Key

                                                           [primary key]
  pk_livello4                       ascending                   

Indexes

idx_livello4_quattro                                  [non-unique index]
  nome                              unknown                     

sqlite_autoindex_livello4_1                               [unique index]
  pk_livello4                       unknown                     

idx_livello4_FULL4                                    [non-unique index]
  nome                              unknown                     
  descrizione                       unknown                     



livello5                                                         [table]
------------------------------------------------------------------------
  pk_livello5                       VARCHAR(255) NOT NULL       
  nome                              VARCHAR(255)                
  descrizione                       MEDIUMTEXT                  
  fk_livello4                       VARCHAR(50)                 

Primary Key

                                                           [primary key]
  pk_livello5                       ascending                   

Indexes

idx_livello5_nome                                     [non-unique index]
  nome                              unknown                     

sqlite_autoindex_livello5_1                               [unique index]
  pk_livello5                       unknown                     



professioni                                                      [table]
------------------------------------------------------------------------
  id                                INTEGER NOT NULL            
                                    auto-incremented            
  pk_professioni                    VARCHAR(12) NOT NULL        
  nome                              VARCHAR(255)                
  fk_livello5                       VARCHAR(255)                
  anno                              VARCHAR(4)                  
  provenienza                       LONGTEXT                    
  pk_professioni_01                 VARCHAR(12)                 
  nome_01                           VARCHAR(255)                
  codice                            VARCHAR(1)                  
  flag_vista                        LONGTEXT                    

Primary Key

                                                           [primary key]
  id                                ascending                   

Indexes

idx_professioni_nome                                  [non-unique index]
  nome                              unknown                     



professioni_personalita                                          [table]
------------------------------------------------------------------------
  pk_livello5                       VARCHAR(15) NOT NULL        
  titolo_di_studio                  VARCHAR(100) NOT NULL       
