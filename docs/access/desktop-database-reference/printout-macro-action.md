---
title: PrintOut マクロ アクション
TOCTitle: PrintOut macro action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 2cfb01c542134570b2ccc0ac2a0e31fd3599cc5c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585484"
---
# <a name="printout-macro-action"></a>PrintOut マクロ アクション

**適用先:** Access 2013、Office 2013

You can use the **PrintOut** action to print the active object in the open database. You can print datasheets, reports, forms, data access pages, and modules.

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>Setting

"PrintOut/印刷" アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Print Range/印刷範囲</strong></p></td>
<td><p>The range to print. Click <strong>All</strong> (the user can print all of the object), <strong>Selection</strong> (the user can print the part of the object that's selected), or <strong>Pages</strong> (the user can specify a range of pages in the <strong>Page From</strong> and <strong>Page To</strong> arguments) in the <strong>Print Range</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>All</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Page From/開始ページ</strong></p></td>
<td><p>印刷する最初のページを指定します。このページの先頭から印刷が開始されます。[ <strong>印刷範囲</strong>] ボックスで [ <strong>ページ指定</strong>] を選択した場合、この引数は省略できません。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Page To/終了ページ</strong></p></td>
<td><p>印刷する最後のページを指定します。このページの最後で印刷が終了します。[ <strong>印刷範囲</strong>] ボックスで [ <strong>ページ指定</strong>] を選択した場合、この引数は省略できません。  </p></td>
</tr>
<tr class="even">
<td><p><strong>Print Quality/印刷品質</strong></p></td>
<td><p>印刷の品質を指定します。[ <strong>高</strong>]、[ <strong>中</strong>]、[ <strong>低</strong>]、[ <strong>簡易</strong>] のいずれかをクリックします。印刷の品質が低いほど、速く印刷されます。既定値は [ <strong>高</strong>] です。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Copies/部数</strong></p></td>
<td><p>印刷部数を指定します。既定値は 1 です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Collate Copies/部単位で印刷</strong></p></td>
<td><p>Click <strong>Yes</strong> (collate the printed copies) or <strong>No</strong> (do not collate copies). The object may print faster if this argument is set to <strong>No</strong>. The default is <strong>Yes</strong>.  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

このアクションの動作は、オブジェクトを選択し、[ **ファイル**] タブをクリックして、[ **印刷**] をクリックした場合と同じです。ただし、このアクションを使用する場合は、[ **印刷**] ダイアログ ボックスは表示されません。

> [!TIP]
> If you have particular print settings you use frequently, create a macro containing a **PrintOut** action with these settings in its arguments.

The arguments for this action correspond to options in the **Print** dialog box. However, unlike the **FindRecord** action and **Find and Replace** dialog box, the argument settings aren't shared with the **Print** dialog box options.

To run the **PrintOut** action in a Visual Basic for Applications (VBA) module, use the **PrintOut** method of the **DoCmd** object.

