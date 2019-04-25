---
title: After Insert マクロ イベント
TOCTitle: After Insert macro event
ms:assetid: 78013896-ee07-6979-96f7-fa0f3490419e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196099(v=office.15)
ms:contentKeyID: 48545742
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3180
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c84a737d08b791bfe560bfe6af6bcc59a14d2678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297222"
---
# <a name="after-insert-macro-event"></a>After Insert マクロ イベント

**適用先**: Access 2013、Office 2013

The **After Insert** event occurs after a record is added.

> [!NOTE]
> After Insert イベントは、データ マクロでのみ使用できます。

## <a name="remarks"></a>注釈

After Insert イベントでは、テーブルにレコードを追加したときに特定のアクションを実行します。通常は、ビジネス ルールやワークフローの実行、総計の更新、通知の送信などを行います。

**Updated("*フィールド名*")** 関数を使用すると、フィールドが変更されているかどうかを判断できます。 次のコード例では、PaidInFull フィールドが変更されているかどうかを If ステートメントで判断する方法を示します。

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

After Insert イベントで使用できるマクロ コマンドは次のとおりです。

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


To create a Data macro that captures the **After Insert** event, use the following steps.

1.  Open the table for which you want to capture the **After Insert** event.

2.  [ **テーブル**] タブの [ **イベント後**] で、[ **挿入後処理**] をクリックします。

空のデータ マクロがマクロ デザイナーに表示されます。

## <a name="example"></a>例

The following code example uses the **After Insert** event to perform some processing when a record is added to the Donations table. When a record is added, the amount of the donation is added to the DonationsReceived field in the Campaigns table and the TotalDonatedField in the Donors table.

**マクロ デザイナーに貼り付けることができるマクロのコピーを表示するには、ここをクリックします。**

この例をマクロ デザイナーで表示するには、次の手順に従います。

1.  Open the table for which you want to capture the **After Insert** event.

2.  [ **テーブル**] タブの [ **イベント後**] で、[ **挿入後処理**] をクリックします。

3.  Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.

4.  Activate the macro designer window and then press CTRL+V.

<!-- end list -->

```xml
    <DataMacros> 
      <DataMacro Event="AfterInsert"> 
        <Statements> 
          <Comment>This data macro increments the DonationsReceived field in Campaigns and theAmountCollected field in Pledges </Comment> 
          <Action Name="SetLocalVar"> 
            <Argument Name="Name">varAmount</Argument> 
            <Argument Name="Value">[Amount]</Argument> 
          </Action> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([CampaignID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Campaigns</Reference> 
                    <WhereCondition>[ID]=[Donations].[CampaignID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[DonationsReceived]</Argument> 
                          <Argument Name="Value">[DonationsReceived]+[varAmount]</Argument> 
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
              <Condition>Not (IsNull([DonorID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Donors</Reference> 
                    <WhereCondition>[ID]=[Donations].[DonorID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[TotalDonated]</Argument> 
                          <Argument Name="Value">[TotalDonated]+[varAmount]</Argument> 
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
                  Name   varAmount 
            Expression   =[Amount] 
     
    If   Not (IsNull([CampaignID]))   Then 
     
         For Each Record In   Campaigns 
            Where Condition   =[ID]=[Donations].[CampaignID] 
                      Alias 
     
                 EditRecord 
                              Alias 
                     SetField 
                                 Name   [DonationsReceived] 
                                Value   =[DonationsReceived]+[varAmount] 
                End EditRecord 
    End If 
     
    If   Not (IsNull([DonorID]))   Then 
     
         For Each Record In  Donors 
            WhereCondition   =[ID]=[Donations].[DonorID] 
                     Alias 
     
                 EditRecord 
                              Alias 
                     SetField 
                                 Name   [TotalDonated] 
                                Value   =[TotalDonated]+[varAmount] 
                 End EditRecord 
    End If
```
