---
title: "'SetDisplayedCategories/表示されるカテゴリの設定' マクロ アクション"
TOCTitle: SetDisplayedCategories Macro Action
ms:assetid: e8bf39a6-c639-2232-7b21-3b0badf37e4b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836053(v=office.15)
ms:contentKeyID: 48548429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm20026
f1_categories:
- Office.Version=v15
ms.openlocfilehash: af4b491ff76a28c998e1ec195a861dbf065d36c8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478946"
---
# <a name="setdisplayedcategories-macro-action"></a>"SetDisplayedCategories/表示されるカテゴリの設定" マクロ アクション


**適用されます**Access 2013 |。Office 2013

**SetDisplayedCategories**アクションを使用すると、カテゴリ**のカテゴリに移動**] の下のナビゲーション ウィンドウのタイトル バーに表示を指定します。 などのオブジェクトは**作成日**順が表示されるように、ナビゲーション ウィンドウを切り替えられないようにする場合は、タイトル バーのドロップダウン リスト内のオプションを非表示にする、このアクションを使用できます。

## <a name="setting"></a>設定値

**SetDisplayedCategories**アクションには、次の引数があります。

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
<td><p><strong>カテゴリ</strong></p></td>
<td><p>表示または非表示にするカテゴリの名前を入力または選択します。すべてのカテゴリを表示または非表示にする場合は、この引数を指定しないでください。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

  - ナビゲーション ウィンドウのタイトル バーに表示される標題は、現在アクティブなフィルター (使用されている場合) を示します。タイトル バーの任意の場所をクリックすると、ドロップダウン リストが表示されます。[ **カテゴリに移動**] の下に、このマクロ アクションが制御する項目が表示されます。

  - のみこの操作を有効またはカテゴリは、指定したカテゴリの表示を無効になります。任意のナビゲーション ウィンドウの表示の切り替えを行うことはできません。 などのオブジェクトは**作成日**順に表示している**SetDisplayedCategories**アクションを使用して、[**作成日**] オプションを無効にする場合は、アクセス、ナビゲーション ウィンドウに切り替わらない別のカテゴリ。

  - **SetDisplayedCategories**アクションは、VBA モジュールで実行するには、 **DoCmd**オブジェクトの**SetDisplayedCategories**メソッドを使用します。

