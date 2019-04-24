---
title: SelectObject マクロ アクション
TOCTitle: SelectObject macro action
ms:assetid: a90539a0-c5a0-e997-9c25-e0972d28f2a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821420(v=office.15)
ms:contentKeyID: 48546914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm41840
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6287bc8a66858d51d65c37477eed7a86cd7839af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308730"
---
# <a name="selectobject-macro-action"></a>SelectObject マクロ アクション

**適用先:** Access 2013、Office 2013

"SelectObject/オブジェクトの選択" アクションを使用すると、指定したデータベース オブジェクトを選択できます。

## <a name="setting"></a>Setting

"SelectObject/オブジェクトの選択" アクションの引数は次のとおりです。

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
<td><p><strong>Object Type/オブジェクトの種類</strong></p></td>
<td><p>選択するデータベース オブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>オブジェクトの種類</strong>] ボックスで、[<strong>テーブル</strong>]、[<strong>クエリ</strong>]、[<strong>フォーム</strong>]、[<strong>レポート</strong>]、[<strong>マクロ</strong>]、[<strong>モジュール</strong>]、[<strong>データ アクセス ページ</strong>]、[<strong>サーバー ビュー</strong>]、[<strong>ダイアグラム</strong>]、[<strong>ストアド プロシージャ</strong>]、[<strong>関数</strong>] のいずれかをクリックします。この引数は省略できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>オブジェクト名</strong></p></td>
<td><p>選択するオブジェクトの名前を指定します。 [ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、 <strong>Object Type/オブジェクトの種類</strong> 引数で選択した種類のオブジェクトがすべて表示されます。 "In Navigation Pane/ナビゲーションウィンドウ" 引数を<strong>[Yes/はい]</strong>に設定しない限り、この引数は省略できません。</p><p><strong>注</strong>:<STRONG>サーバービュー</STRONG>、<STRONG>ダイアグラム</STRONG>、または<STRONG>ストアドプロシージャ</STRONG>オブジェクトのオブジェクト名は、Access プロジェクト (.adp) の [<STRONG>オブジェクト名</STRONG>] ボックスには表示されません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>In Navigation Pane/ナビゲーション ウィンドウ内</strong></p></td>
<td><p>Microsoft Access がオブジェクトをナビゲーション ウィンドウで選択するかどうかを指定します。ナビゲーション ウィンドウでオブジェクトを選択する場合は [<strong>はい</strong>] を、ナビゲーション ウィンドウでオブジェクトを選択しない場合は [<strong>いいえ</strong>] をクリックします。既定値は [<strong>いいえ</strong>] です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

The **SelectObject** action works with any Access object that can receive the focus. This action gives the specified object the focus and shows the object if it's hidden. If the object is a form, the **SelectObject** action sets the form's **Visible** property to **Yes** and returns the form to the mode set by its form properties (for example, as a modal or pop-up form).

If the object isn't open in one of the other Access windows, you can select it in the Navigation Pane by setting the **In Navigation Pane** argument to **Yes**. If you set the **In Navigation Pane** argument to **No**, an error message appears when you try to select an object that isn't open.

Often, you might use this action to select an object on which you want to perform additional actions. For example, if you have Access configured to use overlapping windows instead of tabbed documents, you may want to restore an object that has been minimized (by using the **RestoreWindow** action) or maximize a window that contains an object you want to work with (by using the **MaximizeWindow** action).

If you select a form, you can use the **GoToControl**, **GoToRecord**, and **GoToPage** actions to move to specific areas on the form. The **GoToRecord** action also works for datasheets.

To run the **SelectObject** action in a Visual Basic for Applications (VBA) module, use the **SelectObject** method of the **DoCmd** object.

