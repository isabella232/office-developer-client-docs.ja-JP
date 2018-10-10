---
title: '手順 4: データを受信し、表示する'
TOCTitle: 'Step 4: Receive and Display the Data'
ms:assetid: a27cc1d8-0ee0-95a5-ad70-88c454c10485
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249749(v=office.15)
ms:contentKeyID: 48546764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2a447b68b8c0eeb18d18050ba8dbbb6f09786ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478905"
---
# <a name="step-4-receive-and-display-the-data"></a>手順 4: データを受信し、表示する


**適用されます**Access 2013 |。Office 2013

## <a name="step-4-receive-and-display-the-data"></a>手順 4: データを受信し、表示する

この手順では、 [Recordset](datacontrol-object-rds.md) を取得するための XMLResponse.asp ファイルを示す **RDS.DataControl** オブジェクトが埋め込まれた HTML ファイルを作成します。Windows のメモ帳などのテキスト エディターで default.htm を開き、次のコードを追加します。URL の "sqlserver" は、実際に使用するサーバー コンピューターの名前に置き換えてください。

```html 
 
<HTML> 
<HEAD><TITLE>ADO Recordset Persistence Sample</TITLE></HEAD> 
<BODY> 
 
<TABLE DATASRC="#RDC1" border="1"> 
  <TR> 
<TD><SPAN DATAFLD="title"></SPAN></TD> 
<TD><SPAN DATAFLD="price"></SPAN></TD> 
  </TR> 
</TABLE> 

<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"> 
   <PARAM NAME="URL" VALUE="XMLResponse.asp"> 
</OBJECT> 
 
</BODY> 
</HTML> 
```

Default.htm ファイルを閉じ、XMLResponse.asp を保存した同じフォルダーに保存します。 4.0 またはそれ以降の Internet Explorer を使用すると、URL の https://*sql server*/XMLPersist/default.htm を開き、結果を確認します。 データは、バインドされた DHTML テーブルに表示されます。 これで URL の https://*sql server*/XMLPersist/XMLResponse.asp を開き、結果を確認します。 XML が表示されます。

