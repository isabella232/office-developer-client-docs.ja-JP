---
title: After Delete マクロ イベント
TOCTitle: After Delete macro event
ms:assetid: ecf9e6d4-345f-9b78-eb36-bd526e5df09b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836323(v=office.15)
ms:contentKeyID: 48548527
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm15155
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f524a544736f68bcfa6bd15e3bcc720ffa2bc4d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297215"
---
# <a name="after-delete-macro-event"></a>After Delete マクロ イベント

**適用先:** Access 2013、Office 2013

The **After Delete** event occurs after a record is deleted.

> [!NOTE]
> After Delete イベントは、データ マクロでのみ使用できます。

## <a name="remarks"></a>注釈

After Delete イベントでは、レコードを削除したときに特定のアクションを実行します。通常は、ビジネス ルールやワークフローの実行、総計の更新、通知の送信などを行います。

When the **After Delete** event occurs, the values contained in the deleted record are still available. 削除された値を使用して合計を増減したり、監査トレールを作成したり、 *WhereCondition*引数の既存の値と比較したりすることができます。

**Updated ("*Field Name*")** 関数を使用して、フィールドが変更されたかどうかを調べることができます。 The following code example shows how to use an If staement to determine determine whether the PaidInFull field has been changed.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

削除したレコード内の値にアクセスするには、次の構文を使用します。

`[Old].[Field Name]`

たとえば、削除したレコード内の QuantityInStock フィールド値にアクセスするには、次の構文を使用します。

`[Old].[QuantityInStock]`

The values contained in the deleted record are deleted permanently when the **After Delete** event ends.

次のマクロコマンドは、 **After Delete**イベントで使用できます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>コマンドの種類</p></th>
<th><p>Command</p></th>
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
<td><p><a href="createrecord-data-block.md">CreateRecord マクロアクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ ブロック</p></td>
<td><p><a href="editrecord-data-block.md">"レコードの操作" マクロアクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ ブロック</p></td>
<td><p><a href="foreachrecord-data-block.md">ForEachRecord マクロアクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ ブロック</p></td>
<td><p><a href="lookuprecord-data-block.md">LookupRecord データブロック</a></p></td>
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


After Delete イベントをキャプチャするデータ マクロを作成するには、次の手順に従います。

1.  After Delete イベントをキャプチャするテーブルを開きます。

2.  [**テーブル**] タブの [**イベント後**] で、[**削除後処理**] をクリックします。

空のデータ マクロがマクロ デザイナーに表示されます。

## <a name="example"></a>例

次のコード例では、After Delete イベントを使用して、Donations テーブルからレコードを削除したときに特定の処理を実行します。 レコードが削除されると、寄付の金額は、DonationsReceived テーブルの DonationsReceived フィールドと、[寄付] テーブル内の TotalDonatedField の値になります。

**Click here to view a copy of the macro that you can paste into Macro Designer.**

この例をマクロ デザイナーで表示するには、次の手順に従います。

1.  After Delete イベントをキャプチャするテーブルを開きます。

2.  [**テーブル**] タブの [**イベント後**] で、[**削除後処理**] をクリックします。

3.  以下のコードを選択して、Ctrl キーを押しながら C キーを押して、クリップボードにコピーします。

4.  マクロ デザイナーを起動して、Ctrl キーを押しながら V キーを押します。

<!-- end list -->

```xml
    <?xml version="1.0" encoding="UTF-16" standalone="no"?> 
    <DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
      <DataMacro Event="AfterDelete"> 
        <Statements> 
          <Comment>Initialize a variable and assign the old</Comment> 
          <Action Name="SetLocalVar"> 
            <Argument Name="Name">varAmount</Argument> 
            <Argument Name="Value">[Old].[Amount]</Argument> 
          </Action> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([Old].[CampaignID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Campaigns</Reference> 
                    <WhereCondition>[ID]=[Old].[CampaignID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Collapsed="true" Name="SetField"> 
                          <Argument Name="Field">[DonationsReceived]</Argument> 
                          <Argument Name="Value">[DonationsReceived]-[varAmount]</Argument> 
                        </Action> 
                      </Statements> 
                    </EditRecord> 
                  </Statements> 
                </ForEachRecord> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([Old].[DonorID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Donors</Reference> 
                    <WhereCondition>[ID]=[Old].[DonorID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[TotalDonated]</Argument> 
                          <Argument Name="Value">[TotalDonated]-[varAmount]</Argument> 
                        </Action> 
                      </Statements> 
                    </EditRecord> 
                  </Statements> 
                </ForEachRecord> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
        </Statements> 
      </DataMacro> 
    </DataMacros>
```

<br/>

```vb
    SetLocalVar 
                    Name    varAmount 
              Expression   =[Old].[Amount] 
     
    If   Not(IsNull([Old].[CampaignID]]))   Then 
     
         For Each Record In     Campaigns 
            Where Condition     =[ID]=[Old].[CampaignID] 
                      Alias 
            EditRecord 
                      Alias 
                  SetField   ([DonationsReceived], [DonationsReceived] - [varAmount]) 
            End EditRecord 
     
    End If 
     
    If   Not(IsNull([Old].[DonorID]]))   Then 
     
         For Each Record In    Donors 
            Where Condition     =[ID]=[Old].[DonorID] 
                      Alias 
            EditRecord 
                      Alias 
     
              SetField 
                             Name   [TotalDonated] 
                            Value   =[TotalDonated]-[varAmount] 
            End EditRecord 
    End If
```
