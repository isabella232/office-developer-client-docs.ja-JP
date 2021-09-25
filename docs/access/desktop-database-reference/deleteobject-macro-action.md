---
title: DeleteObject マクロ アクション
TOCTitle: DeleteObject macro action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 32fcab6018adcdb40af56788a036154ce99a8ca6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553124"
---
# <a name="deleteobject-macro-action"></a>DeleteObject マクロ アクション

**適用先:** Access 2013、Office 2013

**DeleteObject** アクションを使用すると、指定したデータベース オブジェクトを削除できます。

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>Setting

**DeleteObject** アクションの引数は次のとおりです。

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
<td><p><strong>オブジェクトの種類</strong></p></td>
<td><p>削除するオブジェクトの種類を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>オブジェクトの種類</strong>] ボックスの一覧で [ <strong>テーブル</strong>]、[ <strong>クエリ</strong>]、[ <strong>フォーム</strong>]、[ <strong>レポート</strong>]、[ <strong>マクロ</strong>]、[ <strong>モジュール</strong>]、[ <strong>データ アクセス ページ</strong>]、[ <strong>サーバー ビュー</strong>]、[ <strong>ダイアグラム</strong>]、[ <strong>ストアド プロシージャ</strong>]、[ <strong>関数</strong>] のいずれかをクリックします。ナビゲーション ウィンドウで選択したオブジェクトを削除する場合は、この引数を指定しません。  </p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name/オブジェクト名</strong></p></td>
<td><p>削除するオブジェクトの名前を指定します。[ <strong>オブジェクト名</strong> ] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。[ <strong>オブジェクトの種類</strong> ] ボックスに何も指定しない場合は、このボックスにも何も指定しないでください。ライブラリ データベースで " <strong>DeleteObject/オブジェクトの削除</strong> " アクションが定義されているマクロを実行すると、この名前のオブジェクトが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。  </p></td>
</tr>
</tbody>
</table>

> [!WARNING]
> [!注意] [ **オブジェクトの種類** ] ボックスと [ **オブジェクト名** ] ボックスに値を指定しない場合、 **DeleteObject** アクションでは、ナビゲーション ウィンドウで選択したオブジェクトが削除されますが、削除を確認するメッセージは表示されません。

## <a name="remarks"></a>注釈

**DeleteObject** アクションを使って、マクロの実行中に一時的に作成したオブジェクトを削除できます。たとえば、 **OpenQuery** アクションを使用してテーブル作成クエリを実行し、一時的なテーブルを作成したとします。この一時的なテーブルは、使用し終わったら、 **DeleteObject** アクションを使用して削除できます。

このアクションの動作は、ナビゲーション ウィンドウでオブジェクトを選択して DEL キーを押した場合や、ナビゲーション ウィンドウでオブジェクトを右クリックして [ **削除**] をクリックした場合と同じです。

Visual Basic for Applications モジュールで **DeleteObject** アクションを実行するには、 **DoCmd** オブジェクトの **DeleteObject** メソッドを使用します。

