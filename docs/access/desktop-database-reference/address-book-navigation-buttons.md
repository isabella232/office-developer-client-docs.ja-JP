---
title: アドレス帳の移動ボタン
TOCTitle: Address Book navigation buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7c87acd433df4a303c1e6a15a60184cadf994c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282465"
---
# <a name="address-book-navigation-buttons"></a>アドレス帳の移動ボタン

**適用先:** Access 2013、Office 2013

アドレス帳アプリケーションでは、web ページの下部にあるナビゲーションボタンが表示されます。 ナビゲーション ボタンを使ってデータの最初または最後の行、あるいは現在の行の前後にある行を選択することにより、HTML のグリッド表示内でデータ間を移動できます。

## <a name="navigation-sub-procedures"></a>ナビゲーションのサブ プロシージャ

Address Book アプリケーションには、ユーザーが [First]、[Next]、[Previous]、および [Last] の各ボタンをクリックしてデータ間を移動できるようにする複数のプロシージャが含まれています。

たとえば、**最初**のボタンをクリックすると、VBScript\_の最初の OnClick Sub プロシージャがアクティブになります。 The procedure executes a [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, which makes the first row of data the current selection. **最後**のボタンをクリックすると\_、 [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md)メソッドが呼び出され、その最後の行のデータが現在の選択範囲になる直前の OnClick Sub プロシージャがアクティブになります。 The remaining navigation buttons work in a similar fashion.

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

