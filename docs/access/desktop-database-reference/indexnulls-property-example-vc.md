---
title: IndexNulls プロパティの使用例 (VC++)
TOCTitle: IndexNulls property example (VC++)
ms:assetid: 05d1f8b3-ae70-cca5-d60d-af55f5f7c13a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248813(v=office.15)
ms:contentKeyID: 48543039
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 22dba78c2a9ad1c7fb20a355801a13c100da0239
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602368"
---
# <a name="indexnulls-property-example-vc"></a>IndexNulls プロパティの使用例 (VC++)


**適用先**: Access 2013、Office 2013

ここでは、[Index](indexnulls-property-adox.md) の [IndexNulls](index-object-adox.md) プロパティの使用例を示します。 このコードでは、新しいインデックスが作成され、ユーザーの入力に基づいて **IndexNulls** の値が設定されます。 次に **、Northwind** カタログの **Employees** [テーブルに](table-object-adox.md)*インデックスが追加*[されます](catalog-object-adox.md)。 新しい **Index** が [Employees](recordset-object-ado.md) テーブルに基づいて **Recordset** に適用され、 **Recordset** が開きます。 新しいレコードが **Employees** テーブルに追加され、 **Null** 値がインデックス フィールドに入ります。 この新しいレコードが表示されるかどうかは、 **IndexNulls** プロパティの設定によって決まります。

```cpp 
 
// BeignIndexNullCpp 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" rename("EOF", "EndOfFile") 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
#include "ADOXIndexNullsX.h" 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void IndexNullsX(_bstr_t); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 printf("\nShow records having indexed field value = NULL? (Y/N):"); 
 char input = getche(); 
 
 if(toupper(input)=='Y') 
 { 
 IndexNullsX("Allow"); 
 } 
 else if(toupper(input)=='N') 
 { 
 IndexNullsX("Ignore"); 
 } 
 else 
 { 
 exit(0); 
 } 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// IndexNullsX Function // 
// // 
////////////////////////////////////////////////////////// 
void IndexNullsX(_bstr_t strSel) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatalog = NULL; 
 _IndexPtr m_pIndexNew = NULL; 
 
 // Define ADODB object pointers 
 ADODB::_ConnectionPtr m_pCnn = NULL; 
 ADODB::_RecordsetPtr m_pRstEmployees = NULL; 
 
 // Define other variables 
 IADORecordBinding *picRs = NULL; // Interface Pointer Declared 
 CEmployeeRs emprs; // C++ Class Object 
 
 // Define string variable. 
 _bstr_t strCnn("Provider='Microsoft.JET.OLEDB.4.0';" 
 "data source='c:\\Program Files\\Microsoft Office\\Office\\" 
 "Samples\\Northwind.mdb';"); 
 
 try 
 { 
 TESTHR(hr = m_pCnn.CreateInstance(__uuidof(ADODB::Connection))); 
 TESTHR(hr = m_pCatalog.CreateInstance(__uuidof (Catalog))); 
 TESTHR(hr = m_pIndexNew.CreateInstance(__uuidof(Index))); 
 TESTHR(hr = m_pRstEmployees.CreateInstance( 
 __uuidof(ADODB::Recordset))); 
 
 // Connect the catalog. 
 m_pCnn->Open(strCnn,"","",NULL); 
 m_pCatalog->PutActiveConnection(_variant_t((IDispatch *)m_pCnn)); 
 
 // Append Country column to new index. 
 m_pIndexNew->Columns->Append("Country",adVarWChar,0); 
 m_pIndexNew->Name = "NewIndex"; 
 
 // Set IndexNulls based on user input 
 if(strcmp((LPSTR)strSel,"Allow")==0) 
 { 
 m_pIndexNew->IndexNulls = adIndexNullsAllow; 
 } 
 else if(strcmp((LPSTR)strSel,"Ignore")==0) 
 { 
 m_pIndexNew->IndexNulls = adIndexNullsIgnore; 
 } 
 
 // Append new index to Employees table 
 m_pCatalog->Tables->GetItem("Employees")->Indexes->Append( 
 _variant_t((IDispatch *)m_pIndexNew)); 
 m_pRstEmployees->Index = m_pIndexNew->Name; 
 m_pRstEmployees->Open("Employees", 
 _variant_t((IDispatch *)m_pCnn), 
 ADODB::adOpenKeyset,ADODB::adLockOptimistic, 
 ADODB::adCmdTableDirect); 
 
 // Add a new record to the Employees table. 
 m_pRstEmployees->AddNew(); 
 m_pRstEmployees->Fields->GetItem("FirstName")->Value = 
 (_bstr_t) "Gary"; 
 m_pRstEmployees->Fields->GetItem("LastName")->Value = 
 (_bstr_t) "Haarsager"; 
 m_pRstEmployees->Update(); 
 
 // Bookmark the newly added record. 
 _variant_t varBookmark = m_pRstEmployees->Bookmark; 
 
 // Use the new index to set the order of the records. 
 m_pRstEmployees->MoveFirst(); 
 printf("\n\nIndex = %s,",(LPSTR) m_pRstEmployees->Index); 
 printf("IndexNulls = %d\n\n",m_pIndexNew->IndexNulls); 
 cout<<"Country - Name"<<endl; 
 
 // Open an IADORecordBinding interface pointer which 
 // we will use for binding Recordset to a class 
 TESTHR(hr = m_pRstEmployees->QueryInterface( 
 __uuidof(IADORecordBinding),(LPVOID*)&picRs)); 
 
 // Bind the Recordset to a C++ class here 
 TESTHR(hr = picRs->BindToRecordset(&emprs)); 
 
 // Enumerate the Recordset.The value of the 
 // IndexNulls property will determine if the newly 
 // added record appears in the output. 
 while(!(m_pRstEmployees->EndOfFile)) 
 { 
 printf("%s - %s %s\n", 
 emprs.lemp_CountryStatus == adFldOK ? 
 emprs.m_szemp_Country :"[Null]", 
 emprs.lemp_FirstNameStatus == adFldOK ? 
 emprs.m_szemp_FirstName :"<NULL>", 
 emprs.lemp_LastNameStatus == adFldOK ? 
 emprs.m_szemp_LastName :"<NULL>"); 
 m_pRstEmployees->MoveNext(); 
 } 
 
 // Delete new record because this is a demonstration. 
 m_pRstEmployees->Bookmark = varBookmark; 
 m_pRstEmployees->Delete(ADODB::adAffectCurrent); 
 } 
 catch(_com_error &e) 
 { 
 // Notify the user of errors if any. 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 printf("\n\tSource : %s \n\tdescription : %s \n ", 
 (LPCSTR)bstrSource,(LPCSTR)bstrDescription); 
 } 
 catch(...) 
 { 
 cout << "Error occured in include files...."<< endl; 
 } 
 
 if (m_pRstEmployees) 
 { 
 if (m_pRstEmployees->State == 1) 
 { 
 m_pRstEmployees->Close(); 
 m_pRstEmployees = NULL; 
 } 
 } 
 
 // Delete new Index because this is a demonstration. 
 if (m_pCatalog) 
 m_pCatalog->Tables->GetItem("Employees")->Indexes-> 
 Delete(m_pIndexNew->Name); 
 
 if (m_pCnn) 
 { 
 if (m_pCnn->State == 1) 
 { 
 m_pCnn->Close(); 
 m_pCnn = NULL; 
 } 
 } 
 
 m_pCatalog = NULL; 
} 
// EndIndexNullCpp 
```

<br/>

**IndexNullX.h**

```cpp
    // BeginIndexNullsH 
    // IndexNullsX.h 
     
    #include "icrsint.h" 
     
    //This class extracts LastName,Country,FirstName from Employees table 
     
    class CEmployeeRs : public CADORecordBinding 
    { 
    BEGIN_ADO_BINDING(CEmployeeRs) 
     // Column LastName is the 2nd field in the table 
     ADO_VARIABLE_LENGTH_ENTRY2(2,adVarChar,m_szemp_LastName, 
     sizeof(m_szemp_LastName),lemp_LastNameStatus,TRUE) 
     // Column Country is the 11th field in the table 
     ADO_VARIABLE_LENGTH_ENTRY2(11,adVarChar,m_szemp_Country, 
     sizeof(m_szemp_Country),lemp_CountryStatus,TRUE) 
     // Column Country is the 17th field in the table 
     ADO_VARIABLE_LENGTH_ENTRY2(17,adVarChar,m_szemp_FirstName, 
     sizeof(m_szemp_FirstName),lemp_FirstNameStatus,TRUE) 
    END_ADO_BINDING() 
     
    public: 
     CHAR m_szemp_LastName[21]; 
     ULONG lemp_LastNameStatus; 
     CHAR m_szemp_Country[16]; 
     ULONG lemp_CountryStatus; 
     CHAR m_szemp_FirstName[11]; 
     ULONG lemp_FirstNameStatus; 
    }; 
    // EndIndexNullsH
```
