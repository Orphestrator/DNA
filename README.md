# Orphestrator DNA - Data centric Network Application

DNA provides a HTTP Context Adapter which is nameable. Each DNAContextAdapter could bind one or more 
data services like:
- CSVDataService
- ExcelDataService
- DatabaseDataService
- more will follow

## Orphestrator\DNA\IDataService

Provides the initial interface for an DataService and provides following methods:
- List<IDataAccessObject> read(ICondition:condition, IRange:range)
- IDataAccessObject readOneByKey(string:id)

## Orphestrator\DNA\IMutableDataService

Inherits from IDataService and provides additional methods:
- IDataAccessObject:createdData create(IDataAccessObject:data) 
- IDataAccessObject:updatedData update(IDataAccessObject:data)
- IDataAccessObject:deletedData delete(IDataAccessObject:data)
