---
title: LookupRecord データブロック
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 920f0830a310452962eb5dd1c21be63215bf0f03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289792"
---
# <a name="lookuprecord-data-block"></a>LookupRecord データブロック

**適用先:** Access 2013、Office 2013

A **LookupRecord** data block performs a set of actions on a specific record.

> [!NOTE]
> LookupRecord  データ ブロックは、データ マクロでのみ使用できます。

## <a name="setting"></a>Setting

**LookupRecord** アクションの引数は次のとおりです。

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
<td><p>In</p></td>
<td><p>はい</p></td>
<td><p>操作するレコードを識別する文字列を指定します。<em></em>In 引数にはテーブルの名前、選択クエリ、または SQL ステートメントが含まれます。</p><p><strong>注</strong>: 指定されたレコードには、リンクテーブルまたは ODBC データソースに格納されているデータを含めることはできません。</p></td>
</tr>
<tr class="even">
<td><p>Where Condition/Where 条件式</p></td>
<td><p>いいえ</p></td>
<td><p><strong>LookupRecord</strong> データ ブロックを適用するデータの範囲を制限するための文字列式を指定します。たとえば、多くの場合、抽出条件は SQL 式の WHERE 句と同じ役割を果たします (ただし WHERE という語は使用しません)。抽出条件を省略すると、<strong>LookupRecord</strong> データ ブロックは <em>In</em> 引数で指定したドメイン全体に適用されます。抽出条件に含めるフィールドは、<em>In</em> にも含まれている必要があります。</p></td>
</tr>
<tr class="odd">
<td><p>エイリアス</p></td>
<td><p>いいえ</p></td>
<td><p><em></em>In 引数で指定したレコードの別名となる文字列。以降の参照用にテーブル名を短くして、あいまいな参照を防ぐ目的でよく使用されます。<em></em>Alias が指定されていない場合、表またはクエリ名前がエイリアスとして使用されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

*In* 引数および "*Where Condition/Where 条件式*" 引数で指定した条件に複数のレコードが該当する場合、**LookupRecord** データ ブロックは 1 つ目のレコードにのみ適用されます。

## <a name="example"></a>例

次の例は、 SetReturnVar アクションを使用して名前付きデータ マクロから値を返す方法を示します。 " CurrentServiceRequest" という名前の **ReturnVar** が、名前付きデータ マクロの呼び出し元であるマクロまたは Visual Basic for Applications (VBA) サブルーチンに返されます。

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

<br/>

次の例は、" RaiseError" アクションを使用して Before Change データ マクロ イベントを取り消す方法を示します。 AssignedTo フィールドが更新されると、 LookupRecord データ ブロックを使用して、割り当てられた技術者が未解決サービス リクエストに現在割り当てられているかどうかが確認されます。 これが真の場合、 Before Change イベントが取り消されて、レコードは更新されません。

```vb
    /* Get the name of the technician  */
    Look Up A Record In tblTechnicians
        Where Condition =[tblTechnicians].[ID]=[tblServiceRequests].[AssignedTo]
    SetLocalVar
        Name TechName
        Expression [tblTechnicians].[FirstName] & " " & [tblTechnicians].[LastName]
    /* End LookUpRecord  */
    
    If Updated("AssignedTo") Then
        Look Up A Record In tblServiceRequests
            Where Condition SR.[AssignedTo]=tblServiceRequests[AssignedTo] And 
                SR.[ID]<>tblServiceRequests.[ID] And IsNull(SR.[ActualCompletionDate])
            Alias SR
            RaiseError
                Error Number 1234
                Error Description ="Cannot assign a request to the specified technician: " & [TechName]
    
    End If
```
