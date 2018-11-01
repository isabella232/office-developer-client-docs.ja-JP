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
# <a name="making-a-connection"></a><span data-ttu-id="fffa5-102">接続を作成する</span><span class="sxs-lookup"><span data-stu-id="fffa5-102">Making a Connection</span></span>

<span data-ttu-id="fffa5-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fffa5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fffa5-104">データ ソースに接続するには、*接続文字列*、プロバイダーおよびデータ ソースごとに、パラメーターが異なる場合がありますを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fffa5-104">To connect to a data source, you must specify a *connection string*, the parameters of which might differ for each provider and data source.</span></span> <span data-ttu-id="fffa5-105">詳細については、「[接続文字列](creating-the-connection-string.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fffa5-105">For more information, see [Creating the Connection String](creating-the-connection-string.md).</span></span>

<span data-ttu-id="fffa5-p102">ADO では、多くの場合、 **Connection** オブジェクトの **Open** メソッドを使用して接続を開きます。 **Open** メソッドの構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fffa5-p102">ADO most commonly opens a connection by using the **Connection** object **Open** method. The syntax for the **Open** method is shown here:</span></span>

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

<span data-ttu-id="fffa5-108">または、ショートカットの手法では、 **Recordset.Open**、暗黙的な接続を開くし、1 回の操作では、その接続上でコマンドを発行するを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="fffa5-108">Alternatively, you can invoke a shortcut technique, **Recordset.Open**, to open an implicit connection and issue a command over that connection in one operation.</span></span> <span data-ttu-id="fffa5-109">これには、 **Open**メソッドを*暗黙的*な有効な接続文字列で渡すことです。</span><span class="sxs-lookup"><span data-stu-id="fffa5-109">Do this by passing in a valid connection string as the *ActiveConnection* argument to the **Open** method.</span></span> <span data-ttu-id="fffa5-110">Visual Basic 内の各メソッドの構文を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="fffa5-110">Here is the syntax for each method in Visual Basic:</span></span>

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> <span data-ttu-id="fffa5-p104">[!メモ] **Connection** オブジェクトと **Recordset.Open** ショートカットの使い分けは次のようになります。複数の **Recordset** を開く予定がある場合や、複数のコマンドを実行する場合は、 **Connection** オブジェクトを使用します。 **Recordset.Open** ショートカットを使用した場合でも、ADO によって接続が暗黙的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="fffa5-p104">When should you use a **Connection** object vs. the **Recordset.Open** shortcut? Use the **Connection** object if you plan to open more than one **Recordset**, or when executing multiple commands. A connection is still created by ADO implicitly when you use the **Recordset.Open** shortcut.</span></span>


