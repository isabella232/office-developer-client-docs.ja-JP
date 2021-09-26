---
title: After Update マクロ イベント
TOCTitle: After Update macro event
ms:assetid: 5213793b-8301-0f18-3a12-4e3764c879ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193905(v=office.15)
ms:contentKeyID: 48544838
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm85126
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 60726e4c514f9fc8e6a432bac171d6bc35c4c05e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559123"
---
# <a name="after-update-macro-event"></a>After Update マクロ イベント

**適用先**: Access 2013、Office 2013

The **After Update** event occurs after a record is changed.

> [!NOTE]
> After Update イベントは、データ マクロでのみ使用できます。

## <a name="remarks"></a>注釈

After Update イベントでは、レコードを変更したときに特定のアクションを実行します。通常は、ビジネス ルールの実行、総計の更新、通知の送信などを行います。

**Updated("*フィールド名*")** 関数を使用すると、フィールドが変更されているかどうかを判断できます。次のコード例では、PaidInFull フィールドが変更されているかどうかを **If** ステートメントで判断する方法を示します。

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

次の構文を使用して、フィールド内の以前の値にアクセスできます。

`[Old].[Field Name]`

たとえば、QuantityInStock フィールド内の以前の値にアクセスするには、次の構文を使用します。

`[Old].[QuantityInStock]`

**After Update** イベントが終了すると、以前の値は完全に削除されます。

After Update イベントで使用できるマクロ コマンドは次のとおりです。

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
<td><p><a href="createrecord-data-block.md">CreateRecord マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ ブロック</p></td>
<td><p><a href="editrecord-data-block.md">EditRecord マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ ブロック</p></td>
<td><p><a href="foreachrecord-data-block.md">ForEachRecord マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ ブロック</p></td>
<td><p><a href="lookuprecord-data-block.md">LookupRecord データ ブロック</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="cancelrecordchange-macro-action.md">CancelRecordChange マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="clearmacroerror-macro-action.md">ClearMacroError マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="deleterecord-macro-action.md">DeleteRecord マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="exitforeachrecord-macro-action.md">ExitForEachRecord マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="logevent-macro-action.md">LogEvent マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="onerror-macro-action.md">OnError マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="raiseerror-macro-action.md">RaiseError マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="rundatamacro-macro-action.md">RunDataMacro マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="sendemail-macro-action.md">SendEmail マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="setfield-macro-action.md">SetField マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="setlocalvar-macro-action.md">SetLocalVar マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="stopallmacros-macro-action.md">StopAllMacros マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="stopmacro-macro-action.md">StopMacro マクロ アクション</a></p></td>
</tr>
</tbody>
</table>


To create a Data macro that captures the **After Update** event, use the folloiwng steps:

1.  Open the table for which you want to capture the **After Update** event.

2.  [ **テーブル**] タブの [ **イベント後**] で、[ **更新後処理**] をクリックします。

空のデータ マクロがマクロ デザイナーに表示されます。

## <a name="example"></a>例

次のコード例では、After Update イベントを使用して、問題のステータスを更新するたびに Comment テーブルにレコードを追加する名前付きデータ マクロを実行します。

**マクロ デザイナーに貼り付けることができるマクロのコピーを表示するには、ここをクリックします。**

この例をマクロ デザイナーで表示するには、次の手順に従います。

1.  Open the table for which you want to capture the **After Update** event.

2.  [ **テーブル**] タブの [ **イベント後**] で、[ **更新後処理**] をクリックします。

3.  Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.

4.  Activate the macro designer window and then press CTRL+V.

<!-- end list -->

```xml
    <DataMacros xmlns="http://schemas.microsoft.com/office/accessservices/2009/04/application"> 
      <DataMacro Event="AfterUpdate"> 
        <Statements> 
          <ConditionalBlock> 
            <If> 
              <Condition>Updated("Status")</Condition> 
              <Statements> 
                <Action Name="RunDataMacro"> 
                  <Argument Name="MacroName">Comments.AddComment</Argument> 
                  <Parameters> 
                    <Parameter Name="prmRelatedID" Value="[ID]" /> 
                    <Parameter Name="prmComment" Value="&quot;-- Status changed to &quot; &amp; [Status]" /> 
                    <Parameter Name="prmUserID" Value="[UserID]" /> 
                  </Parameters> 
                </Action> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
          <ConditionalBlock> 
            <If> 
              <Condition>Updated("Resolution")</Condition> 
              <Statements> 
                <Action Name="RunDataMacro"> 
                  <Argument Name="MacroName">Comments.AddComment</Argument> 
                  <Parameters> 
                    <Parameter Name="prmRelatedID" Value="[ID]" /> 
                    <Parameter Name="prmUserID" Value="[UserID]" /> 
                    <Parameter Name="prmComment" Value="&quot;-- Issue resolved as &quot; &amp; [Resolution]" /> 
                  </Parameters> 
                </Action> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
        </Statements> 
      </DataMacro> 
    </DataMacros>
``` 

<br/>

```vb
If  Updated("Status")   Then 
     RunDataMacro 
        Macro Name   Comments.AddComment 
     Parameters 
       prmRelatedID   = [ID] 
         prmComment   ="--Status Changes to "&[Status] 
          prmUserID   =[ChangedByUserID] 
End If 
 
If   Updated("Resolution")   Then 
     RunDataMacro 
        Macro Name   Comments.AddComment 
     Parameters 
       prmRelatedID   = [ID] 
          prmUserID   =[ChangedByUserID] 
         prmComment   ="--Issue Resolved as "&[Status] 
End If 
```

