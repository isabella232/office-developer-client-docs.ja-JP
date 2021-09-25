---
title: ブックマークの使用 (Access デスクトップ データベースリファレンス)
TOCTitle: Using Bookmarks
ms:assetid: fe6333ef-c9d9-1e84-2252-d27edc676e97
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250306(v=office.15)
ms:contentKeyID: 48548935
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b7291c1fd3fa63e20b5ac3a098884e0c4fd0ec6e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588932"
---
# <a name="using-bookmarks"></a>ブックマークの使用


**適用先**: Access 2013、Office 2013

**Recordset** 内を移動した後、各レコードをスクロールして値を比較しなくても特定のレコードに直接戻ることができると便利な場合があります。たとえば、 **Find** メソッドでレコードを検索して見つからなかった場合、 **Recordset** のいずれかの端に自動的に戻ります。プロバイダーがブックマークをサポートしている場合、ブックマークを使用すると、 **Find** メソッドを使用する前の位置をマークし、その位置に戻ることができます。ブックマークはバリアント ( **Variant** ) 型の値で、 **Recordset** オブジェクト内のレコードを一意に識別します。

**Recordset** **Filter** メソッドでブックマークのバリアント型配列を使用して、選択したレコードセットをフィルターすることもできます。この方法の詳細については、この章の後半の「 [レコードセットを使用する](working-with-recordsets.md)」の「結果のフィルター処理」を参照してください。

**Bookmark** プロパティを使用すると、レコードのブックマークを取得したり、 **Recordset** オブジェクト内の現在のレコードを、有効なブックマークで識別されたレコードに設定したりできます。次のコードでは、 **Bookmark** プロパティを使用してブックマークを設定し、他のレコードに移動した後にブックマークが設定されたレコードに戻ります。 **Recordset** がブックマークをサポートしているかどうかを判断するには、 **Supports** メソッドを使用します。

```vb 
 
'BeginBookmarkEg 
 Dim varBookmark As Variant 
 Dim blnCanBkmrk As Boolean 
 
 objRs.Open strSQL, strConnStr, adOpenStatic, adLockOptimistic, adCmdText 
 
 If objRs.RecordCount > 4 Then 
 objRs.Move 4 ' move to the fifth record 
 blnCanBkmrk = objRs.Supports(adBookmark) 
 If blnCanBkmrk = True Then 
 varBookmark = objRs.Bookmark ' record the bookmark 
 objRs.MoveLast ' move to a different record 
 objRs.Bookmark = varBookmark ' return to the bookmarked (sixth) record 
 End If 
 End If 
'EndBookmarkEg 
```

[Supports](supports-method-ado.md) メソッドの詳細については、後で説明します。

複製された **Recordset** の場合を除いて、同じコマンドを使用した場合でも、ブックマークが一意なのは作成された **Recordset** 内です。つまり、ある **Recordset** から取得した **Bookmark** を使用して、同じコマンドで開いた別の **Recordset** 内の同じレコードに移動することはできません。

