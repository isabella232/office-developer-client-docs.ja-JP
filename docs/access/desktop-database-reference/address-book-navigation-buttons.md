---
title: Address Book のナビゲーション ボタン
TOCTitle: Address Book Navigation Buttons
ms:assetid: 4ec32c08-5b35-8dce-23ec-0daa4db551cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249253(v=office.15)
ms:contentKeyID: 48544765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d68a15873bc5030fd51e54c2219a0ffd91f080f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478361"
---
# <a name="address-book-navigation-buttons"></a><span data-ttu-id="0cd0a-102">Address Book のナビゲーション ボタン</span><span class="sxs-lookup"><span data-stu-id="0cd0a-102">Address Book Navigation Buttons</span></span>


<span data-ttu-id="0cd0a-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="0cd0a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0cd0a-p101">Address Book アプリケーションでは、Web ページの一番下にナビゲーション ボタンが表示されます。ナビゲーション ボタンを使ってデータの最初または最後の行、あるいは現在の行の前後にある行を選択することにより、HTML のグリッド表示内でデータ間を移動できます。</span><span class="sxs-lookup"><span data-stu-id="0cd0a-p101">The Address Book application displays the navigation buttons at the bottom of the Web page. You can use the navigation buttons to navigate through the data in the HTML grid display by selecting either the first or last row of data, or rows adjacent to the current selection.</span></span>

## <a name="navigation-sub-procedures"></a><span data-ttu-id="0cd0a-106">ナビゲーションのサブ プロシージャ</span><span class="sxs-lookup"><span data-stu-id="0cd0a-106">Navigation Sub Procedures</span></span>

<span data-ttu-id="0cd0a-107">アドレス帳アプリケーションは、ユーザーが、**最初**、**次\*\*\*\*前**、および**最後**のボタンのデータを移動する] をクリックしてできるようにするいくつかの手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="0cd0a-107">The Address Book application contains several procedures that allow users to click the **First**, **Next**, **Previous**, and **Last** buttons to move around the data.</span></span>

<span data-ttu-id="0cd0a-108">たとえば、最初の VBScript をアクティブに**最初**のボタンをクリックすると\_OnClick Sub プロシージャです。</span><span class="sxs-lookup"><span data-stu-id="0cd0a-108">For example, clicking the **First** button activates the VBScript First\_OnClick Sub procedure.</span></span> <span data-ttu-id="0cd0a-109">プロシージャは、データの現在の選択範囲の最初の行では、 [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md)メソッドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0cd0a-109">The procedure executes a [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, which makes the first row of data the current selection.</span></span> <span data-ttu-id="0cd0a-110">アクティブに最後の**最後**のボタンをクリックすると\_OnClick Sub プロシージャは、データの最後の行の現在の選択範囲を作成、 [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0cd0a-110">Clicking the **Last** button activates the Last\_OnClick Sub procedure, which invokes the [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-rds.md) method, making the last row of data the current selection.</span></span> <span data-ttu-id="0cd0a-111">他のナビゲーション ボタンは、同様の方法で動作します。</span><span class="sxs-lookup"><span data-stu-id="0cd0a-111">The remaining navigation buttons work in a similar fashion.</span></span>

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

