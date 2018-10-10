---
title: After Insert マクロ イベント
TOCTitle: After Insert Macro Event
ms:assetid: 78013896-ee07-6979-96f7-fa0f3490419e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196099(v=office.15)
ms:contentKeyID: 48545742
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3180
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a343c9bb0ea498c3388eb5ce67c3e0692808824c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477452"
---
# <a name="after-insert-macro-event"></a>After Insert マクロ イベント


**適用されます**Access 2013 |。Office 2013

**挿入の後**のイベントは、レコードを追加した後に発生します。


> [!NOTE]
> **挿入した後**のイベントは、データ マクロでのみ使用可能。



## <a name="remarks"></a>備考

テーブルにレコードを追加するときに発生するアクションを実行するのにには、イベントの**後に、挿入**を使用します。 **後に挿入**するための一般的な使用法には、ビジネス ルール、ワークフローを強制すること、回数の集計の更新通知を送信するなどがあります。

**更新 (以下「*フィールド名*」)** 関数を使用すると、フィールドが変更されたかどうかを判断します。 コード例を次に示しますが、**場合**に使用する方法を示していますを決定するためのステートメントでは、PaidInFull フィールドが変更されたかどうかを確認します。

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

**挿入した後**のイベントで使用できるマクロのコマンドを次の表に一覧します。

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
<td><p><a href="cancelrecordchange-macro-action.md">"CancelRecordChange/レコードの変更の取り消し" マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="clearmacroerror-macro-action.md">"ClearMacroError/マクロエラーのクリア" マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="deleterecord-macro-action.md">"DeleteRecord/レコードの削除" マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="exitforeachrecord-macro-action.md">"ExitForEachRecord/レコードごとに終了" マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="logevent-macro-action.md">"LogEvent/イベントのログ記録" マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="onerror-macro-action.md">OnError マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="raiseerror-macro-action.md">"RaiseError/エラーの生成" マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="rundatamacro-macro-action.md">"RunDataMacro/データマクロの実行" マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="sendemail-macro-action.md">SendEmail マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="setfield-macro-action.md">"SetField/フィールドの設定" マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="setlocalvar-macro-action.md">"SetLocalVar/ローカル変数の設定" マクロ アクション</a></p></td>
</tr>
<tr class="odd">
<td><p>データ アクション</p></td>
<td><p><a href="stopallmacros-macro-action.md">"StopAllMacros/全マクロの中止" マクロ アクション</a></p></td>
</tr>
<tr class="even">
<td><p>データ アクション</p></td>
<td><p><a href="stopmacro-macro-action.md">StopMacro マクロ アクション</a></p></td>
</tr>
</tbody>
</table>


**挿入した後**のイベントをキャプチャするデータ マクロを作成するには、次の手順を使用します。

1.  **後挿入**イベントをキャプチャするテーブルを開きます。

2.  [ **テーブル**] タブの [ **イベント後**] で、[ **挿入後処理**] をクリックします。

空のデータ マクロがマクロ デザイナーに表示されます。

## <a name="example"></a>例

次のコード例では、寄付のテーブルにレコードを追加するときに、いくつか処理を実行するのにイベントの**後に、挿入**を使用します。 レコードが追加されると、DonationsReceived テーブル内のフィールド、キャンペーン、寄付金提供者の表に TotalDonatedField に、寄付の金額が追加されます。

**マクロ デザイナーに貼り付けることができるマクロのコピーを表示するのにはここをクリックします。**

この例をマクロ デザイナーで表示するには、次の手順に従います。

1.  **後挿入**イベントをキャプチャするテーブルを開きます。

2.  [ **テーブル**] タブの [ **イベント後**] で、[ **挿入後処理**] をクリックします。

3.  次のコード例を選択して、Ctrl キーを押しながら C キーを押して、クリップボードにコピーします。

4.  マクロ デザイナーを起動して、Ctrl キーを押しながら V キーを押します。

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
