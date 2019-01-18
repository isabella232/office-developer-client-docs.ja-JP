---
title: Before Change マクロ イベント
TOCTitle: Before Change macro event
ms:assetid: da456d55-a773-abeb-1fac-ef58e3331cb5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835322(v=office.15)
ms:contentKeyID: 48548077
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm19867
dev_langs:
- xml
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b37fb96ddfeaabc97c6f445f8951876e8026fbfe
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703959"
---
# <a name="before-change-macro-event"></a>Before Change マクロ イベント

**適用されます**Access 2013、Office 2013。

**変更する前に**イベントは、レコードが変更されたとき、変更がコミットされる前に発生します。

> [!NOTE]
> **変更**する前にイベントは、データ マクロでのみ使用します。

## <a name="remarks"></a>備考

レコードの前に発生する操作を実行**する前に変更**イベントを使用して変更されます。 **変更**する前に、検証を実行して、カスタム エラー メッセージが発生する通常使用されます。

**更新 (以下「*フィールド名*」)** 関数を使用すると、フィールドが変更されたかどうかを判断します。 次のコード例では、PaidInFull フィールドが変更されたかどうかを決定する**If**ステートメントを使用する方法を示します。

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

によって作成される新しいレコード**を変更する前に**イベントを発生するかどうか、または既存のレコードへの変更を確認するのにには、 **IsInsert**プロパティを使用します。 **IsInsert** en の既存のレコードへの変更によってイベントが発生した場合、新しいレコードでは、 **false を指定**して、イベントが発生した場合**は True**プロパティが含まれます。

次のコード例は、 **IsInsert**プロパティを使用するための構文を示しています。

```vb
    If   [IsInsert] = True   Then 
     
       /*  Actions for validating a new record go here.       */ 
     
    Else 
     
       /* Actions for processing a changed record go here.    */ 
     
    End If
```

次の構文を使用して、フィールド内の以前の値にアクセスできます。

```vb
    [Old].[Field Name]
```

たとえば、QuantityInStock フィールド内の以前の値にアクセスするには、次の構文を使用します。

```vb
    [Old].[QuantityInStock]
```

以前の値は、**変更**する前にイベントが終了すると完全に削除されます。

**RaiseError**アクションを使用して**変更**する前にイベントをキャンセルできます。 エラーが発生したとき、**変更**する前にイベントに含まれる変更は破棄されます。

**変更**する前にイベントで使用できるマクロのコマンドを次の表に一覧します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>コマンドの種類</p></th>
<th><p>コマンド</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>プログラム フロー</p></td>
<td><p><a href="comment-macro-statement.md">Comment マクロ ステートメント</a></p></td>
</tr>
<tr class="even">
<td><p>プログラム フロー</p></td>
<td><p><a href="group-macro-statement.md">Group マクロ ステートメント</a></p></td>
</tr>
<tr class="odd">
<td><p>プログラム フロー</p></td>
<td><p><a href="if-then-else-macro-block.md">If...Then...Else マクロ ブロック</a></p></td>
</tr>
<tr class="even">
<td><p>データ ブロック</p></td>
<td><p><a href="lookuprecord-data-block.md">マクロ アクションの不一致</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="clearmacroerror-macro-action.md">ClearMacroError マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="onerror-macro-action.md">OnError マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="raiseerror-macro-action.md">RaiseError マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="setfield-macro-action.md">SetField マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="setlocalvar-macro-action.md">SetLocalVar マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="stopmacro-macro-action.md">StopMacro マクロ アクション</a></p></td>
</tr>
</tbody>
</table>


**変更**する前にイベントをキャプチャするデータ マクロを作成するには、次の手順を使用します。

1.  **変更**する前にイベントをキャプチャするテーブルを開きます。

2.  [ **テーブル**] タブの [ **イベント前**] で、[ **変更前**] をクリックします。

空のデータ マクロがマクロ デザイナーに表示されます。

## <a name="example"></a>例

次のコード例では、状態のフィールドを検証するために**変更**する前にイベントを使用します。 [解像度] フィールドに不適切な値が含まれている場合、エラーが発生します。

```vb 
 
/* Check to ensure that if the bug is resloved that the user has selected a resolution      */ 
If   [Status]="3 - Resolved" And IsNull([Resolution])   Then 
 
     RaiseError 
             Error Number   1 
        Error Description   You must select a resolution. 
End If 
 
/* Check to ensure that if a bug is closed that the user has selected a resolution first     */ 
If   [Status]="4 - Closed" And IsNull([Resolution])   Then 
 
      RaiseError 
             Error Number   2 
        Error Description   An issue must be resolved before it can be closed. 
End If 
 
If   [Status]<>"3 - Resolved" And [Status]<>"4 - Closed"   Then 
 
      SetField 
             Name   Resolution 
            Value   =Null 
End If 
 
```

この例をマクロ デザイナーで表示するには、次の手順に従います。

1.  **変更**する前にイベントをキャプチャするテーブルを開きます。

2.  [ **テーブル**] タブの [ **イベント前**] で、[ **変更前**] をクリックします。

3.  コード例を次のコードを選択し、クリップボードにコピーするのには**CTRL + C**キーを押します。

4.  マクロ デザイナー ウィンドウをアクティブにして、 **ctrl キーと V**キーを押します。



```xml
<DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
  <DataMacro Event="BeforeChange"> 
    <Statements> 
      <Comment>Check to ensure that if the bug is resloved that the user has selected a resolution </Comment> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]="3 - Resolved" And IsNull([Resolution])</Condition> 
          <Statements> 
            <Action Name="RaiseError"> 
              <Argument Name="Number">1</Argument> 
              <Argument Name="Description">You must select a resolution.</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
      <Comment>Check to ensure that if a bug is closed that the user has selected a resolution first </Comment> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]="4 - Closed" And IsNull([Resolution])</Condition> 
          <Statements> 
            <Action Name="RaiseError"> 
              <Argument Name="Number">2</Argument> 
              <Argument Name="Description">An issue must be resolved before it can be closed.</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]&lt;&gt;"3 - Resolved" And [Status]&lt;&gt;"4 - Closed"</Condition> 
          <Statements> 
            <Action Name="SetField"> 
              <Argument Name="Field">Resolution</Argument> 
              <Argument Name="Value">Null</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
    </Statements> 
  </DataMacro> 
</DataMacros>
```

次の例は、" RaiseError" アクションを使用して Before Change データ マクロ イベントを取り消す方法を示します。 AssignedTo フィールドが更新されると、 LookupRecord データ ブロックを使用して、割り当てられた技術者が未解決サービス リクエストに現在割り当てられているかどうかが確認されます。 これが true の場合は、変更する前にイベントをキャンセルするとレコードは更新されません。

**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。

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
