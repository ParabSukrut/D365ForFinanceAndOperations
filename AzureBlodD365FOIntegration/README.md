THis solutions is going to help integrate Dynamics 365 for fincnace or supply chain  with Azure blob storage. 
Solution has class with name CopyItemMasterDataToBlob which connects to azure blob storage using connection string , creates a file which contains item data and writes that file to the blob storage. 

BlobSettingsTable is created with below fields to store blob related info and documents

Process | blob Storage account | Conatainer Name | Blob account key

Authentication : Pass your storage account  name and key to class Microsoft.WindowsAzure.Storage.Auth.StorageCredentials to authenticate with your storage.
