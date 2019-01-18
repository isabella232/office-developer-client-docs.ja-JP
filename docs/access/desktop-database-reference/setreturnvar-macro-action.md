---
title: SetReturnVar マクロ アクション
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e0c849fc507d535807bc088e667acd74410ddd8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708159"
---
# <a name="setreturnvar-macro-action"></a>SetReturnVar マクロ アクション

**適用されます**Access 2013、Office 2013。

" **SetReturnVar/戻り変数の設定** " アクションは、戻り変数を作成し、それを特定の値に設定します。

> [!NOTE]
> [!メモ] " **SetReturnVar/戻り変数の設定** " アクションは、データ マクロでのみ使用できます。

## <a name="setting"></a>設定

" **SetReturnVar/戻り変数の設定** " アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>必須</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>名前</p></td>
<td><p>はい</p></td>
<td><p>変数の名前を指定する文字列。</p></td>
</tr>
<tr class="even">
<td><p>演算</p></td>
<td><p>はい</p></td>
<td><p>この一時変数の値を設定に使用する式を指定します。 式の前に等号 (=) を付けないでください。 この引数を設定するのには、<strong>式ビルダー</strong>を使用するのには [<strong>ビルド</strong>] ボタンをクリックすることができます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

" **SetReturnVar/戻り変数の設定** " アクションを使用して、 **ReturnVar** を作成します。この変数は、" **RunDataMacro/データマクロの実行** " アクションを使用してデータ マクロを呼び出すマクロが使用できます。

" **SetReturnVar/戻り変数の設定** " アクションによって **ReturnVar** が作成されたら、呼び出し元のマクロは式でその変数を使用できます。たとえば、 **UpdateSuccess** という名前の **ReturnVar** を作成した場合は、次の構文を使用して変数を使用できます。

```vb
    =[ReturnVars]![UpdateSuccess]
```

" **SetReturnVar/戻り変数の設定** " アクションは、指定されたデータ マクロでのみ使用できます。データ マクロ イベントに接続されたデータ マクロでは使用できません。

## <a name="example"></a>例

次の例は、 SetReturnVar アクションを使用して名前付きデータ マクロから値を返す方法を示します。" CurrentServiceRequest" という名前の **ReturnVar** が、名前付きデータ マクロの呼び出し元であるマクロまたは Visual Basic for Applications (VBA) サブルーチンに返されます。

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
