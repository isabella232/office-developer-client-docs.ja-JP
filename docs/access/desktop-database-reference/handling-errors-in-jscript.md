---
title: JScript でのエラーを処理
TOCTitle: Handling errors in JScript
ms:assetid: 2197b4b9-819f-43ff-3ac6-3823c62b40c6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248993(v=office.15)
ms:contentKeyID: 48543684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 886111bcb381385632cace35dd120016c63e3754
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943956"
---
# <a name="handling-errors-in-jscript"></a><span data-ttu-id="aa389-102">JScript でのエラーを処理</span><span class="sxs-lookup"><span data-stu-id="aa389-102">Handling errors in JScript</span></span>


<span data-ttu-id="aa389-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="aa389-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aa389-p101">Microsoft JScript のコードでは、 **Connection** オブジェクトの **Errors** コレクションの **Count** プロパティを確認する必要があります。このプロパティの値が 0 より大きい場合は、他の言語の場合と同様、コレクションを反復処理し、値を表示します。</span><span class="sxs-lookup"><span data-stu-id="aa389-p101">Your Microsoft JScript code must check the **Count** property of the **Connection** object's **Errors** collection. If the value is greater than 0, iterate through the collection and print the values as you would in any of the other languages.</span></span>

```javascript 
 
<!-- BeginErrorExampleJS --> 
<%@ Language=JScript %> 
<HTML> 
<HEAD> 
<title>Error Handling example (JScript)</title> 
</HEAD> 
<BODY> 
<h1>Error Handling example (JScript)</h1> 
<% 
 var cnn1 = Server.CreateObject("ADODB.Connection"); 
 var errLoop = Server.CreateObject("ADODB.Error"); 
 var strError = new String; 
 
 try 
 { 
 // Intentionally trigger an error. 
 cnn1.Open("nothing"); 
 } 
 catch(e) 
 { 
 Response.Write(e.message); 
 } 
%> 
 
</BODY> 
</HTML> 
<!-- EndErrorExampleJS --> 
```

