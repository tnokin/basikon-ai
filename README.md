"# basikon-ai" 

# IBAN automation

- Users can upload a PDF or an image
- Users can shoot their IBAN (bank information) with the camera of their device.

- Document is attached to an entity (person, contract).
- Data extracted from IBAN are mapped in person.bankAccounts[]

```javascript
bankAccounts: [
    {
      name: String,  //name of the account
      bankIban: String,
      bankBic: String,
      bankName: String,
      bankCountry: String,
      bankOwner: String,
      bankOpeningDate: Date,
      bankPreferredWithdrawalDate: String,
      rumMandateId: String,
      rumDateOfSignature: Date
    }
  ],
```

# BALANCESHEET automation

Company informations are usually composed of :
- balancesheet 
- trial balance

Process would be :
- user upload balancesheet/trial balance in pdf
- transform balancesheet/trial balance pdf into a basikonsheet representing the original documents
- transform basikonsheet to standard basikonsheet grid analysis

The result will be 3 entities attached to contract, credit line, funds or person
- the original doc
- the basikonsheet representation of the original doc
- the target basikonsheet define by the company

The result can be applied after training and configuration to any pdf/image document presenting numbers in tables
