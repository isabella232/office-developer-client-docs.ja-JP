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
localization_priority: Priority
ms.openlocfilehash: a96b46fcc78c4f93887e487f52091a77da6c0d2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297187"
---
# <a name="after-update-macro-event"></a><span data-ttu-id="5e670-102">After Update マクロ イベント</span><span class="sxs-lookup"><span data-stu-id="5e670-102">After Update macro event</span></span>

<span data-ttu-id="5e670-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="5e670-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5e670-104">The **After Update** event occurs after a record is changed.</span><span class="sxs-lookup"><span data-stu-id="5e670-104">The **After Update** event occurs after a record is changed.</span></span>

> [!NOTE]
> <span data-ttu-id="5e670-105">After Update イベントは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="5e670-105">The **After Update** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e670-106">注釈</span><span class="sxs-lookup"><span data-stu-id="5e670-106">Remarks</span></span>

<span data-ttu-id="5e670-p101">After Update イベントでは、レコードを変更したときに特定のアクションを実行します。通常は、ビジネス ルールの実行、総計の更新、通知の送信などを行います。</span><span class="sxs-lookup"><span data-stu-id="5e670-p101">Use the **After Update** event to perform any actions that you want to occur when a record is changed. Common uses for the **After Insert** include enforcing business rules, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="5e670-109">**Updated("*フィールド名*")** 関数を使用すると、フィールドが変更されているかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="5e670-109">You can use the *Updated("**Field Name**")* function to determine whether a field has changed.</span></span> <span data-ttu-id="5e670-110">次のコード例では、PaidInFull フィールドが変更されているかどうかを If ステートメントで判断する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5e670-110">The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="5e670-111">次の構文を使用して、フィールド内の以前の値にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="5e670-111">You can use access a the previous value in a field by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="5e670-112">たとえば、QuantityInStock フィールド内の以前の値にアクセスするには、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="5e670-112">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="5e670-113">**After Update** イベントが終了すると、以前の値は完全に削除されます。</span><span class="sxs-lookup"><span data-stu-id="5e670-113">The previous values are deleted permanently when the **After Update** event ends.</span></span>

<span data-ttu-id="5e670-114">After Update イベントで使用できるマクロ コマンドは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5e670-114">The following table lists macro commands can be used in the**After Update** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5e670-115">コマンドの種類</span><span class="sxs-lookup"><span data-stu-id="5e670-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="5e670-116">コマンド</span><span class="sxs-lookup"><span data-stu-id="5e670-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e670-117">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="5e670-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="5e670-118"><a href="comment-macro-statement.md">Comment マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="5e670-118"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e670-119">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="5e670-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="5e670-120"><a href="group-macro-statement.md">Group マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="5e670-120"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e670-121">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="5e670-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="5e670-122"><a href="if-then-else-macro-block.md">If...Then...Else マクロ ブロック</a></span><span class="sxs-lookup"><span data-stu-id="5e670-122"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e670-123">データ ブロック</span><span class="sxs-lookup"><span data-stu-id="5e670-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="5e670-124"><a href="createrecord-data-block.md">CreateRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-124"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e670-125">データ ブロック</span><span class="sxs-lookup"><span data-stu-id="5e670-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="5e670-126"><a href="editrecord-data-block.md">EditRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-126"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e670-127">データ ブロック</span><span class="sxs-lookup"><span data-stu-id="5e670-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="5e670-128"><a href="foreachrecord-data-block.md">ForEachRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-128"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e670-129">データ ブロック</span><span class="sxs-lookup"><span data-stu-id="5e670-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="5e670-130"><a href="lookuprecord-data-block.md">LookupRecord データ ブロック</a></span><span class="sxs-lookup"><span data-stu-id="5e670-130"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e670-131">データ アクション</span><span class="sxs-lookup"><span data-stu-id="5e670-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5e670-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e670-133">データ アクション</span><span class="sxs-lookup"><span data-stu-id="5e670-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5e670-134"><a href="clearmacroerror-macro-action.md">ClearMacroError マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-134"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e670-135">データ アクション</span><span class="sxs-lookup"><span data-stu-id="5e670-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5e670-136"><a href="deleterecord-macro-action.md">DeleteRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-136"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e670-137">データ アクション</span><span class="sxs-lookup"><span data-stu-id="5e670-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5e670-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e670-139">データ アクション</span><span class="sxs-lookup"><span data-stu-id="5e670-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5e670-140"><a href="logevent-macro-action.md">LogEvent マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-140"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e670-141">データ アクション</span><span class="sxs-lookup"><span data-stu-id="5e670-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5e670-142"><a href="onerror-macro-action.md">OnError マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-142"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e670-143">データ アクション</span><span class="sxs-lookup"><span data-stu-id="5e670-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5e670-144"><a href="raiseerror-macro-action.md">RaiseError マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-144"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e670-145">データ アクション</span><span class="sxs-lookup"><span data-stu-id="5e670-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5e670-146"><a href="rundatamacro-macro-action.md">RunDataMacro マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-146"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e670-147">データ アクション</span><span class="sxs-lookup"><span data-stu-id="5e670-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5e670-148"><a href="sendemail-macro-action.md">SendEmail マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-148"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e670-149">データ アクション</span><span class="sxs-lookup"><span data-stu-id="5e670-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5e670-150"><a href="setfield-macro-action.md">SetField マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-150"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e670-151">データ アクション</span><span class="sxs-lookup"><span data-stu-id="5e670-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5e670-152"><a href="setlocalvar-macro-action.md">SetLocalVar マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-152"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e670-153">データ アクション</span><span class="sxs-lookup"><span data-stu-id="5e670-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5e670-154"><a href="stopallmacros-macro-action.md">StopAllMacros マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-154"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e670-155">データ アクション</span><span class="sxs-lookup"><span data-stu-id="5e670-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5e670-156"><a href="stopmacro-macro-action.md">StopMacro マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="5e670-156"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5e670-157">To create a Data macro that captures the **After Update** event, use the folloiwng steps:</span><span class="sxs-lookup"><span data-stu-id="5e670-157">To create a Data macro that captures the **After Update** event, use the folloiwng steps:</span></span>

1.  <span data-ttu-id="5e670-158">Open the table for which you want to capture the **After Update** event.</span><span class="sxs-lookup"><span data-stu-id="5e670-158">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="5e670-159">[ **テーブル**] タブの [ **イベント後**] で、[ **更新後処理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e670-159">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

<span data-ttu-id="5e670-160">空のデータ マクロがマクロ デザイナーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5e670-160">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="5e670-161">例</span><span class="sxs-lookup"><span data-stu-id="5e670-161">Example</span></span>

<span data-ttu-id="5e670-162">次のコード例では、After Update イベントを使用して、問題のステータスを更新するたびに Comment テーブルにレコードを追加する名前付きデータ マクロを実行します。</span><span class="sxs-lookup"><span data-stu-id="5e670-162">The following code example uses the **After Update** event to run a named data macro that adds a record to the Comment table each time the status of an issue is updated.</span></span>

<span data-ttu-id="5e670-163">**マクロ デザイナーに貼り付けることができるマクロのコピーを表示するには、ここをクリックします。**</span><span class="sxs-lookup"><span data-stu-id="5e670-163">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="5e670-164">この例をマクロ デザイナーで表示するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5e670-164">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="5e670-165">Open the table for which you want to capture the **After Update** event.</span><span class="sxs-lookup"><span data-stu-id="5e670-165">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="5e670-166">[ **テーブル**] タブの [ **イベント後**] で、[ **更新後処理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e670-166">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

3.  <span data-ttu-id="5e670-167">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span><span class="sxs-lookup"><span data-stu-id="5e670-167">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="5e670-168">Activate the macro designer window and then press CTRL+V.</span><span class="sxs-lookup"><span data-stu-id="5e670-168">Activate the macro designer window and then press CTRL+V.</span></span>

<!-- end list -->

```xml
    <DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
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

