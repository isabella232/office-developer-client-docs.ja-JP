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
localization_priority: Normal
ms.openlocfilehash: 1c37e798e0624a5655b63a76332073e5b57c0823
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704141"
---
# <a name="navigateto-macro-action"></a>NavigateTo マクロ アクション

**適用されます**Access 2013、Office 2013。

**移動**操作を使用するには、ナビゲーション ウィンドウでデータベース オブジェクトの表示を制御します。 たとえば、データベース オブジェクトの分類方法を変更したり、フィルターを適用して特定のデータベース オブジェクトだけを表示したりできます。

## <a name="setting"></a>設定値

**移動**操作では、次の引数があります。

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
<td><p><strong>カテゴリ</strong></p></td>
<td><p>必ず指定します。ナビゲーション ウィンドウにオブジェクトを表示する際に使用するカテゴリを指定します。[<strong>カテゴリ</strong>] ボックスで [<strong>オブジェクトの種類</strong>]、[<strong>テーブルとビュー</strong>]、[<strong>更新日</strong>]、[<strong>作成日</strong>]、または [<strong>ユーザー設定</strong>] をクリックします。</p></td>
</tr>
<tr class="even">
<td><p><strong>グループ</strong></p></td>
<td><p>省略可能。 カテゴリ内のオブジェクト、<strong>グループ</strong>引数の制限は、ナビゲーション ウィンドウに表示されます。 引数<strong>Group</strong>を空白のままにする場合、ナビゲーション ウィンドウには、引数<strong>Category</strong>で指定した条件によって分類されるすべてのデータベース オブジェクトが表示されます。 さまざまな<strong>カテゴリ</strong>の引数の有効な<strong>グループ</strong>の引数の例としては、次の表に表示されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

- このアクションは、ナビゲーション ウィンドウのタイトル バーからカテゴリとグループを選択することに似ています。

- **グループ**の有効な引数は、どの**カテゴリ**の引数の使用によって異なります。 **グループ**の無効な引数を入力すると、エラー メッセージが表示されます。次の表には、各**カテゴリ**の引数に有効な**グループ**の引数の例が含まれています。
    
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

- VBA モジュールでは、**移動**操作を実行するには、 **DoCmd**オブジェクトの**NavigateTo**メソッドを使用します。

> [!NOTE]
> (**すべてのテーブル**、**すべての Access オブジェクト**、または**すべての日付**など) のカテゴリの最上位レベルに移動するにする必要があります、グループ引数を指定しません。 などの引数**Category** **オブジェクトの種類**がある場合は、エラー**グループ**引数の結果として**すべての Access オブジェクト**を入力します。


