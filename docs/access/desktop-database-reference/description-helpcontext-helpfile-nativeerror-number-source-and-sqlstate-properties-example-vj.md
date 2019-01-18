---
title: 説明、HelpContext、HelpFile プロパティの使用例 (vj++)
TOCTitle: Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState properties example (VJ++)
ms:assetid: daa3ff89-9f7f-f832-479e-bbb51c918ae8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250100(v=office.15)
ms:contentKeyID: 48548085
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 53cf6ca9c7758b20115f99601d07d26bbd1b1f3c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714732"
---
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vj"></a>Description プロパティ、HelpContext プロパティ、HelpFile プロパティ、NativeError プロパティ、Number プロパティ、Source プロパティ、SQLState プロパティの使用例 (VJ++)


**適用されます**Access 2013、Office 2013。

この例では、エラーを発生させてトラップし、生成された [Error](description-property-ado.md) オブジェクトの [Description](helpcontext-helpfile-properties-ado.md)、[HelpContext](helpcontext-helpfile-properties-ado.md)、[HelpFile](nativeerror-property-ado.md)、[NativeError](number-property-ado.md)、[Number](source-property-ado-error.md)、[Source](sqlstate-property-ado.md)、および [SQLState](error-object-ado.md) プロパティを表示します。

```java
    // BeginDescriptionJ
    // The WFC class includes the ADO objects.
    
    import com.ms.wfc.data.*;
    import java.io.* ;
    
    public class DescriptionX
    {
       // The main entry point for the application.
    
       public static void main (String[] args)
       {
          DescriptionX();
          System.exit(0);
       }
    
       // DescriptionX function
    
       static void DescriptionX()
       {
          // Declarations.
          BufferedReader in = new 
             BufferedReader(new InputStreamReader(System.in));
    
          // Define ADO Objects.
          Connection cnConn1 = null;
    
          try
          {
             // Intentionally trigger an error.
             cnConn1 = new Connection();
             cnConn1.open("nothing");
          }
          catch( AdoException ae )
          {
             // Notify user of any errors that result from ADO.
             PrintProviderError(cnConn1);
          }
    
          try
          {
             System.out.println("\nPress <Enter> key to continue.");
             in.readLine();
          }
          // System read requires this catch.
          catch( java.io.IOException je)
          {
             PrintIOError(je);
          }
      
       }
    
       // PrintProviderError Function
    
       static void PrintProviderError( Connection Cnn1 )
       {
          // Print Provider errors from Connection object.
          // ErrItem is an item object in the Connections Errors collection.
          com.ms.wfc.data.Error  ErrItem = null;
          long nCount = 0;
          int  i      = 0;
    
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
    // EndDescriptionJ
```
