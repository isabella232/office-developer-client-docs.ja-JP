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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709979"
---
# <a name="rundatamacro-macro-action"></a>RunDataMacro マクロ アクション

**適用されます**Access 2013、Office 2013。

**RunDataMacro**アクションを使用すると、名前付きデータ マクロを実行します。

## <a name="setting"></a>設定

" **RunDataMacro/データマクロの実行** " アクションの引数は次のとおりです。

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


## <a name="remarks"></a>解説

**RunDataMacro**アクションを使用すると、マクロ、名前付きデータ マクロでは、およびマクロの次のイベントの中で:**[マクロのイベントの後に削除](after-delete-macro-event.md)**、**[マクロのイベントの後に挿入](after-insert-macro-event.md)** と**[更新後のマクロのイベント](after-update-macro-event.md)** です。

データ マクロの名前は、それが関連付けられている (たとえば、 **Comments.AddComment**、 **AddComment**だけではなく) テーブルを含める必要があります。

マクロ デザイナーで実行するデータ マクロを選択すると、そのデータ マクロにパラメーターが必要であるかどうかが自動的に判断されます。パラメーターが必要な場合は、引数を入力するテキストボックスが表示されます。

**RunDataMacro**アクションを含むマクロを実行するし、 **RunDataMacro**アクションに到達して、data という名前のマクロが実行されます。 Data という名前のマクロが完了したら、アクセスが元に戻りし、次のアクションを実行します。

## <a name="example"></a>例

次の例では、名前付きデータ マクロにパラメーターを渡す方法を示します。 RunDataMacro アクションを使用して、tblServiceRequests テーブルの dmGetCurrentServiceRequest のデータ マクロが呼び出されます。 DmGetCurrentServiceRequest が完了したら、CurrentServiceRequest 変数には、フォームのデータ マクロは、txtCurrentSR テキスト ボックスに書き込まれますが返されます。

**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。

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
