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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721851"
---
# <a name="selectobject-macro-action"></a>SelectObject マクロ アクション

**適用されます**Access 2013、Office 2013。

**SelectObject**アクションを使用すると、指定されたデータベース オブジェクトを選択します。

## <a name="setting"></a>設定値

**SelectObject**アクションには、次の引数があります。

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
<td><p>選択するオブジェクトの名前です。 [ <strong>オブジェクト名</strong> ] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。 これは、 <strong>[はい]</strong>に、ナビゲーション ウィンドウで引数を設定しない限り、必要な引数です。</p><p><strong>注</strong>: Access プロジェクト (.adp) の<STRONG>オブジェクト名</STRONG>] ボックスに<STRONG>サーバー ビュー</STRONG>、<STRONG>ダイアグラム</STRONG>、または<STRONG>ストアド プロシージャ</STRONG>のオブジェクトのオブジェクト名が表示されません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>In Navigation Pane/ナビゲーション ウィンドウ内</strong></p></td>
<td><p>Microsoft Access がオブジェクトをナビゲーション ウィンドウで選択するかどうかを指定します。ナビゲーション ウィンドウでオブジェクトを選択する場合は [<strong>はい</strong>] を、ナビゲーション ウィンドウでオブジェクトを選択しない場合は [<strong>いいえ</strong>] をクリックします。既定値は [<strong>いいえ</strong>] です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

**SelectObject**アクションは、フォーカスを受け取ることができるすべての Access オブジェクトで動作します。 このアクションは、指定したオブジェクトにフォーカスを提供し、オブジェクトを示して 場合は、非表示には。 オブジェクトがフォームの場合は、 **SelectObject**アクション **[はい]** に、フォームの**Visible**プロパティを設定して (たとえば、または作業ウィンドウ固定のポップアップ フォームの場合) として、フォームのプロパティで設定されているモードにフォームを返します。

オブジェクトが、ほかのウィンドウのいずれかで開いていない場合、 **[はい]** を**ナビゲーション ウィンドウで**引数を設定することによって選択のナビゲーション ウィンドウでできます。 **ナビゲーション ウィンドウ**に引数を**No**に設定するが表示されていないオブジェクトを選択しようとするときにエラー メッセージが表示されます。

多くの場合、追加アクションを実行するオブジェクトを選択するのには、このアクションを使用する場合があります。 たとえば、タブ付きドキュメントではなく重ねて表示されるウィンドウを使用するように構成にアクセスする場合がする (アクションを使用して**RestoreWindow** ) 最小化されているオブジェクトを復元するか、使用するオブジェクトを含むウィンドウを最大化(アクションを使用して、 **MaximizeWindow** )。

フォームを選択した場合は、フォーム上の特定の領域に移動する**GoToControl**、 **GoToRecord**、 **GoToPage**操作を使用できます。 **GoToRecord**アクションは、データシートにも有効です。

実行するには、 **SelectObject**アクションを Visual Basic for Applications (VBA) モジュールで**DoCmd**オブジェクトの**SelectObject**メソッドを使用します。

