---
title: JScript でエラーを処理する
TOCTitle: Handling Errors in JScript
ms:assetid: 2197b4b9-819f-43ff-3ac6-3823c62b40c6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248993(v=office.15)
ms:contentKeyID: 48543684
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1c264d4fb4eae460934fcd056e371607c5c0138e
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860211"
---
# <a name="handling-errors-in-jscript"></a><span data-ttu-id="441eb-102">JScript でエラーを処理する</span><span class="sxs-lookup"><span data-stu-id="441eb-102">Handling Errors in JScript</span></span>


<span data-ttu-id="441eb-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="441eb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="441eb-p101">Microsoft JScript のコードでは、 **Connection** オブジェクトの **Errors** コレクションの **Count** プロパティを確認する必要があります。このプロパティの値が 0 より大きい場合は、他の言語の場合と同様、コレクションを反復処理し、値を表示します。</span><span class="sxs-lookup"><span data-stu-id="441eb-p101">Your Microsoft JScript code must check the **Count** property of the **Connection** object's **Errors** collection. If the value is greater than 0, iterate through the collection and print the values as you would in any of the other languages.</span></span>

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

