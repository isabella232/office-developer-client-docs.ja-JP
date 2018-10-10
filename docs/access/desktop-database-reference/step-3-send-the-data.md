---
title: '手順 3: データを送信する'
TOCTitle: 'Step 3: Send the Data'
ms:assetid: d22ffe59-179b-fd1a-1211-be1a0d76b02f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250049(v=office.15)
ms:contentKeyID: 48547878
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed3e6bfd6fe3b6727055eb264b1261b13d7a5a0b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476419"
---
# <a name="step-3-send-the-data"></a><span data-ttu-id="3be56-102">手順 3: データを送信する</span><span class="sxs-lookup"><span data-stu-id="3be56-102">Step 3: Send the Data</span></span>


<span data-ttu-id="3be56-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="3be56-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="3be56-104">手順 3: データを送信する</span><span class="sxs-lookup"><span data-stu-id="3be56-104">Step 3: Send the Data</span></span>

<span data-ttu-id="3be56-p101">**Recordset** の準備が完了したので、これを XML として ASP **Response** オブジェクトに保存して、クライアントに送信する必要があります。XMLResponse.asp の最後に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="3be56-p101">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object. Add the following code to the bottom of XMLResponse.asp:</span></span>

```vb 
 
  Response.ContentType = "text/xml" 
  Response.Expires = 0 
  Response.Buffer = False 
 
 
  Response.Write "<?xml version='1.0'?>" & vbNewLine 
  adoRec.save Response, adPersistXML 
  adoRec.Close 
  Set adoRec=Nothing 
%> 
```

<span data-ttu-id="3be56-107">ASP**応答**オブジェクトが**レコード セット**の[保存](save-method-ado.md)メソッドの保存先として指定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3be56-107">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="3be56-108">**Save** メソッドの保存先には、 **IStream** インターフェイスをサポートする任意のオブジェクト (ADO の [Stream](stream-object-ado.md) オブジェクトなど)、または、 **Recordset** の保存先の完全なパスを含むファイル名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="3be56-108">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

<span data-ttu-id="3be56-109">XMLResponse.asp を保存して閉じ、次の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="3be56-109">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="3be56-110">Adovbs.inc ファイルを c: からコピーも\\Program Files\\ファイルの一般的な\\システム\\XMLResponse.asp ファイルがあるフォルダーにフォルダーを Ado。</span><span class="sxs-lookup"><span data-stu-id="3be56-110">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

<span data-ttu-id="3be56-111">**次へ**[手順 4: データを受け取る](step-4-receive-and-display-the-data.md)</span><span class="sxs-lookup"><span data-stu-id="3be56-111">**Next** [Step 4: Receive the Data](step-4-receive-and-display-the-data.md)</span></span>

