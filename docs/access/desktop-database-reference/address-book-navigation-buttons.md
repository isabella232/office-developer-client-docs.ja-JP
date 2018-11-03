---
title: アドレス帳のナビゲーション ボタン
TOCTitle: Address Book navigation buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d1a8caae94bf56532b45dcfa3e647ba092552795
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947554"
---
# <a name="address-book-navigation-buttons"></a>アドレス帳のナビゲーション ボタン

**適用されます**Access 2013、Office 2013。

アドレス帳アプリケーションでは、web ページの下部にあるナビゲーション ボタンが表示されます。 ナビゲーション ボタンを使ってデータの最初または最後の行、あるいは現在の行の前後にある行を選択することにより、HTML のグリッド表示内でデータ間を移動できます。

## <a name="navigation-sub-procedures"></a>ナビゲーションのサブ プロシージャ

アドレス帳アプリケーションは、ユーザーが、**最初**、**次****前**、および**最後**のボタンのデータを移動する] をクリックしてできるようにするいくつかの手順を説明します。

たとえば、最初の VBScript をアクティブに**最初**のボタンをクリックすると\_OnClick Sub プロシージャです。 プロシージャは、データの現在の選択範囲の最初の行では、 [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md)メソッドを実行します。 アクティブに最後の**最後**のボタンをクリックすると\_OnClick Sub プロシージャは、データの最後の行の現在の選択範囲を作成、 [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md)メソッドを呼び出します。 他のナビゲーション ボタンは、同様の方法で動作します。

```vb 
 
' Move to the first record in the bound Recordset. 
Sub First_OnClick 
 DC1.Recordset.MoveFirst 
End Sub 
 
' Move to the next record from the current position 
' in the bound Recordset. 
Sub Next_OnClick 
 If Not DC1.Recordset.EOF Then ' Cannot move beyond bottom record. 
 DC1.Recordset.MoveNext 
 Exit Sub 
 End If 
End Sub 
 
' Move to the previous record from the current position in the bound 
' Recordset. 
Sub Prev_OnClick 
 If Not DC1.Recordset.BOF Then ' Cannot move beyond top record. 
 DC1.Recordset.MovePrevious 
 Exit Sub 
 End If 
End Sub 
 
' Move to the last record in the bound Recordset. 
Sub Last_OnClick 
 DC1.Recordset.MoveLast 
End Sub 
```

