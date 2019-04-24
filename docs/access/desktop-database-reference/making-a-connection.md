---
title: 接続の作成
TOCTitle: Making a connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 487212acd8847928e1fab405593edb172d0172d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289785"
---
# <a name="making-a-connection"></a><span data-ttu-id="1662f-102">接続の作成</span><span class="sxs-lookup"><span data-stu-id="1662f-102">Making a connection</span></span>

<span data-ttu-id="1662f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="1662f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1662f-104">データソースに接続するには、*接続文字列*を指定する必要があります。これらのパラメーターは、プロバイダーとデータソースごとに異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1662f-104">To connect to a data source, you must specify a *connection string*, the parameters of which might differ for each provider and data source.</span></span> <span data-ttu-id="1662f-105">For more information, see [Creating the Connection String](creating-the-connection-string.md).</span><span class="sxs-lookup"><span data-stu-id="1662f-105">For more information, see [Creating the Connection String](creating-the-connection-string.md).</span></span>

<span data-ttu-id="1662f-p102">ADO では、多くの場合、**Connection** オブジェクトの **Open** メソッドを使用して接続を開きます。**Open** メソッドの構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1662f-p102">ADO most commonly opens a connection by using the **Connection** object **Open** method. The syntax for the **Open** method is shown here:</span></span>

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

<span data-ttu-id="1662f-p103">代わりに、**Recordset.Open** というショートカット コマンドを呼び出す方法もあります。この方法では、一度の操作で、暗黙的な接続を開き、その接続に関するコマンドを発行できます。これには、**Open** メソッドの *ActiveConnection* 引数として、有効な接続文字列を渡します。ここでは、各メソッドの構文を Visual Basic で示しています。</span><span class="sxs-lookup"><span data-stu-id="1662f-p103">Alternatively, you can invoke a shortcut technique, **Recordset.Open**, to open an implicit connection and issue a command over that connection in one operation. Do this by passing in a valid connection string as the *ActiveConnection* argument to the **Open** method. Here is the syntax for each method in Visual Basic:</span></span>

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> <span data-ttu-id="1662f-p104">[!メモ] **Connection** オブジェクトと **Recordset.Open** ショートカットの使い分けは次のようになります。複数の **Recordset** を開く予定がある場合や、複数のコマンドを実行する場合は、 **Connection** オブジェクトを使用します。 **Recordset.Open** ショートカットを使用した場合でも、ADO によって接続が暗黙的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="1662f-p104">When should you use a **Connection** object vs. the **Recordset.Open** shortcut? Use the **Connection** object if you plan to open more than one **Recordset**, or when executing multiple commands. A connection is still created by ADO implicitly when you use the **Recordset.Open** shortcut.</span></span>


