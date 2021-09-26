---
title: SetDisplayedCategories マクロ アクション
TOCTitle: SetDisplayedCategories macro action
ms:assetid: e8bf39a6-c639-2232-7b21-3b0badf37e4b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836053(v=office.15)
ms:contentKeyID: 48548429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm20026
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 16467b8b471111a7210678526e3230726ce5447d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621858"
---
# <a name="setdisplayedcategories-macro-action"></a>SetDisplayedCategories マクロ アクション


**適用先**: Access 2013、Office 2013

You can use the **SetDisplayedCategories** action to specify which categories are displayed under **Navigate to Category** in the title bar of the Navigation Pane. For example, if you want to prevent users from switching the Navigation Pane so that it displays objects sorted by **Created Date**, you can use this action to hide that option in the title bar's drop-down list.

## <a name="setting"></a>設定

"SetDisplayedCategories/表示されるカテゴリの設定" アクションの引数は次のとおりです。

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
<td><p><strong>Show</strong></p></td>
<td><p>カテゴリを表示する場合は [<strong>はい</strong>] を選択します。カテゴリを非表示にする場合は [<strong>いいえ</strong>] を選択します。</p></td>
</tr>
<tr class="even">
<td><p><strong>分類</strong></p></td>
<td><p>表示または非表示にするカテゴリの名前を入力または選択します。すべてのカテゴリを表示または非表示にする場合は、この引数を指定しないでください。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

  - ナビゲーション ウィンドウのタイトル バーに表示される標題は、現在アクティブなフィルター (使用されている場合) を示します。タイトル バーの任意の場所をクリックすると、ドロップダウン リストが表示されます。[ **カテゴリに移動**] の下に、このマクロ アクションが制御する項目が表示されます。

  - This action only enables or disables the display of the specified category or categories; it does not perform any switching of the Navigation Pane display. For example, if you are displaying objects sorted by **Creation Date** and you use the **SetDisplayedCategories** action to disable the **Creation Date** option, Access does not switch the Navigation Pane to another category.

  - To run the **SetDisplayedCategories** action in a VBA module, use the **SetDisplayedCategories** method of the **DoCmd** object.

