---
<span data-ttu-id="9de85-101"><<<<<<< ヘッド タイトル: プロバイダーと DefaultDatabase プロパティの使用例 (vc++) TOCTitle: プロバイダーと DefaultDatabase プロパティの使用例 (vc++) === タイトル: プロバイダーと DefaultDatabase プロパティの使用例 (vc++) TOCTitle: プロバイダーDefaultDatabase プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="9de85-101"><<<<<<< HEAD title: Provider and DefaultDatabase Properties Example (VC++) TOCTitle: Provider and DefaultDatabase Properties Example (VC++) ======= title: Provider and DefaultDatabase properties example (VC++) TOCTitle: Provider and DefaultDatabase properties example (VC++)</span></span>
>>>>>>> <span data-ttu-id="9de85-102">マスターの ms:assetid: 21c38be4-3906-cee8-b77b-300f1226392a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248995(v=office.15) ms:contentKeyID: 48543687 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="9de85-102">master ms:assetid: 21c38be4-3906-cee8-b77b-300f1226392a ms:mtpsurl: https://msdn.microsoft.com/library/JJ248995(v=office.15) ms:contentKeyID: 48543687 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="9de85-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="9de85-103"><<<<<<< HEAD</span></span>
# <a name="provider-and-defaultdatabase-properties-example-vc"></a><span data-ttu-id="9de85-104">Provider プロパティと DefaultDatabase プロパティの使用例 (VC++)</span><span class="sxs-lookup"><span data-stu-id="9de85-104">Provider and DefaultDatabase Properties Example (VC++)</span></span>
=======
# <a name="provider-and-defaultdatabase-properties-example-vc"></a><span data-ttu-id="9de85-105">プロバイダーと DefaultDatabase プロパティの使用例 (vc++)</span><span class="sxs-lookup"><span data-stu-id="9de85-105">Provider and DefaultDatabase properties example (VC++)</span></span>
>>>>>>> <span data-ttu-id="9de85-106">master</span><span class="sxs-lookup"><span data-stu-id="9de85-106">master</span></span>


<span data-ttu-id="9de85-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9de85-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9de85-p101">この例では、異なるプロバイダーを使用する 3 つの [Connection](provider-property-ado.md) オブジェクトを開くことによって、 [Provider](connection-object-ado.md) プロパティの機能を示します。また、 [DefaultDatabase](defaultdatabase-property-ado.md) プロパティを使用して、Microsoft ODBC Provider の既定のデータベースを設定します。</span><span class="sxs-lookup"><span data-stu-id="9de85-p101">This example demonstrates the [Provider](provider-property-ado.md) property by opening three [Connection](connection-object-ado.md) objects using different providers. It also uses the [DefaultDatabase](defaultdatabase-property-ado.md) property to set the default database for the Microsoft ODBC Provider.</span></span>

```cpp 
 
// BeginProviderCpp 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <ole2.h> 
#include <stdio.h> 
#include <conio.h> 
 
// Function declarations 
inline void TESTHR(HRESULT x) {if FAILED(x) _com_issue_error(x);}; 
void ProviderX(void); 
void PrintProviderError(_ConnectionPtr pConnection); 
void PrintComError(_com_error &e); 
 
/////////////////////////////// 
// // 
// Main Function // 
// // 
/////////////////////////////// 
void main() 
{ 
 if(FAILED(::CoInitialize(NULL))) 
 return; 
 
 ProviderX(); 
 
 ::CoUninitialize(); 
} 
 
///////////////////////////////// 
// // 
// ProviderX Function // 
// // 
///////////////////////////////// 
 
void ProviderX(void) 
{ 
 HRESULT hr = S_OK; 
 
 // Define ADO object pointers. 
 // Initialize pointers on define. 
 // These are in the ADODB:: namespace. 
 _ConnectionPtr pConnection1 = NULL; 
 _ConnectionPtr pConnection2 = NULL; 
 _ConnectionPtr pConnection3 = NULL; 
 
 try 
 { 
 // Open a Connection using the Microsoft ODBC provider. 
 TESTHR(pConnection1.CreateInstance(__uuidof(Connection))); 
 pConnection1->ConnectionString = "driver={SQL Server};" 
 "server='MySqlServer';user id='MyUserId';password='MyPassword';"; 
 pConnection1->Open("","","",adConnectUnspecified); 
 pConnection1->DefaultDatabase = "pubs"; 
 
 // Display the provider 
 printf("\n\nConnection1 provider: %s \n\n", 
 (LPCSTR)pConnection1->Provider); 
 
 // Open a connection using the OLE DB Provider for Microsoft Jet. 
 TESTHR(pConnection2.CreateInstance(__uuidof(Connection))); 
 pConnection2->Provider = "Microsoft.Jet.OLEDB.4.0"; 
 
 char *sConn = "c:\\Program Files\\Microsoft Office\\Office\\" 
 "Samples\\Northwind.mdb"; 
 
 pConnection2->Open(sConn,"admin","",NULL); 
 
 // Display the provider 
 printf("Connection2 provider: %s \n\n",(LPCSTR)pConnection2-> 
 Provider); 
 
 // Open a Connection using the Microsoft SQL Server provider. 
 TESTHR(pConnection3.CreateInstance(__uuidof(Connection))); 
 pConnection3->Provider = "sqloledb"; 
 pConnection3->Open("Data Source='MySqlServer';Initial Catalog='pubs';", 
 "MyUserId","MyPassword",NULL); 
 
 // Display the provider. 
 printf("Connection3 provider: %s\n\n",(LPCSTR)pConnection3-> 
 Provider); 
 } 
 
 catch (_com_error &e) 
 { 
 // Notify the user of errors if any. 
 PrintProviderError(pConnection1); 
 if(pConnection2) PrintProviderError(pConnection2); 
 if(pConnection3) PrintProviderError(pConnection3); 
 PrintComError(e); 
 } 
 
 if (pConnection1) 
 if (pConnection1->State == adStateOpen) 
 pConnection1->Close(); 
 if (pConnection2) 
 if (pConnection2->State == adStateOpen) 
 pConnection2->Close(); 
 if (pConnection3) 
 if (pConnection3->State == adStateOpen) 
 pConnection3->Close(); 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// PrintProviderError Function // 
// // 
/////////////////////////////////////////////////////////// 
void PrintProviderError(_ConnectionPtr pConnection) 
{ 
 // Print Provider Errors from Connection object. 
 // pErr is a record object in the Connection's Error collection. 
 ErrorPtr pErr = NULL; 
 
 if( (pConnection->Errors->Count) > 0) 
 { 
 long nCount = pConnection->Errors->Count; 
 
 // Collection ranges from 0 to nCount -1. 
 for(long i = 0;i < nCount;i++) 
 { 
 pErr = pConnection->Errors->GetItem(i); 
 printf("Error number: %x\t%s\n", pErr->Number, 
 (LPCSTR) pErr->Description); 
 } 
 } 
} 
 
/////////////////////////////////////////////////////////// 
// // 
// PrintComError Function // 
// // 
/////////////////////////////////////////////////////////// 
void PrintComError(_com_error &e) 
{ 
 _bstr_t bstrSource(e.Source()); 
 _bstr_t bstrDescription(e.Description()); 
 
 // Print COM errors. 
 printf("Error\n"); 
 printf("\tCode = %08lx\n", e.Error()); 
 printf("\tCode meaning = %s\n", e.ErrorMessage()); 
 printf("\tSource = %s\n", (LPCSTR) bstrSource); 
 printf("\tDescription = %s\n", (LPCSTR) bstrDescription); 
} 
// EndProviderCpp 
```

