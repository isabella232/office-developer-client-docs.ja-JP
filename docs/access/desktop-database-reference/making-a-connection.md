---
title: 接続を作成する
TOCTitle: Making a Connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bd99419a841a8fa876dd0ad30b4d06360a27df1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882050"
---
# <a name="making-a-connection"></a>接続を作成する

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


