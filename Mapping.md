# ERD_Task
ERD_Task

Mapping 1
Musician(ID PK, Name, Phone , st , city)
Instrument(Name PK, Key)
Album(ID PK, Title, CopyrightDate)
Song(Title PK, Author)

Plays(MusicianID FK - Musician, InstrumentName FK - Instrument, PK(MusicianID, InstrumentName))
Produces(MusicianID FK - Musician, AlbumID FK - Album, PK(MusicianID, AlbumID))
Includes(AlbumID FK - Album, SongTitle FK - Song, PK(AlbumID, SongTitle))
AppearsAt(MusicianID FK - Musician, CityName, PK(MusicianID, CityName))



Mapping 2

Property(ID PK, Name, Add , city , state , Zip)
Owner(ID PK, Name, Address)
SalesOffice(Number PK, City, State, Zip)
Employee(ID PK, Name)

Owns(OwnerID FK - Owner, PropertyID FK - Property, PercentOwned, 
     PK(OwnerID, PropertyID))
Lists(SalesOfficeNum FK - SalesOffice, PropertyID FK - Property,
     PK(SalesOfficeNum, PropertyID))
Manages(EmployeeID FK - Employee, PropertyID FK - Property, 
        PK(EmployeeID, PropertyID))
WorksAt(EmployeeID FK - Employee, SalesOfficeNum FK - SalesOffice, Date,
        PK(EmployeeID, SalesOfficeNum))




Mapping 3

Patient(ID PK, Name, DOB)
Nurse(ID PK, Name)
Ward(Code PK, Name)
Drug(ID PK, Name, Brand)
Consultant(ID PK, Name)

Supervises(NurseID FK - Nurse, WardCode FK - Ward, 
           PK(NurseID, WardCode))
Hosts(WardCode FK - Ward, PatientID FK - Patient,
      PK(WardCode, PatientID))
AssignedTo(PatientID FK - Patient, NurseID FK - Nurse, 
           PK(PatientID, NurseID))
Examines(PatientID FK - Patient, ConsultantID FK - Consultant,
         PK(PatientID, ConsultantID))
Gives(PatientID FK - Patient, DrugID FK - Drug, Dosage, Time, Date,
      PK(PatientID, DrugID, Time, Date))
ServesIn(ConsultantID FK - Consultant, WardCode FK - Ward,
         PK(ConsultantID, WardCode))





