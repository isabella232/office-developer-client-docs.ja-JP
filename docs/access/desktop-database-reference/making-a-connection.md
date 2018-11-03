---
title: 接続を作成します。
TOCTitle: Making a connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0335c4bbc0d1240d6d4ca53ceacf47bf44fce67d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945888"
---
# <a name="making-a-connection"></a>接続を作成します。

**適用されます**Access 2013、Office 2013。

データ ソースに接続するには、*接続文字列*、プロバイダーおよびデータ ソースごとに、パラメーターが異なる場合がありますを参照してください。 詳細については、「[接続文字列](creating-the-connection-string.md)」を参照してください。

ADO では、多くの場合、 **Connection** オブジェクトの **Open** メソッドを使用して接続を開きます。 **Open** メソッドの構文は次のとおりです。

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

または、ショートカットの手法では、 **Recordset.Open**、暗黙的な接続を開くし、1 回の操作では、その接続上でコマンドを発行するを呼び出すことができます。 これには、 **Open**メソッドを*暗黙的*な有効な接続文字列で渡すことです。 Visual Basic 内の各メソッドの構文を以下に示します。

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> [!メモ] **Connection** オブジェクトと **Recordset.Open** ショートカットの使い分けは次のようになります。複数の **Recordset** を開く予定がある場合や、複数のコマンドを実行する場合は、 **Connection** オブジェクトを使用します。 **Recordset.Open** ショートカットを使用した場合でも、ADO によって接続が暗黙的に作成されます。


