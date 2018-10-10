---
title: (デスクトップ データベース参照のアクセス) の行数をカウントします。
TOCTitle: Counting Rows
ms:assetid: ff684c5e-7f41-0dae-beea-f5c71f79bd84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250312(v=office.15)
ms:contentKeyID: 48548963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 93a583ef0a8f0ef287835eebdd9d68cf726a19df
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478585"
---
# <a name="counting-rows"></a>行数をカウントする


**適用されます**Access 2013 |。Office 2013

**RecordCount** プロパティは、 **Recordset** 内のレコード数を示す長整数型 ( **Long** ) の値を返します。 **Recordset** オブジェクト内のレコード数を調べるには、 **RecordCount** プロパティを使用します。レコード数を特定できない場合、またはプロバイダーやカーソルの種類が **RecordCount** をサポートしていない場合は、このプロパティは -1 を返します。閉じている **Recordset** の **RecordCount** プロパティを読み取ると、エラーが発生します。

**RecordCount** プロパティの値は、プロバイダーの機能とカーソルの種類によって異なります。 **RecordCount** プロパティは、前方スクロール カーソルの場合は -1 を返し、静的カーソルまたはキーセット カーソルの場合は実際の数を返し、動的カーソルの場合はデータ ソースによって -1 または実際の数を返します。

サンプル**レコード セット**の[データを調べること](chapter-3-examining-data.md)で導入されたため-1 を返します、前方スクロール カーソルが開かれました。 **RecordCount** プロパティを使用するには、より高度なカーソル (静的カーソルまたはキーセット カーソル) で **Recordset** を開く必要があります。

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

