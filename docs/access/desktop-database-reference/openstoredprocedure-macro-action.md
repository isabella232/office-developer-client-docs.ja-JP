---
title: OpenStoredProcedure マクロ アクション
TOCTitle: OpenStoredProcedure macro action
ms:assetid: b14dbb82-7c8a-0ace-e251-46599551a490
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822003(v=office.15)
ms:contentKeyID: 48547142
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm187628
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 5da86224211362c4819f7f5a49e3509c900f319a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611882"
---
# <a name="openstoredprocedure-macro-action"></a>OpenStoredProcedure マクロ アクション

**適用先**: Access 2013、Office 2013

Access プロジェクトで、"OpenStoredProcedure/ストアドプロシージャを開く" アクションを使用すると、データシート ビュー、ストアド プロシージャ デザイン ビュー、または印刷プレビューでストアド プロシージャを開くことができます。データシート ビューで開いた場合、その名前のストアド プロシージャが実行されます。ストアド プロシージャのデータ入力モードの設定を行ったり、表示するレコードを制限することができます。

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>Setting

"OpenStoredProcedure/ストアドプロシージャを開く" アクションの引数は次のとおりです。

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
<td><p><strong>Procedure Name/プロシージャ名</strong></p></td>
<td><p>開くストアド プロシージャの名前を指定します。 [ <strong>マクロ ビルダー] ウィンドウの</strong> [ <strong>アクション引数</strong> ] セクションの [プロシージャ名] ボックスには、現在のデータベース内のすべてのストアド プロシージャが表示されます。 この引数は省略できません。 ライブラリ データベースで "OpenStoredProcedure/ストアドプロシージャを開く" アクションが定義されているマクロを実行すると、この名前のストアド プロシージャが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>表示</strong></p></td>
<td><p>ストアド プロシージャを開くときのビューを指定します。[<strong>ビュー</strong>] ボックスで、[<strong>データシート ビュー</strong>]、[<strong>デザイン ビュー</strong>]、[<strong>印刷プレビュー</strong>]、[<strong>ピボットテーブル ビュー</strong>]、または [<strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [<strong>データシート ビュー</strong>] です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Data Mode/データ モード</strong></p></td>
<td><p>ストアド プロシージャを開くときのデータ入力モードを指定します。これはデータシート ビューで開いているストアド プロシージャにのみ適用されます。新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [<strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [<strong>編集</strong>]、レコードの表示のみを許可する場合は [<strong>読み取り専用</strong>] をクリックします。既定値は [<strong>編集</strong>] です。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>注釈

このアクションの動作は、ナビゲーション ウィンドウでストアド プロシージャをダブルクリックした場合や、ナビゲーション ウィンドウでストアド プロシージャを右クリックして目的のコマンドをクリックした場合と同じです。

ストアド プロシージャが開いているときにデザイン ビューに切り替えると、ストアド プロシージャの "Data Mode/データ モード" 引数の設定は解除されます。再びデータシート ビューに切り替えても、元の設定には戻りません。

> [!TIP]
> - ストアド プロシージャをナビゲーション ウィンドウからマクロ アクション行にドラッグできます。 これにより、データシート ビューでストアド プロシージャを開く **OpenStoredProcedure** アクションが自動的に作成されます。
> - ストアド プロシージャを実行すると、通常は、それがストアド プロシージャであること、および影響を受けるレコード数を示すシステム メッセージが表示されますが、これを表示しないようにするには、"SetWarning/メッセージの設定" アクションを使用します。

**OpenStoredProcedure** アクションを Visual Basic for Applications (VBA) モジュールで実行するには **、DoCmd** オブジェクトの **OpenStoredProcedure** メソッドを使用します。

