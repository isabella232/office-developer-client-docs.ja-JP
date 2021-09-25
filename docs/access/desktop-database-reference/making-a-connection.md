---
title: 接続の作成
TOCTitle: Making a connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5c63ad8329dddecfb8a5900a1ade860325629322
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581036"
---
# <a name="making-a-connection"></a>接続の作成

**適用先:** Access 2013、Office 2013

データ ソースに接続するには、接続文字列を指定する必要があります。パラメーターはプロバイダーとデータ ソースごとに異なる場合があります。 For more information, see [Creating the Connection String](creating-the-connection-string.md).

ADO では、多くの場合、**Connection** オブジェクトの **Open** メソッドを使用して接続を開きます。**Open** メソッドの構文は次のとおりです。

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

代わりに、**Recordset.Open** というショートカット コマンドを呼び出す方法もあります。この方法では、一度の操作で、暗黙的な接続を開き、その接続に関するコマンドを発行できます。これには、**Open** メソッドの *ActiveConnection* 引数として、有効な接続文字列を渡します。ここでは、各メソッドの構文を Visual Basic で示しています。

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> [!メモ] **Connection** オブジェクトと **Recordset.Open** ショートカットの使い分けは次のようになります。複数の **Recordset** を開く予定がある場合や、複数のコマンドを実行する場合は、 **Connection** オブジェクトを使用します。 **Recordset.Open** ショートカットを使用した場合でも、ADO によって接続が暗黙的に作成されます。


