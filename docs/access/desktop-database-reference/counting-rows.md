---
title: 行数をカウントする (Access デスクトップデータベースリファレンス)
TOCTitle: Counting rows
ms:assetid: ff684c5e-7f41-0dae-beea-f5c71f79bd84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250312(v=office.15)
ms:contentKeyID: 48548963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2388978185ac29149f7f15150ccfdbc559cc910f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295416"
---
# <a name="counting-rows"></a>行のカウント


**適用先:** Access 2013、Office 2013

**RecordCount** プロパティは、 **Recordset** 内のレコード数を示す長整数型 ( **Long** ) の値を返します。 **Recordset** オブジェクト内のレコード数を調べるには、 **RecordCount** プロパティを使用します。レコード数を特定できない場合、またはプロバイダーやカーソルの種類が **RecordCount** をサポートしていない場合は、このプロパティは -1 を返します。閉じている **Recordset** の **RecordCount** プロパティを読み取ると、エラーが発生します。

**RecordCount** プロパティの値は、プロバイダーの機能とカーソルの種類によって異なります。 **RecordCount** プロパティは、前方スクロール カーソルの場合は -1 を返し、静的カーソルまたはキーセット カーソルの場合は実際の数を返し、動的カーソルの場合はデータ ソースによって -1 または実際の数を返します。

「[3 章: データを調べる](chapter-3-examining-data.md)」にあるサンプル **Recordset** は、前方スクロール カーソルが開いているため -1 を返します。**RecordCount** プロパティを使用するには、より高度なカーソル (静的カーソルまたはキーセット カーソル) で **Recordset** を開く必要があります。

場合によっては、データ ソースからすべてのレコードを最初にフェッチしないと、プロバイダーまたはカーソルが **RecordCount** 値を提供できないことがあります。このような種類のフェッチを強制的に行うには、 **Recordset** **MoveLast** メソッドを呼び出してから **RecordCount** を呼び出します。

**Recordset** **Open** メソッドを呼び出すコード行を次の行に置き換えると、

```vb 
 
oRs.Open sSQL, sCnStr, adOpenStatic, adLockOptimistic, adCmdText 
```

**Microsoft OLE DB Provider for SQL Server** の静的カーソルは [RecordCount](microsoft-ole-db-provider-for-sql-server.md) をサポートしているため、 **RecordCount** プロパティを使用できます。たとえば、次のコードを実行すると、カーソルが **RecordCount** プロパティをサポートしている場合、コマンドが返すレコード数がデバッグ ウィンドウに表示されます。

```vb 
 
Debug.Print oRs.RecordCount ' Output: 4 
```

ここからは、これらのさらに高度な (ただし負荷が高い) カーソルとロックの種類の設定を使用します。

