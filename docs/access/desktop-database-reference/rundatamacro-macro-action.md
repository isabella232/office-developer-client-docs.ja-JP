---
title: RunDataMacro マクロ アクション
TOCTitle: RunDataMacro macro action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: d24cf33bd9b5ced31ec7a71ce67efc70b26b5e02
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557793"
---
# <a name="rundatamacro-macro-action"></a>RunDataMacro マクロ アクション

**適用先:** Access 2013、Office 2013

"RunDataMacro/データマクロの実行" アクションを使用して、名前付きデータ マクロを実行できます。

## <a name="setting"></a>設定

"RunDataMacro/データマクロの実行" アクションの引数は次のとおりです。

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
<td><p>名前</p></td>
<td><p>実行するデータ マクロの名前</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

マクロ、名前付きデータ マクロ、および次のマクロ イベントで **RunDataMacro** アクション **[](after-delete-macro-event.md)** を使用できます。マクロ **[](after-insert-macro-event.md)** イベントの削除後、マクロの挿入後イベント、および更新後マクロ **[イベント](after-update-macro-event.md)** です。

データ マクロの名前には、アタッチするテーブル **(AddComment ではなく Comments.AddComment** など) を含める **必要があります**。

マクロ デザイナーで実行するデータ マクロを選択すると、そのデータ マクロにパラメーターが必要であるかどうかが自動的に判断されます。パラメーターが必要な場合は、引数を入力するテキストボックスが表示されます。

When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.

## <a name="example"></a>例

次の例は、名前付きデータ マクロにパラメーターを渡す方法を示しています。 tblServiceRequests テーブルの dmGetCurrentServiceRequest データ マクロは、RunDataMacro アクションを使用して呼び出されます。 dmGetCurrentServiceRequest が終了すると、データ マクロが txtCurrentSR テキスト ボックスに書き込まれた CurrentServiceRequest 変数が返されます。

**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```
