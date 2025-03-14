# SQL_QGIS
QGIS Useful SQL Query  


## ricavare bounding box per tutte le geometrie che hanno un attributo comune all'interno di un layer
SELECT 
    "attributee",
    ST_Envelope(ST_Collect(geometry)) AS geometry
FROM 
    'namelayer'
WHERE 
    "attribute" IS NOT NULL
GROUP BY 
    "attribute"

    
