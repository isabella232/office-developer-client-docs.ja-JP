---
title: XML DOM オブジェクトに保存する
TOCTitle: Saving to the XML DOM Object
ms:assetid: 3c61fc30-9862-347b-c215-08597eccfead
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249160(v=office.15)
ms:contentKeyID: 48544318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d0118eb277f8f1cc3332aeff1880b161d62f36cb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885396"
---
# <a name="saving-to-the-xml-dom-object"></a><span data-ttu-id="3f1ac-102">XML DOM オブジェクトに保存する</span><span class="sxs-lookup"><span data-stu-id="3f1ac-102">Saving to the XML DOM Object</span></span>


<span data-ttu-id="3f1ac-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3f1ac-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="saving-to-the-xml-dom-object"></a><span data-ttu-id="3f1ac-104">XML DOM オブジェクトに保存する</span><span class="sxs-lookup"><span data-stu-id="3f1ac-104">Saving to the XML DOM Object</span></span>

<span data-ttu-id="3f1ac-105">次の Visual Basic コードに示すように、XML 形式の **Recordset** を MSXML DOM オブジェクトのインスタンスに保存できます。</span><span class="sxs-lookup"><span data-stu-id="3f1ac-105">You can save a **Recordset** in XML format to an instance of an MSXML DOM object, as shown in the following Visual Basic code:</span></span>

```vb 
 
Dim xDOM As New MSXML.DOMDocument 
Dim rsXML As New ADODB.Recordset 
Dim sSQL As String, sConn As String 
     
sSQL = "SELECT customerid, companyname, contactname FROM customers" 
sConn="Provider=Microsoft.Jet.OLEDB.4.0;Data Source=D:\Program Files" & _ 
        "\Common Files\System\msadc\samples\NWind.mdb" 
rsXML.Open sSQL, sConn 
rsXML.Save xDOM, adPersistADO   'Save Recordset directly into a DOM tree. 
... 
```

