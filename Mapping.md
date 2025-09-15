# ERD_Task
ERD_Task

Mapping 1
Musician(ID PK, Name, Phone , st , city)
PlaySong(song_title,MusicianId)
Instrument(Name PK, Key)
Album(ID PK, Title, Date,MusicianID "fk")
Song(Title PK, Author, AlbumId "FK")
playInstrument(instrumentName,MusicianId)



Mapping 2

Property(ID PK, Name, Add , city , state , Zip,salesOfficeNum "FK")
Owner(ID PK, Name, Address)
ownerhasproperty (propertyId "FK" , OwnerId "FK")
SalesOffice(Number PK, City, State, Zip)
Employee(ID PK, Name,salesOfficeNum "FK")




Mapping 3

Patient(ID PK, Name, DOB,consultantID,WardID"FK")
Nurses(ID PK, Name,WardID"FK")
Wards(ID PK, Name)
Drugs(Code PK, RecDosage)
patientDrug (PatientID,DrugCode)
Brands (Drugid FK , brand)
Consultants(ID PK, Name)
PatientNurserelation(NurseID,PatientID)






