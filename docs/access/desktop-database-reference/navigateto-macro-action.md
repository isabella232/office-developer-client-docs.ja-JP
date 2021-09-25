---
title: NavigateTo マクロ アクション
TOCTitle: NavigateTo macro action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 4bf5a40d1643861a438e4de4668d845c92ebb93f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577214"
---
# <a name="navigateto-macro-action"></a>NavigateTo マクロ アクション

**適用先:** Access 2013、Office 2013

You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane. For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.

## <a name="setting"></a>設定

"NavigateTo/移動先" アクションの引数は次のとおりです。

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
<td><p><strong>分類</strong></p></td>
<td><p>必ず指定します。ナビゲーション ウィンドウにオブジェクトを表示する際に使用するカテゴリを指定します。[<strong>カテゴリ</strong>] ボックスで [<strong>オブジェクトの種類</strong>]、[<strong>テーブルとビュー</strong>]、[<strong>更新日</strong>]、[<strong>作成日</strong>]、または [<strong>ユーザー設定</strong>] をクリックします。</p></td>
</tr>
<tr class="even">
<td><p><strong>グループ</strong></p></td>
<td><p>オプション。 "Group/グループ" 引数は、ナビゲーション ウィンドウ内のカテゴリに表示されるオブジェクトを制限します。 引数 Group を空白 <strong>のままに</strong> すると、ナビゲーション ウィンドウには、Category 引数で指定した条件に分類された、すべてのデータベース オブジェクトが <strong>表示</strong> されます。 次の表は、さまざまな "Category/カテゴリ" 引数で使用できる有効な "Group/グループ" 引数の例を示しています。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

- このアクションは、ナビゲーション ウィンドウのタイトル バーからカテゴリとグループを選択する場合と似ています。

- Valid **Group** arguments depend on which **Category** argument is used. If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.
    
  <table>
  <colgroup>
  <col style="width: 50%" />
  <col style="width: 50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th><p>引数 Category</p></th>
  <th><p>"Group/グループ" 引数の例</p></th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td><p>オブジェクトの種類</p></td>
  <td><p>テーブル、フォーム、クエリ、ページ、マクロ、モジュール</p></td>
  </tr>
  <tr class="even">
  <td><p>テーブルとビュー</p></td>
  <td><p>データベース内の特定のテーブルの名前</p></td>
  </tr>
  <tr class="odd">
  <td><p>更新日</p></td>
  <td><p>今日、昨日、先月、先月よりも前の日付</p></td>
  </tr>
  <tr class="even">
  <td><p>作成日</p></td>
  <td><p>今日、昨日、先月、先月よりも前の日付</p></td>
  </tr>
  <tr class="odd">
  <td><p>ユーザー設定のカテゴリ</p></td>
  <td><p>指定したユーザー設定のカテゴリに対応する作成済みグループの名前</p></td>
  </tr>
  </tbody>
  </table>

- To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.

> [!NOTE]
> To navigate to the top level of a category (for example, **All Tables**, **All Access Objects**, or **All Dates**), you must leave the Group argument blank. For example, when the **Category** argument is **Object Type**, entering **All Access Objects** as a **Group** argument results in an error.


