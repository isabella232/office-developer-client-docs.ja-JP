---
title: "'RunDataMacro/データマクロの実行' マクロ アクション"
TOCTitle: RunDataMacro Macro Action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6777ae05d2ab7455016df834d17abb3406a2d710
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889925"
---
# <a name="rundatamacro-macro-action"></a>"RunDataMacro/データマクロの実行" マクロ アクション

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


## <a name="remarks"></a>備考

**RunDataMacro**アクションを使用すると、マクロ、名前付きデータ マクロでは、およびマクロの次のイベントの中で:**[マクロ イベントの削除後](after-delete-macro-event.md)**、**[マクロ イベントの挿入後](after-insert-macro-event.md)**、**[更新後のマクロ イベント](after-update-macro-event.md)** です。

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
