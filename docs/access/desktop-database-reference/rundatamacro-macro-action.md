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
localization_priority: Normal
ms.openlocfilehash: 32945f0822682a9432d75ed1ac59117dde3cc0e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306812"
---
# <a name="rundatamacro-macro-action"></a>RunDataMacro マクロ アクション

**適用先:** Access 2013、Office 2013

"RunDataMacro/データマクロの実行" アクションを使用して、名前付きデータ マクロを実行できます。

## <a name="setting"></a>Setting

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

**RunDataMacro**アクションは、マクロ、マクロの名前付きデータマクロ、およびマクロイベントの終了後**[](after-delete-macro-event.md)**、マクロイベントの**[挿入](after-insert-macro-event.md)** 後、および更新後**[マクロイベント](after-update-macro-event.md)** の後に使用できます。

データマクロの名前には、追加先のテーブルを含める必要があります (たとえば、addcomment だけではなく****、**コメント**など)。

マクロ デザイナーで実行するデータ マクロを選択すると、そのデータ マクロにパラメーターが必要であるかどうかが自動的に判断されます。パラメーターが必要な場合は、引数を入力するテキストボックスが表示されます。

When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action.

## <a name="example"></a>例

次の例は、名前付きデータマクロにパラメーターを渡す方法を示しています。 tblServiceRequests テーブルの dmGetCurrentServiceRequest data マクロは、RunDataMacro アクションを使用して呼び出されます。 dmGetCurrentServiceRequest が完了すると、CurrentServiceRequest 変数が返された形式で、データマクロが txtcurrentsr テキストボックスに書き込まれます。

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
