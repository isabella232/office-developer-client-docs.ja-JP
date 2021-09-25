---
title: Provider プロパティと DefaultDatabase プロパティの使用例 (VJ++)
TOCTitle: Provider and DefaultDatabase properties example (VJ++)
ms:assetid: babd3c3c-bb6e-46ce-88f2-ef2810d798fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249898(v=office.15)
ms:contentKeyID: 48547380
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d9477312e9d7dafd2cdde68a62aee70b2dc9cad4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617804"
---
# <a name="provider-and-defaultdatabase-properties-example-vj"></a>Provider プロパティと DefaultDatabase プロパティの使用例 (VJ++)


**適用先**: Access 2013、Office 2013

この例では、異なるプロバイダーを使用する 3 つの [Connection](provider-property-ado.md) オブジェクトを開くことによって、 [Provider](connection-object-ado.md) プロパティの機能を示します。また、 [DefaultDatabase](defaultdatabase-property-ado.md) プロパティを使用して、Microsoft ODBC Provider の既定のデータベースを設定します。

```java 
 
// BeginProviderJ 
import java.io.*; 
import com.ms.wfc.data.*; 
 
public class ProviderX 
{ 
 // The main entry point of the application. 
 public static void main (String[] args) 
 { 
 ProviderX(); 
 System.exit(0); 
 } 
 // ProviderX Function 
 static void ProviderX() 
 { 
 // Define ADO Objects. 
 Connection cnn1 = null; 
 Connection cnn2 = null; 
 Connection cnn3 = null; 
 
 // Declarations. 
 BufferedReader in = 
 new BufferedReader(new InputStreamReader(System.in)); 
 try 
 { 
 // Open a connection using the Microsoft ODBC Provider. 
 cnn1 = new Connection(); 
 cnn1.setConnectionString("driver={SQL Server};"+ 
 "server='MySqlServer';User ID='MyUserID';Password='MyPassword';"); 
 cnn1.open(); 
 cnn1.setDefaultDatabase("Pubs"); 
 
 // Display the provider. 
 System.out.println("\n\n\tCnn1 provider: "+ cnn1.getProvider()); 
 
 // Open connection using the OLE DB Provider for Microsoft Jet. 
 cnn2 = new Connection(); 
 cnn2.setProvider("Microsoft.Jet.OLEDB.4.0"); 
 cnn2.open("C:\\Program Files\\Microsoft Office\\Office\\Samples\\Northwind.mdb","admin",""); 
 
 // Display the provider. 
 System.out.println("\n\n\tCnn2 provider: " + 
 cnn2.getProvider()); 
 
 // Open a connection using the Microsoft SQL Server Provider. 
 cnn3 = new Connection(); 
 cnn3.setProvider("sqloledb"); 
 cnn3.open("Data Source='MySqlServer';Initial Catalog='Pubs';Integrated Security='SSPI';","",""); 
 
 // Display the provider. 
 System.out.println("\n\n\tCnn3 provider: " + 
 cnn3.getProvider()); 
 
 System.out.println("\n\n\tPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 catch(AdoException ae) 
 { 
 // Notify the user of any errors that result from ADO. 
 
 // As passing a Connection, check for null pointer first. 
 if(cnn1 != null) 
 { 
 PrintProviderError(cnn1); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getLocalizedMessage()); 
 } 
 } 
 // System read requires needs this catch. 
 catch(java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (cnn1 != null) 
 if (cnn1.getState() == 1) 
 cnn1.close(); 
 if (cnn2 != null) 
 if (cnn2.getState() == 1) 
 cnn2.close(); 
 if (cnn3 != null) 
 if (cnn3.getState() == 1) 
 cnn3.close(); 
 } 
 } 
 // PrintProviderError Function 
 
 static void PrintProviderError( Connection Cnn1 ) 
 { 
 // Print Provider errors from Connection object. 
 // ErrItem is an item object in the Connections Errors collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = Cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if( nCount > 0); 
 { 
 // Collection ranges from 0 to nCount - 1 
 for (i = 0; i< nCount; i++) 
 { 
 ErrItem = Cnn1.getErrors().getItem(i); 
 System.out.println("\t Error number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription() ); 
 } 
 } 
 
 } 
 
 // PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
// EndProviderJ 
```

