---
title: DefinedSize プロパティの使用例 (VC++)
TOCTitle: DefinedSize Property Example (VC++)
ms:assetid: eac03770-4e6a-90fd-3e0e-89246b61d403
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250192(v=office.15)
ms:contentKeyID: 48548474
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09bcf0746497fc7daff85411c418638301300717
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477814"
---
# <a name="definedsize-property-example-vc"></a><span data-ttu-id="05951-102">DefinedSize プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="05951-102">DefinedSize Property Example (VC++)</span></span>


<span data-ttu-id="05951-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="05951-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="05951-104">ここでは、[Column](definedsize-property-adox.md) の [DefinedSize](column-object-adox.md) プロパティの使用例を示します。</span><span class="sxs-lookup"><span data-stu-id="05951-104">This example demonstrates the [DefinedSize](definedsize-property-adox.md) property of a [Column](column-object-adox.md).</span></span> <span data-ttu-id="05951-105">コードは、 *Northwind*データベースの [**社員**] テーブルの [フリガナ] 列のサイズを再定義します。</span><span class="sxs-lookup"><span data-stu-id="05951-105">The code will redefine the size of the FirstName column of the **Employees** table of the *Northwind* database.</span></span> <span data-ttu-id="05951-106">次に、 [Employees](field-object-ado.md) テーブルに基づいた [レコードセット](recordset-object-ado.md)の FirstName **フィールド**の値の変更が表示されます。</span><span class="sxs-lookup"><span data-stu-id="05951-106">Then, the change in the values of the FirstName [Field](field-object-ado.md) of a [Recordset](recordset-object-ado.md) based on the **Employees** table is displayed.</span></span> <span data-ttu-id="05951-107">既定では、 **DefinedSize** プロパティを再定義すると、FirstName フィールドがスペースで埋められます。</span><span class="sxs-lookup"><span data-stu-id="05951-107">Note that by default, the FirstName field becomes padded with spaces after you redefine the **DefinedSize** property.</span></span>

```cpp 
 
// BeginDefinedSizeCpp 
#import "c:\Program Files\Common Files\system\ado\msadox.dll" no_namespace 
#import "C:\Program Files\Common Files\System\ADO\msado15.dll" rename("EOF", "EndOfFile") 
 
#include "iostream.h" 
#include "stdio.h" 
#include "conio.h" 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void DefinedSizeX(void); 
 
////////////////////////////////////////////////////////// 
// // 
// Main Function // 
// // 
////////////////////////////////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 DefinedSizeX(); 
 
 ::CoUninitialize(); 
} 
 
////////////////////////////////////////////////////////// 
// // 
// DefinedSizeX Function // 
// // 
////////////////////////////////////////////////////////// 
void DefinedSizeX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADOX object pointers. 
 // Initialize pointers on define. 
 // These are in the ADOX:: namespace. 
 _CatalogPtr m_pCatNorthwind = NULL; 
 _ColumnPtr m_pColFirstName = NULL; 
 _ColumnPtr m_pColNewFirstName = NULL; 
 
 // Define ADODB object pointers 
 ADODB::_RecordsetPtr m_pRstEmployees = NULL; 
 
 // Define string variables. 
 _bstr_t strCnn("Provider='Microsoft.JET.OLEDB.4.0';data source=" 
 "'c:\\Program Files\\Microsoft Office\\Office\\Samples\\" 
 "Northwind.mdb';"); 
 _bstr_t aryFirstName[10]; 
 
 try 
 { 
 // Open a Recordset for the Employees table. 
 TESTHR(hr = m_pRstEmployees.CreateInstance( 
 __uuidof(ADODB::Recordset))); 
 TESTHR(hr = m_pCatNorthwind.CreateInstance(__uuidof (Catalog))); 
 TESTHR(hr = m_pColNewFirstName.CreateInstance(__uuidof(Column))); 
 
 m_pRstEmployees->Open("Employees",strCnn,ADODB::adOpenKeyset, 
 ADODB::adLockReadOnly,ADODB::adCmdTable); 
 
 long lngSize = m_pRstEmployees->RecordCount; 
 aryFirstName[lngSize]; 
 
 // Open a catalog for the Northwind database, 
 // using same connection as rstEmployees. 
 m_pCatNorthwind->PutActiveConnection(m_pRstEmployees-> 
 GetActiveConnection()); 
 
 // Loop through the recordset displaying the contents, 
 // of the FirstName field, the field's defined size, 
 // and its actual size. 
 // Also store FirstName values in aryFirstName array. 
 m_pRstEmployees->MoveFirst(); 
 printf("\nOriginal Defined Size and Actual Size"); 
 int iCount=0; 
 while (!(m_pRstEmployees->EndOfFile)) 
 { 
 printf("\nEmployee Name:"); 
 printf("%s ",(LPSTR)(_bstr_t)m_pRstEmployees->Fields-> 
 GetItem("FirstName")->Value); 
 printf("%s\n",(LPSTR)(_bstr_t)m_pRstEmployees->Fields-> 
 GetItem("LastName")->Value); 
 printf(" FirstName Defined size: %d\n",m_pRstEmployees-> 
 Fields->GetItem("FirstName")->DefinedSize) ; 
 printf(" FirstName Actual size: %d\n",m_pRstEmployees-> 
 Fields->GetItem("FirstName")->ActualSize); 
 aryFirstName[iCount] = (_bstr_t) m_pRstEmployees->Fields-> 
 GetItem("FirstName")->Value; 
 m_pRstEmployees->MoveNext(); 
 iCount++; 
 if(iCount%5==0) 
 { 
 printf("Press any key to continue..."); 
 getch(); 
 system("cls"); 
 } 
 } 
 m_pRstEmployees->Close(); 
 
 // Redefine the DefinedSize of FirstName in the catalog. 
 m_pColFirstName = m_pCatNorthwind->Tables->GetItem("Employees")-> 
 Columns->GetItem("FirstName"); 
 m_pColNewFirstName->Name = m_pColFirstName->Name; 
 m_pColNewFirstName->Type = m_pColFirstName->Type; 
 m_pColNewFirstName->DefinedSize = 
 (m_pColFirstName->DefinedSize) + 1; 
 
 // Append new FirstName column to catalog. 
 m_pCatNorthwind->Tables->GetItem("Employees")->Columns-> 
 Delete(m_pColFirstName->Name); 
 m_pCatNorthwind->Tables->GetItem("Employees")->Columns-> 
 Append(_variant_t((IDispatch*)m_pColNewFirstName,true), 
 adVarWChar,m_pColNewFirstName->DefinedSize); 
 
 // Open Employee table in Recordset for updating. 
 m_pRstEmployees->Open("Employees",m_pCatNorthwind-> 
 GetActiveConnection(),ADODB::adOpenKeyset, 
 ADODB::adLockOptimistic,ADODB::adCmdTable); 
 
 // Loop through the recordset displaying the contents 
 // of the FirstName field,the field's defined size, 
 // and its actual size. 
 // Also restore FirstName values from aryFirstName. 
 printf("Press any key to continue..."); 
 getch(); 
 system("cls"); 
 m_pRstEmployees->MoveFirst(); 
 printf("\n\nNew Defined Size and Actual Size"); 
 iCount=0; 
 while (!(m_pRstEmployees->EndOfFile)) 
 { 
 m_pRstEmployees->Fields->GetItem("FirstName")->Value = 
 aryFirstName[iCount]; 
 printf("\nEmployee Name: "); 
 printf("%s ",(LPSTR) (_bstr_t)m_pRstEmployees->Fields-> 
 GetItem("FirstName")->Value); 
 printf("%s\n",(LPSTR)(_bstr_t)m_pRstEmployees->Fields-> 
 GetItem("LastName")->Value); 
 printf(" FirstName Defined size: %d\n",m_pRstEmployees-> 
 Fields->GetItem("FirstName")->DefinedSize ); 
 printf(" FirstName Actual size: %d\n",m_pRstEmployees-> 
 Fields->GetItem("FirstName")->ActualSize ); 
 m_pRstEmployees->MoveNext(); 
 iCount++; 
 if(iCount%5==0) 
 { 
 printf("Press any key to continue..."); 
 getch(); 
 system("cls"); 
 } 
 } 
 m_pRstEmployees->Close(); 
 
 // Restore original FirstName column to catalog 
 m_pCatNorthwind->Tables->GetItem("Employees")->Columns-> 
 Delete(m_pColNewFirstName->Name); 
 
 m_pCatNorthwind->Tables->GetItem("Employees")->Columns-> 
 Append(_variant_t((IDispatch*)m_pColFirstName,true), 
 adVarWChar,m_pColFirstName->DefinedSize); 
 
 // Restore original FirstName values to Employees table. 
 m_pRstEmployees->Open("Employees",m_pCatNorthwind-> 
 GetActiveConnection(),ADODB::adOpenKeyset, 
 ADODB::adLockOptimistic,ADODB::adCmdTable); 
 
 m_pRstEmployees->MoveFirst(); 
 iCount = 0; 
 while(!(m_pRstEmployees->EndOfFile)) 
 { 
 m_pRstEmployees->Fields->GetItem("FirstName")->Value = 
 aryFirstName[iCount]; 
 m_pRstEmployees->MoveNext(); 
 iCount++; 
 } 
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
 cout << "Error occured in DefinedSizeX...."<< endl; 
 } 
 
 if (m_pRstEmployees) 
 if (m_pRstEmployees->State == 1) 
 m_pRstEmployees->Close(); 
 
 m_pCatNorthwind = NULL; 
} 
// EndDefinedSizeCpp 
```
