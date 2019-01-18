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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716139"
---
# <a name="after-insert-macro-event"></a><span data-ttu-id="1ec35-102">After Insert マクロ イベント</span><span class="sxs-lookup"><span data-stu-id="1ec35-102">After Insert macro event</span></span>

<span data-ttu-id="1ec35-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1ec35-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ec35-104">**挿入の後**のイベントは、レコードを追加した後に発生します。</span><span class="sxs-lookup"><span data-stu-id="1ec35-104">The **After Insert** event occurs after a record is added.</span></span>

> [!NOTE]
> <span data-ttu-id="1ec35-105">**挿入した後**のイベントは、データ マクロでのみ使用可能。</span><span class="sxs-lookup"><span data-stu-id="1ec35-105">The **After Insert** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec35-106">備考</span><span class="sxs-lookup"><span data-stu-id="1ec35-106">Remarks</span></span>

<span data-ttu-id="1ec35-107">テーブルにレコードを追加するときに発生するアクションを実行するのにには、イベントの**後に、挿入**を使用します。</span><span class="sxs-lookup"><span data-stu-id="1ec35-107">Use the **After Insert** event to perform any actions that you want to occur when a record is added to a table.</span></span> <span data-ttu-id="1ec35-108">**後に挿入**するための一般的な使用法には、ビジネス ルール、ワークフローを強制すること、回数の集計の更新通知を送信するなどがあります。</span><span class="sxs-lookup"><span data-stu-id="1ec35-108">Common uses for the **After Insert** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="1ec35-109">**更新 (以下「*フィールド名*」)** 関数を使用すると、フィールドが変更されたかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="1ec35-109">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="1ec35-110">コード例を次に示しますが、**場合**に使用する方法を示していますを決定するためのステートメントでは、PaidInFull フィールドが変更されたかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="1ec35-110">The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="1ec35-111">**挿入した後**のイベントで使用できるマクロのコマンドを次の表に一覧します。</span><span class="sxs-lookup"><span data-stu-id="1ec35-111">The following table lists macro commands that can be used in the**After Insert** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ec35-112">コマンドの種類</span><span class="sxs-lookup"><span data-stu-id="1ec35-112">Command Type</span></span></p></th>
<th><p><span data-ttu-id="1ec35-113">コマンド</span><span class="sxs-lookup"><span data-stu-id="1ec35-113">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ec35-114">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="1ec35-114">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="1ec35-115"><a href="comment-macro-statement.md">Comment マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-115"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ec35-116">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="1ec35-116">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="1ec35-117"><a href="group-macro-statement.md">Group マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-117"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ec35-118">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="1ec35-118">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="1ec35-119"><a href="if-then-else-macro-block.md">If...Then...Else マクロ ブロック</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-119"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ec35-120">データ ブロック</span><span class="sxs-lookup"><span data-stu-id="1ec35-120">Data Block</span></span></p></td>
<td><p><span data-ttu-id="1ec35-121"><a href="createrecord-data-block.md">CreateRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-121"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ec35-122">データ ブロック</span><span class="sxs-lookup"><span data-stu-id="1ec35-122">Data Block</span></span></p></td>
<td><p><span data-ttu-id="1ec35-123"><a href="editrecord-data-block.md">EditRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-123"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ec35-124">データ ブロック</span><span class="sxs-lookup"><span data-stu-id="1ec35-124">Data Block</span></span></p></td>
<td><p><span data-ttu-id="1ec35-125"><a href="foreachrecord-data-block.md">ForEachRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-125"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ec35-126">データ ブロック</span><span class="sxs-lookup"><span data-stu-id="1ec35-126">Data Block</span></span></p></td>
<td><p><span data-ttu-id="1ec35-127"><a href="lookuprecord-data-block.md">不一致データのブロック</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-127"><a href="lookuprecord-data-block.md">LookupRecord data block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ec35-128">データ アクション</span><span class="sxs-lookup"><span data-stu-id="1ec35-128">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1ec35-129"><a href="cancelrecordchange-macro-action.md">CancelRecordChange マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-129"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ec35-130">データ アクション</span><span class="sxs-lookup"><span data-stu-id="1ec35-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1ec35-131"><a href="clearmacroerror-macro-action.md">ClearMacroError マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-131"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ec35-132">データ アクション</span><span class="sxs-lookup"><span data-stu-id="1ec35-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1ec35-133"><a href="deleterecord-macro-action.md">DeleteRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-133"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ec35-134">データ アクション</span><span class="sxs-lookup"><span data-stu-id="1ec35-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1ec35-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ec35-136">データ アクション</span><span class="sxs-lookup"><span data-stu-id="1ec35-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1ec35-137"><a href="logevent-macro-action.md">LogEvent マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-137"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ec35-138">データ アクション</span><span class="sxs-lookup"><span data-stu-id="1ec35-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1ec35-139"><a href="onerror-macro-action.md">OnError マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-139"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ec35-140">データ アクション</span><span class="sxs-lookup"><span data-stu-id="1ec35-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1ec35-141"><a href="raiseerror-macro-action.md">RaiseError マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-141"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ec35-142">データ アクション</span><span class="sxs-lookup"><span data-stu-id="1ec35-142">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1ec35-143"><a href="rundatamacro-macro-action.md">RunDataMacro マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-143"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ec35-144">データ アクション</span><span class="sxs-lookup"><span data-stu-id="1ec35-144">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1ec35-145"><a href="sendemail-macro-action.md">SendEmail マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-145"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ec35-146">データ アクション</span><span class="sxs-lookup"><span data-stu-id="1ec35-146">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1ec35-147"><a href="setfield-macro-action.md">SetField マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-147"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ec35-148">データ アクション</span><span class="sxs-lookup"><span data-stu-id="1ec35-148">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1ec35-149"><a href="setlocalvar-macro-action.md">SetLocalVar マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-149"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ec35-150">データ アクション</span><span class="sxs-lookup"><span data-stu-id="1ec35-150">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1ec35-151"><a href="stopallmacros-macro-action.md">StopAllMacros マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-151"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ec35-152">データ アクション</span><span class="sxs-lookup"><span data-stu-id="1ec35-152">Data Action</span></span></p></td>
<td><p><span data-ttu-id="1ec35-153"><a href="stopmacro-macro-action.md">StopMacro マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="1ec35-153"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ec35-154">**挿入した後**のイベントをキャプチャするデータ マクロを作成するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="1ec35-154">To create a Data macro that captures the **After Insert** event, use the following steps.</span></span>

1.  <span data-ttu-id="1ec35-155">**後挿入**イベントをキャプチャするテーブルを開きます。</span><span class="sxs-lookup"><span data-stu-id="1ec35-155">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="1ec35-156">[ **テーブル**] タブの [ **イベント後**] で、[ **挿入後処理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1ec35-156">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

<span data-ttu-id="1ec35-157">空のデータ マクロがマクロ デザイナーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1ec35-157">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="1ec35-158">例</span><span class="sxs-lookup"><span data-stu-id="1ec35-158">Example</span></span>

<span data-ttu-id="1ec35-159">次のコード例では、寄付のテーブルにレコードを追加するときに、いくつか処理を実行するのにイベントの**後に、挿入**を使用します。</span><span class="sxs-lookup"><span data-stu-id="1ec35-159">The following code example uses the **After Insert** event to perform some processing when a record is added to the Donations table.</span></span> <span data-ttu-id="1ec35-160">レコードが追加されると、DonationsReceived テーブル内のフィールド、キャンペーン、寄付金提供者の表に TotalDonatedField に、寄付の金額が追加されます。</span><span class="sxs-lookup"><span data-stu-id="1ec35-160">When a record is added, the amount of the donation is added to the DonationsReceived field in the Campaigns table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="1ec35-161">**マクロ デザイナーに貼り付けることができるマクロのコピーを表示するのにはここをクリックします。**</span><span class="sxs-lookup"><span data-stu-id="1ec35-161">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="1ec35-162">この例をマクロ デザイナーで表示するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1ec35-162">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="1ec35-163">**後挿入**イベントをキャプチャするテーブルを開きます。</span><span class="sxs-lookup"><span data-stu-id="1ec35-163">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="1ec35-164">[ **テーブル**] タブの [ **イベント後**] で、[ **挿入後処理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1ec35-164">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

3.  <span data-ttu-id="1ec35-165">次のコード例を選択して、Ctrl キーを押しながら C キーを押して、クリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1ec35-165">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="1ec35-166">マクロ デザイナーを起動して、Ctrl キーを押しながら V キーを押します。</span><span class="sxs-lookup"><span data-stu-id="1ec35-166">Activate the macro designer window and then press CTRL+V.</span></span>

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
