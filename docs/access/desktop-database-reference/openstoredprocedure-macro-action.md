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
ms.openlocfilehash: 22d3422a5c00e6caa20003df3574c26ab061ab53
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925346"
---
# <a name="openstoredprocedure-macro-action"></a>OpenStoredProcedure マクロ アクション


**適用されます**Access 2013、Office 2013。

Access プロジェクトで、"OpenStoredProcedure/ストアドプロシージャを開く" アクションを使用すると、データシート ビュー、ストアド プロシージャ デザイン ビュー、または印刷プレビューでストアド プロシージャを開くことができます。データシート ビューで開いた場合、その名前のストアド プロシージャが実行されます。ストアド プロシージャのデータ入力モードの設定を行ったり、表示するレコードを制限することができます。


> [!NOTE]
> <P>[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</P>



## <a name="setting"></a>設定値

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
<td><p>開くストアド プロシージャの名前です。 [<strong>プロシージャ名</strong>] ボックスに<strong>アクションの引数</strong>]、[マクロ ビルダー] ウィンドウのでは、現在のデータベースのすべてのストアド プロシージャを示しています。 この引数は省略できません。 ライブラリ データベースで、 <strong>OpenStoredProcedure</strong>アクションを含むマクロを実行すると、最初に検索の最初にライブラリ データベースで、し、[現在のデータベース内に同じ名前のストアド プロシージャ。</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>ストアド プロシージャを開くときのビューを指定します。[<strong>ビュー</strong>] ボックスで、[<strong>データシート ビュー</strong>]、[<strong>デザイン ビュー</strong>]、[<strong>印刷プレビュー</strong>]、[<strong>ピボットテーブル ビュー</strong>]、または [<strong>ピボットグラフ ビュー</strong>] をクリックします。既定値は [<strong>データシート ビュー</strong>] です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Data Mode/データ モード</strong></p></td>
<td><p>ストアド プロシージャを開くときのデータ入力モードを指定します。これはデータシート ビューで開いているストアド プロシージャにのみ適用されます。新しいレコードの追加を許可して、既存のレコードの編集を禁止する場合は [<strong>追加</strong>]、既存のレコードの編集および新しいレコードの追加を許可する場合は [<strong>編集</strong>]、レコードの表示のみを許可する場合は [<strong>読み取り専用</strong>] をクリックします。既定値は [<strong>編集</strong>] です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

このアクションの動作は、ナビゲーション ウィンドウでストアド プロシージャをダブルクリックした場合や、ナビゲーション ウィンドウでストアド プロシージャを右クリックして目的のコマンドをクリックした場合と同じです。

ストアド プロシージャが開いているときにデザイン ビューに切り替えると、ストアド プロシージャの "Data Mode/データ モード" 引数の設定は解除されます。再びデータシート ビューに切り替えても、元の設定には戻りません。


> [!TIP]
> <P></P>
> <UL>
> <LI>
> <P>ストアド プロシージャをナビゲーション ウィンドウで選択し、マクロのアクション行にドラッグすると、ストアド プロシージャをデータシート ビューで開く "OpenStoredProcedure/ストアドプロシージャを開く" アクションが自動的に作成されます。 >  ストアド プロシージャを実行すると、通常は、それがストアド プロシージャであること、および影響を受けるレコード数を示すシステム メッセージが表示されますが、これを表示しないようにするには、"SetWarning/メッセージの設定" アクションを使用します。 > ストアド プロシージャをナビゲーション ウィンドウで選択し、マクロのアクション行にドラッグすると、ストアド プロシージャをデータシート ビューで開く "OpenStoredProcedure/ストアドプロシージャを開く" アクションが自動的に作成されます。</P>
> <LI>
> <P>これらの表示を抑制するのに<STRONG>SetWarning</STRONG>アクションを使用するには (それがストアド プロシージャおよび影響を受けるレコードの数)、ストアド プロシージャを実行するときに表示されるシステム メッセージを表示したくない場合メッセージです。</P></LI></UL>
> <P></P>



Visual Basic for Applications (VBA) モジュールで "OpenStoredProcedure/ストアドプロシージャを開く" アクションを実行するには、 **DoCmd** オブジェクトの **OpenStoredProcedure** メソッドを使用します。

