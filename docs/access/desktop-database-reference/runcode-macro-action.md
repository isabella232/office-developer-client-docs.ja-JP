---
title: RunCode マクロ アクション
TOCTitle: RunCode macro action
ms:assetid: cb0625be-4b5d-4927-9b0e-59a6e411b5bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834373(v=office.15)
ms:contentKeyID: 48547706
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm98700
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 646c1393cc798c1f827e6ceaebf46bfe7c87bcbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306833"
---
# <a name="runcode-macro-action"></a>RunCode マクロ アクション

**適用先:** Access 2013、Office 2013

**RunCode** アクションを使用すると、Visual Basic for Applications (VBA) の Function プロシージャを呼び出すことができます。

## <a name="setting"></a>Setting

**RunCode** アクションの引数は次のとおりです。

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
<td><p><strong>Function Name/関数名</strong></p></td>
<td><p>呼び出す VBA の Function プロシージャの名前を指定します。関数の引数はかっこ ( ) で囲みます。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>関数名</strong>] ボックスに関数名を入力します。この引数は省略できません。  </p><p><strong>注</strong>: Access データベース (.mdb または .accdb) では、[<strong>ビルド</strong>] ボタンをクリックすると、式ビルダーを使用してこの引数の関数を選択できます。 式ビルダーに表示される一覧で目的の関数をクリックします。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

ユーザー定義の Function プロシージャは、Microsoft Access のモジュールに格納されます。

次の例のように、Function プロシージャに引数を指定しない場合でも、かっこを付ける必要があります。

`TestFunction()`

イベントプロパティの設定に使用されるユーザー定義の関数名とは異なり、 **function name/関数名**引数の関数名の**=** 先頭には、等号 () は付けません。

関数の戻り値は無視されます。

> [!NOTE]
> [!メモ] 関数名とモジュール名が同じ場合、マクロから Function プロシージャを呼び出すことはできません。

> [!TIP]
> [!ヒント] Visual Basic で記述した Sub プロシージャまたはイベント プロシージャを実行するには、Sub プロシージャまたはイベント プロシージャを呼び出す Function プロシージャを作成します。その後、 **RunCode** アクションを使用して、Function プロシージャを実行します。

**RunCode** アクションを使用して関数を呼び出すと、 **Function Name/関数名** 引数で指定した名前の関数が、データベースの標準モジュールで検索されます。ただし、フォームまたはレポートでメニュー コマンドをクリックしてこのアクションを実行した場合や、フォームまたはレポートのイベントに応じてこのアクションが実行された場合、この関数は、最初にフォームまたはレポートのクラス モジュールで検索され、次に標準モジュールで検索されます。 **Function Name/関数名** 引数で指定した関数は、ナビゲーション ウィンドウの [ **モジュール**] 領域に表示されるクラス モジュールでは検索されません。

このアクションは VBA モジュールでは使用できません。VBA では、目的の Function プロシージャを直接実行してください。

