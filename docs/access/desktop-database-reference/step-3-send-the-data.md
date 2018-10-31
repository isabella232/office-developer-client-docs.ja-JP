---
title: '手順 3: データを送信する'
TOCTitle: 'Step 3: Send the Data'
ms:assetid: d22ffe59-179b-fd1a-1211-be1a0d76b02f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250049(v=office.15)
ms:contentKeyID: 48547878
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 692bf7e1adf561c99ec1e3060578de93fbd1a064
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861884"
---
# <a name="step-3-send-the-data"></a>手順 3: データを送信する


**適用されます**Access 2013 |。Office 2013

## <a name="step-3-send-the-data"></a>手順 3: データの送信

**Recordset** の準備が完了したので、これを XML として ASP **Response** オブジェクトに保存して、クライアントに送信する必要があります。XMLResponse.asp の最後に次のコードを追加します。

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

ASP**応答**オブジェクトが**レコード セット**の[保存](save-method-ado.md)メソッドの保存先として指定されていることを確認します。 **Save** メソッドの保存先には、 **IStream** インターフェイスをサポートする任意のオブジェクト (ADO の [Stream](stream-object-ado.md) オブジェクトなど)、または、 **Recordset** の保存先の完全なパスを含むファイル名を指定できます。

XMLResponse.asp を保存して閉じ、次の手順に進みます。 Adovbs.inc ファイルを c: からコピーも\\Program Files\\ファイルの一般的な\\システム\\XMLResponse.asp ファイルがあるフォルダーにフォルダーを Ado。

### <a name="next-step"></a>次のステップ

[手順 4: データを受信します。](step-4-receive-and-display-the-data.md)

