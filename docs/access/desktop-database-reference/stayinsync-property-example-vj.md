---
title: StayInSync プロパティの使用例 (VJ++)
TOCTitle: StayInSync property example (VJ++)
ms:assetid: e9e0fcc7-07b6-c433-7c4c-478fc69eacaf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250184(v=office.15)
ms:contentKeyID: 48548448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 202ce2dd8d8c672a9b6df27dff73f9c3e2691569
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601794"
---
# <a name="stayinsync-property-example-vj"></a>StayInSync プロパティの使用例 (VJ++)


**適用先**: Access 2013、Office 2013

この例では、階層 [Recordset](stayinsync-property-ado.md) 内の行へのアクセスを容易にする [StayInSync](recordset-object-ado.md) プロパティの機能を示します。

外側のループで、各作成者の姓名、州、および ID を表示します。各行に追加された **Recordset** が [Fields](fields-collection-ado.md) コレクションから取得され、親の **Recordset** が新しい行に移動するたびに **StayInSync** プロパティによって自動的に **rstTitleAuthor** に割り当てられます。内側のループでは、追加されたレコードセットの各行から 4 つのフィールドを表示します。

```java 
 
// BeginStayInSyncJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
import com.ms.com.*; 
 
public class StayInSyncX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 StayInSyncX(); 
 System.exit(0); 
 } 
 
 // StayInSyncX function 
 
 static void StayInSyncX() 
 { 
 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Recordset rstAuthors = null; 
 Recordset rstTitleAuthor = null; 
 
 // Declarations. 
 BufferedReader in = new 
 BufferedReader (new InputStreamReader(System.in)); 
 String strCnn = "Provider=MSDataShape;" + 
 "Data Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"; 
 
 
 try 
 { 
 cnConn1 = new Connection(); 
 cnConn1.open(strCnn); 
 rstAuthors = new Recordset(); 
 rstAuthors.setStayInSync(true); 
 rstAuthors.open("SHAPE {select * from Authors} " + 
 "APPEND ({select * from titleauthor}" + 
 "RELATE au_id TO au_id) AS chapTitleAuthor", 
 cnConn1, 
 AdoEnums.CursorType.STATIC, 
 AdoEnums.LockType.READONLY, 
 AdoEnums.CommandType.TEXT); 
 
 Variant varRstTitleAuthor = rstAuthors.getFields(). 
 getItem("chapTitleAuthor").getValue(); 
 rstTitleAuthor =new Recordset(varRstTitleAuthor.toObject()); 
 int intCount =0; 
 while(!rstAuthors.getEOF()) 
 { 
 System.out.println("\n" + 
 rstAuthors.getField("au_fname").getString() + " " + 
 rstAuthors.getField("au_lname").getString() + " " + 
 rstAuthors.getField("state").getString() + " " + 
 rstAuthors.getField("au_id").getString()); 
 while(!rstTitleAuthor.getEOF()) 
 { 
 System.out.println(rstTitleAuthor.getField(0). 
 getString() + " " + 
 rstTitleAuthor.getField(1).getString() + " " + 
 rstTitleAuthor.getField(2).getString() + " " + 
 rstTitleAuthor.getField(3).getString()); 
 rstTitleAuthor.moveNext(); 
 } 
 if(++intCount % 5 == 0) 
 { 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 rstAuthors.moveNext(); 
 } 
 
 System.out.println("\nPress <Enter> to continue.."); 
 in.readLine(); 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 // As passing a Recordset, check for null pointer first. 
 if (rstAuthors != null) 
 { 
 PrintProviderError(rstAuthors.getActiveConnection()); 
 } 
 else 
 { 
 System.out.println("Exception: " + ae.getMessage()); 
 } 
 } 
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (rstTitleAuthor != null) 
 if (rstTitleAuthor.getState() == 1) 
 rstTitleAuthor.close(); 
 if (rstAuthors != null) 
 if (rstAuthors.getState() == 1) 
 rstAuthors.close(); 
 if (cnConn1 != null) 
 if (cnConn1.getState() == 1) 
 cnConn1.close(); 
 } 
 } 
 
 // PrintProviderError Function 
 static void PrintProviderError(Connection cnn1) 
 { 
 // Print Provider Errors from Connection Object. 
 // ErrItem is an item object in the Connections Errors Collection. 
 com.ms.wfc.data.Error ErrItem = null; 
 long nCount = 0; 
 int i = 0; 
 
 nCount = cnn1.getErrors().getCount(); 
 
 // If there are any errors in the collection, print them. 
 if ( nCount > 0) 
 { 
 // Collection ranges from 0 to nCount-1. 
 for ( i=0;i<nCount; i++) 
 { 
 ErrItem = cnn1.getErrors().getItem(i); 
 System.out.println("\t Error Number: " + ErrItem.getNumber() 
 + "\t" + ErrItem.getDescription()); 
 } 
 } 
 } 
 // PrintIOError Function 
 static void PrintIOError(java.io.IOException je) 
 { 
 System.out.println("Error: \n"); 
 System.out.println("\t Source: " + je.getClass() + "\n"); 
 System.out.println("\t Description: "+ je.getMessage() + "\n"); 
 } 
} 
// EndStayInSyncJ 
```

