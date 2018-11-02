---
title: OpenVisualBasicModule マクロ アクション
TOCTitle: OpenVisualBasicModule macro action
ms:assetid: 26eb31c8-3c65-b17d-46cd-c8967434a7a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191906(v=office.15)
ms:contentKeyID: 48543826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50916
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7d3d2d5f76e087e428bc9211805c524ebe5247d9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930449"
---
# <a name="openvisualbasicmodule-macro-action"></a>OpenVisualBasicModule マクロ アクション


**適用されます**Access 2013、Office 2013。

開くには、指定された Visual Basic for Applications (VBA) モジュールは、指定されたプロシージャでは、 **OpenVisualBasicModule**アクションを使用できます。 指定できるのは、Sub プロシージャ、Function プロシージャ、およびイベント プロシージャです。


> [!NOTE]
> <P>[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</P>



## <a name="setting"></a>設定値

**OpenVisualBasicModule**アクションには、次の引数があります。

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
<td><p><strong>Module Name/モジュール名</strong></p></td>
<td><p>開くモジュールの名前。 できますこの引数を指定しない場合は、プロシージャがデータベース内のすべての標準モジュールを検索し、そのプロシージャに適切なモジュールを開きます。 ライブラリ データベースで、 <strong>OpenVisualBasicModule</strong>アクションを含むマクロを実行する場合は、最初の検索にライブラリ データベースで、し、[現在のデータベース内に同じ名前のモジュールです。</p></td>
</tr>
<tr class="even">
<td><p><strong>Procedure Name/プロシージャ名</strong></p></td>
<td><p>モジュールを開いて表示するプロシージャの名前を指定します。この引数を省略すると、モジュールの宣言セクションが開きます。</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><STRONG>モジュール名</STRONG>や<STRONG>プロシージャ名</STRONG>のいずれかの引数に有効な名前を入力してください。</P>



## <a name="remarks"></a>解説

**モジュール名**の引数は、**プロシージャ名**の引数を指定することによって、イベント プロシージャを開くには、このアクションを使用できます。 などを注文フォームの [PrintInvoice] ボタンの**Click**イベント プロシージャを開くには、**モジュール名**の引数を**Form.Orders**に設定し、**プロシージャ名**の引数を設定**PrintInvoice\_をクリックして**。 フォームまたはレポートが、フォームまたはレポートのイベント プロシージャを表示するには、開く必要があります。

同様に、クラス モジュールでプロシージャを開くには、モジュール名を指定する必要がありますが、そのクラス モジュールを開いておく必要はありません。

プライベート プロシージャを開くには、そのプロシージャを含むモジュールを開いておく必要があります。

このアクションの動作は、ナビゲーション ウィンドウでモジュールを右クリックして [ **デザイン ビュー**] をクリックした場合と同じです。このアクションを使用すると、プロシージャ名を指定して、データベースの標準モジュールで検索することもできます。


> [!TIP]
> <P>ナビゲーション ウィンドウでモジュールを選択し、マクロのアクション行にドラッグできます。 宣言セクションには、モジュールを開く<STRONG>OpenVisualBasicModule</STRONG>アクションが自動的に作成します。</P>



VBA モジュールでは、 **OpenVisualBasicModule**アクションを実行するには、 **DoCmd**オブジェクトの**OpenModule**メソッドを使用します。

