---
title: 不一致データのブロック
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d53bb8b6e4520810b98bfe81c9d35186a2392904
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928594"
---
# <a name="lookuprecord-data-block"></a>不一致データのブロック

**適用されます**Access 2013、Office 2013。

**LookupRecord** データ ブロックは、特定のレコードに対して一連のアクションを実行します。

> [!NOTE]
> [!メモ] **LookupRecord** データ ブロックは、データ マクロでのみ使用できます。

## <a name="setting"></a>設定

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
<td><p>操作対象のレコードを識別する文字列です。 <em></em>引数は、テーブル、選択クエリ、または SQL ステートメントの名前を含めることができます。</p>

> [!NOTE]
> 指定したレコードには、リンク テーブルまたは ODBC データ ソース内のデータを含めることはできません。


<p></p></td>
</tr>
<tr class="even">
<td><p>Where Condition/Where 条件式</p></td>
<td><p>いいえ</p></td>
<td><p><strong>LookupRecord</strong> データ ブロックを適用するデータの範囲を制限するための文字列式を指定します。たとえば、多くの場合、抽出条件は SQL 式の WHERE 句と同じ役割を果たします (ただし WHERE という語は使用しません)。抽出条件を省略すると、<strong>LookupRecord</strong> データ ブロックは <em>In</em> 引数で指定したドメイン全体に適用されます。抽出条件に含めるフィールドは、<em>In</em> にも含まれている必要があります。</p></td>
</tr>
<tr class="odd">
<td><p>エイリアス</p></td>
<td><p>いいえ</p></td>
<td><p><em></em>引数で指定されたレコードに別の名前を提供する文字列です。 あいまいな参照を防ぐへの参照のテーブル名を短くには、よく使用されます。 <em>エイリアス</em>が指定されていない場合、テーブルまたはクエリの名前がエイリアスとして使用します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>備考

** *条件*引数で指定した抽出条件は、複数のレコードを指定する場合、**不一致**のデータ ブロック、最初のレコードにのみ動作します。

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

<br/>

次の例は、" RaiseError" アクションを使用して Before Change データ マクロ イベントを取り消す方法を示します。 AssignedTo フィールドが更新されると、 LookupRecord データ ブロックを使用して、割り当てられた技術者が未解決サービス リクエストに現在割り当てられているかどうかが確認されます。これが真の場合、 Before Change イベントが取り消されて、レコードは更新されません。

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
