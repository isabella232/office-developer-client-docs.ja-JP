---
title: '手順 3: サーバーからレコードセットを取得する (RDS チュートリアル)'
TOCTitle: 'Step 3: Server Obtains a Recordset (RDS Tutorial)'
ms:assetid: fadb6a9b-ed44-264f-22fd-26b121f98040
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250282(v=office.15)
ms:contentKeyID: 48548856
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9f3299892118d044bfcc36f3fa28e4e25eaed9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881133"
---
# <a name="step-3-server-obtains-a-recordset-rds-tutorial"></a>手順 3: サーバーによるレコードセットの取得 (RDS チュートリアル)


**適用されます**Access 2013、Office 2013。

サーバー プログラムは、目的の行のデータ ソースのクエリを実行するために、接続文字列とコマンド テキストを使用します。通常、この **Recordset** の取得には ADO が使用されますが、マイクロソフトのその他のデータ アクセス インターフェイス (OLE DB など) を使用することもできます。

カスタマー サーバー プログラムは次のようになります。

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

