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
ms.openlocfilehash: 943f16c5bb1f1525c8da36938fa6beb2e6f71444
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929798"
---
# <a name="after-delete-macro-event"></a><span data-ttu-id="67f2b-102">After Delete マクロ イベント</span><span class="sxs-lookup"><span data-stu-id="67f2b-102">After Delete macro event</span></span>


<span data-ttu-id="67f2b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="67f2b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67f2b-104">**後 Delete**イベントは、レコードが削除された後に発生します。</span><span class="sxs-lookup"><span data-stu-id="67f2b-104">The **After Delete** event occurs after a record is deleted.</span></span>


> [!NOTE]
> <span data-ttu-id="67f2b-105">**削除した後**のイベントは、データ マクロでのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="67f2b-105">The **After Delete** event is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="67f2b-106">備考</span><span class="sxs-lookup"><span data-stu-id="67f2b-106">Remarks</span></span>

<span data-ttu-id="67f2b-107">レコードが削除されるときに発生する操作を実行**した後は、Delete**イベントを使用します。</span><span class="sxs-lookup"><span data-stu-id="67f2b-107">Use the **After Delete** event to perform any actions that you want to occur when a record is deleted.</span></span> <span data-ttu-id="67f2b-108">**後を削除**するための一般的な使用法には、ビジネス ルール、ワークフローを強制すること、回数の集計の更新通知を送信するなどがあります。</span><span class="sxs-lookup"><span data-stu-id="67f2b-108">Common uses for the **After Delete** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="67f2b-109">**後 Delete**イベントが発生すると削除されたレコードに含まれている値を利用できます。</span><span class="sxs-lookup"><span data-stu-id="67f2b-109">When the **After Delete** event occurs, the values contained in the deleted record are still available.</span></span> <span data-ttu-id="67f2b-110">増分または減分の合計、監査証跡を作成または*WhereCondition*引数の既存の値と比較して、削除する値を使用することがあります。</span><span class="sxs-lookup"><span data-stu-id="67f2b-110">You may want to use a deleted value to increment or decrement a total, create an audit trail, or compare to an existing value in a *WhereCondition* argument.</span></span>

<span data-ttu-id="67f2b-111">**更新 (以下「*フィールド名*」)** 関数を使用すると、フィールドが変更されたかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="67f2b-111">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="67f2b-112">コード例を次に示します If を使用する方法を決定する staement では、PaidInFull フィールドが変更されたかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="67f2b-112">The following code example shows how to use an If staement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="67f2b-113">削除したレコード内の値にアクセスするには、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="67f2b-113">You can use access a value in the deleted record by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="67f2b-114">たとえば、削除したレコード内の QuantityInStock フィールド値にアクセスするには、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="67f2b-114">For example, to access the value of the QuantityInStock field in the deleted record, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="67f2b-115">**削除した後**のイベントが終了したとき、削除されたレコードに含まれている値が完全に削除します。</span><span class="sxs-lookup"><span data-stu-id="67f2b-115">The values contained in the deleted record are deleted permanently when the **After Delete** event ends.</span></span>

<span data-ttu-id="67f2b-116">**削除した後**のイベントでは、次のマクロ コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="67f2b-116">The following macro commands can be used in the **After Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67f2b-117">コマンドの種類</span><span class="sxs-lookup"><span data-stu-id="67f2b-117">Command Type</span></span></p></th>
<th><p><span data-ttu-id="67f2b-118">コマンド</span><span class="sxs-lookup"><span data-stu-id="67f2b-118">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67f2b-119">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="67f2b-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="67f2b-120"><a href="comment-macro-statement.md">Comment マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-120"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f2b-121">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="67f2b-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="67f2b-122"><a href="group-macro-statement.md">Group マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-122"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f2b-123">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="67f2b-123">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="67f2b-124"><a href="if-then-else-macro-block.md">If...Then...Else マクロ ブロック</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-124"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f2b-125">データ ブロック</span><span class="sxs-lookup"><span data-stu-id="67f2b-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="67f2b-126"><a href="createrecord-data-block.md">CreateRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-126"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f2b-127">データ ブロック</span><span class="sxs-lookup"><span data-stu-id="67f2b-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="67f2b-128"><a href="editrecord-data-block.md">EditRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-128"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f2b-129">データ ブロック</span><span class="sxs-lookup"><span data-stu-id="67f2b-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="67f2b-130"><a href="foreachrecord-data-block.md">ForEachRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-130"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f2b-131">データ ブロック</span><span class="sxs-lookup"><span data-stu-id="67f2b-131">Data Block</span></span></p></td>
<td><p><span data-ttu-id="67f2b-132"><a href="lookuprecord-data-block.md">不一致データのブロック</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-132"><a href="lookuprecord-data-block.md">LookupRecord data block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f2b-133">データ アクション</span><span class="sxs-lookup"><span data-stu-id="67f2b-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="67f2b-134"><a href="cancelrecordchange-macro-action.md">CancelRecordChange マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-134"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f2b-135">データ アクション</span><span class="sxs-lookup"><span data-stu-id="67f2b-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="67f2b-136"><a href="clearmacroerror-macro-action.md">ClearMacroError マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-136"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f2b-137">データ アクション</span><span class="sxs-lookup"><span data-stu-id="67f2b-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="67f2b-138"><a href="deleterecord-macro-action.md">DeleteRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-138"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f2b-139">データ アクション</span><span class="sxs-lookup"><span data-stu-id="67f2b-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="67f2b-140"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-140"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f2b-141">データ アクション</span><span class="sxs-lookup"><span data-stu-id="67f2b-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="67f2b-142"><a href="logevent-macro-action.md">LogEvent マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-142"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f2b-143">データ アクション</span><span class="sxs-lookup"><span data-stu-id="67f2b-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="67f2b-144"><a href="onerror-macro-action.md">OnError マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-144"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f2b-145">データ アクション</span><span class="sxs-lookup"><span data-stu-id="67f2b-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="67f2b-146"><a href="raiseerror-macro-action.md">RaiseError マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-146"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f2b-147">データ アクション</span><span class="sxs-lookup"><span data-stu-id="67f2b-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="67f2b-148"><a href="rundatamacro-macro-action.md">RunDataMacro マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-148"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f2b-149">データ アクション</span><span class="sxs-lookup"><span data-stu-id="67f2b-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="67f2b-150"><a href="sendemail-macro-action.md">SendEmail マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-150"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f2b-151">データ アクション</span><span class="sxs-lookup"><span data-stu-id="67f2b-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="67f2b-152"><a href="setfield-macro-action.md">SetField マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-152"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f2b-153">データ アクション</span><span class="sxs-lookup"><span data-stu-id="67f2b-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="67f2b-154"><a href="setlocalvar-macro-action.md">SetLocalVar マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-154"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67f2b-155">データ アクション</span><span class="sxs-lookup"><span data-stu-id="67f2b-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="67f2b-156"><a href="stopallmacros-macro-action.md">StopAllMacros マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-156"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67f2b-157">データ アクション</span><span class="sxs-lookup"><span data-stu-id="67f2b-157">Data Action</span></span></p></td>
<td><p><span data-ttu-id="67f2b-158"><a href="stopmacro-macro-action.md">StopMacro マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="67f2b-158"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="67f2b-159">**削除した後**のイベントをキャプチャするデータ マクロを作成するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="67f2b-159">To create a Data Macro that captures the **After Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="67f2b-160">**削除**イベントをキャプチャするテーブルを開きます。</span><span class="sxs-lookup"><span data-stu-id="67f2b-160">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="67f2b-161">[ **テーブル**] タブの [ **イベント後**] で、[ **削除後処理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="67f2b-161">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

<span data-ttu-id="67f2b-162">空のデータ マクロがマクロ デザイナーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="67f2b-162">An empty Data Macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="67f2b-163">例</span><span class="sxs-lookup"><span data-stu-id="67f2b-163">Example</span></span>

<span data-ttu-id="67f2b-164">次のコード例では、寄付のテーブルからレコードが削除されたときに、いくつか処理を実行するのに**後削除**イベントを使用します。</span><span class="sxs-lookup"><span data-stu-id="67f2b-164">The following code example uses the **After Delete** event to perform some processing when a record is deleted from the Donations table.</span></span> <span data-ttu-id="67f2b-165">レコードを削除すると、寄付の金額は、DonationsReceived テーブル内のフィールド、DonationsReceived、寄付金提供者の表に TotalDonatedField の subracted フォームです。</span><span class="sxs-lookup"><span data-stu-id="67f2b-165">When a record is deleted, the amount of the donation is subracted form the DonationsReceived field in the DonationsReceived table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="67f2b-166">**マクロ デザイナーに貼り付けることができるマクロのコピーを表示するのにはここをクリックします。**</span><span class="sxs-lookup"><span data-stu-id="67f2b-166">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="67f2b-167">この例をマクロ デザイナーで表示するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="67f2b-167">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="67f2b-168">**削除**イベントをキャプチャするテーブルを開きます。</span><span class="sxs-lookup"><span data-stu-id="67f2b-168">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="67f2b-169">[ **テーブル**] タブの [ **イベント後**] で、[ **削除後処理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="67f2b-169">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

3.  <span data-ttu-id="67f2b-170">以下のコードを選択して、Ctrl キーを押しながら C キーを押して、クリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="67f2b-170">Select the code listed below and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="67f2b-171">マクロ デザイナーを起動して、Ctrl キーを押しながら V キーを押します。</span><span class="sxs-lookup"><span data-stu-id="67f2b-171">Activate the macro designer window and then press CTRL+V.</span></span>

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
