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
localization_priority: Normal
ms.openlocfilehash: 55af2ce884b26b4c3df219e7d1986e7dc2e4c8ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288281"
---
# <a name="openvisualbasicmodule-macro-action"></a>OpenVisualBasicModule マクロ アクション

**適用先:** Access 2013、Office 2013

You can use the **OpenVisualBasicModule** action to open a specified Visual Basic for Applications (VBA) module at a specified procedure. This can be a Sub procedure, a Function procedure, or an event procedure.

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>設定値

"OpenVisualBasicModule/VisualBasicモジュールを開く" アクションの引数は次のとおりです。

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
<td><p>開くモジュールの名前を指定します。 データベースのすべての標準モジュールでプロシージャを検索して、そのプロシージャに適切なモジュールを開く場合は、この引数を指定しません。 ライブラリ データベースで "OpenVisualBasicModule/VisualBasicモジュールを開く" アクションが定義されているマクロを実行すると、この名前のモジュールが、最初にライブラリ データベースで検索され、次にカレント データベースで検索されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>Procedure Name/プロシージャ名</strong></p></td>
<td><p>モジュールを開いて表示するプロシージャの名前を指定します。この引数を省略すると、モジュールの宣言セクションが開きます。</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> "Module Name/モジュール名" 引数または有効な "プロシージャ名" 引数のいずれかに有効な名前を指定する必要があります。


## <a name="remarks"></a>注釈

You can use this action to open an event procedure by specifying the **Module Name** argument and the **Procedure Name** argument. たとえば、フォームの注文で **[** printinvoice] ボタンの click イベントプロシージャを開くには、" **Module name/名前**" 引数を [フォームに設定する] を指定し、 **"** **プロシージャ名**" 引数を**\_printinvoice クリック**に設定します。 To view the event procedure for a form or report, the form or report must be open.

同様に、クラス モジュールでプロシージャを開くには、モジュール名を指定する必要がありますが、そのクラス モジュールを開いておく必要はありません。

プライベート プロシージャを開くには、そのプロシージャを含むモジュールを開いておく必要があります。

このアクションの動作は、ナビゲーション ウィンドウでモジュールを右クリックして [ **デザイン ビュー**] をクリックした場合と同じです。このアクションを使用すると、プロシージャ名を指定して、データベースの標準モジュールで検索することもできます。

> [!TIP]
> You can select a module in the Navigation Pane and drag it to a macro action row. This automatically creates an **OpenVisualBasicModule** action that opens the module to the Declarations section.

To run the **OpenVisualBasicModule** action in a VBA module, use the **OpenModule** method of the **DoCmd** object.

