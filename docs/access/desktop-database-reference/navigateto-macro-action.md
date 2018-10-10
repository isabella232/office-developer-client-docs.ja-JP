---
title: "'NavigateTo/移動先' マクロ アクション"
TOCTitle: NavigateTo Macro Action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9a6a59b6c84e9814aeb9b4709d27955f29fd9e1e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477874"
---
# <a name="navigateto-macro-action"></a>"NavigateTo/移動先" マクロ アクション


**適用されます**Access 2013 |。Office 2013

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
<td><p><strong>Group</strong></p></td>
<td><p>省略可能。 カテゴリ内のオブジェクト、<strong>グループ</strong>引数の制限は、ナビゲーション ウィンドウに表示されます。 引数<strong>Group</strong>を空白のままにする場合、ナビゲーション ウィンドウには、引数<strong>Category</strong>で指定した条件によって分類されるすべてのデータベース オブジェクトが表示されます。 さまざまな<strong>カテゴリ</strong>の引数の有効な<strong>グループ</strong>の引数の例としては、次の表に表示されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

  - このアクションの動作は、ナビゲーション ウィンドウのタイトル バーからカテゴリやグループを選択した場合と同じです。

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
> <P>(<STRONG>すべてのテーブル</STRONG>、<STRONG>すべての Access オブジェクト</STRONG>、または<STRONG>すべての日付</STRONG>など) のカテゴリの最上位レベルに移動するにする必要があります、グループ引数を指定しません。 などの引数<STRONG>Category</STRONG> <STRONG>オブジェクトの種類</STRONG>がある場合は、エラー<STRONG>グループ</STRONG>引数の結果として<STRONG>すべての Access オブジェクト</STRONG>を入力します。</P>


