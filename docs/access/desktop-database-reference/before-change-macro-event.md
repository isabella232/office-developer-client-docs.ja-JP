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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296858"
---
# <a name="before-change-macro-event"></a><span data-ttu-id="75e17-102">Before Change マクロ イベント</span><span class="sxs-lookup"><span data-stu-id="75e17-102">Before Change macro event</span></span>

<span data-ttu-id="75e17-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="75e17-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75e17-104">The **Before Change** event occurs when a record changes, but before the change is committed.</span><span class="sxs-lookup"><span data-stu-id="75e17-104">The **Before Change** event occurs when a record changes, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="75e17-105">Before Change イベントは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="75e17-105">The **Before Change** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="75e17-106">注釈</span><span class="sxs-lookup"><span data-stu-id="75e17-106">Remarks</span></span>

<span data-ttu-id="75e17-p101">Before Change イベントでは、レコードの変更を確定する前に特定のアクションを実行します。通常は、検証の実行やカスタム エラー メッセージの生成を行います。</span><span class="sxs-lookup"><span data-stu-id="75e17-p101">Use the **Before Change** event to perform any actions that you want to occur before a record is changed. The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="75e17-109">**Updated ("*Field Name*")** 関数を使用して、フィールドが変更されたかどうかを調べることができます。</span><span class="sxs-lookup"><span data-stu-id="75e17-109">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="75e17-110">次のコード例は、 **if**ステートメントを使用して、paidinfull フィールドが変更されているかどうかを判断する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="75e17-110">The following code example shows how to use an **If** statement to determine whether the PaidInFull field has been changed.</span></span>

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

<span data-ttu-id="75e17-p103">Use the **IsInsert** property to determine whether the **Before Change** event was triggered by a new record being created or a change to an existing record. They **IsInsert** property contains **True** if the event was triggered by a new record, **False** if the event was triggered by a change to en existing record.</span><span class="sxs-lookup"><span data-stu-id="75e17-p103">Use the **IsInsert** property to determine whether the **Before Change** event was triggered by a new record being created or a change to an existing record. They **IsInsert** property contains **True** if the event was triggered by a new record, **False** if the event was triggered by a change to en existing record.</span></span>

<span data-ttu-id="75e17-113">The following code example shows the syntax for using the **IsInsert** property.</span><span class="sxs-lookup"><span data-stu-id="75e17-113">The following code example shows the syntax for using the **IsInsert** property.</span></span>

```vb
    If   [IsInsert] = True   Then 
     
       /*  Actions for validating a new record go here.       */ 
     
    Else 
     
       /* Actions for processing a changed record go here.    */ 
     
    End If
```

<span data-ttu-id="75e17-114">次の構文を使用して、フィールド内の以前の値にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="75e17-114">You can use access a the previous value in a field by using the following syntax.</span></span>

```vb
    [Old].[Field Name]
```

<span data-ttu-id="75e17-115">たとえば、QuantityInStock フィールド内の以前の値にアクセスするには、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="75e17-115">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

```vb
    [Old].[QuantityInStock]
```

<span data-ttu-id="75e17-116">The previous values are deleted permanently when the **Before Change** event ends.</span><span class="sxs-lookup"><span data-stu-id="75e17-116">The previous values are deleted permanently when the **Before Change** event ends.</span></span>

<span data-ttu-id="75e17-p104">You can cancel the **Before Change** event by using the **RaiseError** action. When an error is raised the changes contained in the **Before Change** event are discarded.</span><span class="sxs-lookup"><span data-stu-id="75e17-p104">You can cancel the **Before Change** event by using the **RaiseError** action. When an error is raised the changes contained in the **Before Change** event are discarded.</span></span>

<span data-ttu-id="75e17-119">Before Change イベントで使用できるマクロ コマンドは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="75e17-119">The following table lists macro commands that can be used in the**Before Change** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75e17-120">コマンドの種類</span><span class="sxs-lookup"><span data-stu-id="75e17-120">Command Type</span></span></p></th>
<th><p><span data-ttu-id="75e17-121">Command</span><span class="sxs-lookup"><span data-stu-id="75e17-121">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75e17-122">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="75e17-122">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="75e17-123"><a href="comment-macro-statement.md">Comment マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="75e17-123"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e17-124">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="75e17-124">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="75e17-125"><a href="group-macro-statement.md">Group マクロ ステートメント</a></span><span class="sxs-lookup"><span data-stu-id="75e17-125"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e17-126">プログラム フロー</span><span class="sxs-lookup"><span data-stu-id="75e17-126">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="75e17-127"><a href="if-then-else-macro-block.md">If...Then...Else マクロ ブロック</a></span><span class="sxs-lookup"><span data-stu-id="75e17-127"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e17-128">データ ブロック</span><span class="sxs-lookup"><span data-stu-id="75e17-128">Data Block</span></span></p></td>
<td><p><span data-ttu-id="75e17-129"><a href="lookuprecord-data-block.md">LookupRecord マクロアクション</a></span><span class="sxs-lookup"><span data-stu-id="75e17-129"><a href="lookuprecord-data-block.md">LookupRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e17-130">データ アクション</span><span class="sxs-lookup"><span data-stu-id="75e17-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="75e17-131"><a href="clearmacroerror-macro-action.md">ClearMacroError マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="75e17-131"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e17-132">データ アクション</span><span class="sxs-lookup"><span data-stu-id="75e17-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="75e17-133"><a href="onerror-macro-action.md">OnError マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="75e17-133"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e17-134">データ アクション</span><span class="sxs-lookup"><span data-stu-id="75e17-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="75e17-135"><a href="raiseerror-macro-action.md">RaiseError マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="75e17-135"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e17-136">データ アクション</span><span class="sxs-lookup"><span data-stu-id="75e17-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="75e17-137"><a href="setfield-macro-action.md">SetField マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="75e17-137"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e17-138">データ アクション</span><span class="sxs-lookup"><span data-stu-id="75e17-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="75e17-139"><a href="setlocalvar-macro-action.md">SetLocalVar マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="75e17-139"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e17-140">データ アクション</span><span class="sxs-lookup"><span data-stu-id="75e17-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="75e17-141"><a href="stopmacro-macro-action.md">StopMacro マクロ アクション</a></span><span class="sxs-lookup"><span data-stu-id="75e17-141"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75e17-142">To create a Data Macro that captures the **Before Change** event, use the following steps:</span><span class="sxs-lookup"><span data-stu-id="75e17-142">To create a Data Macro that captures the **Before Change** event, use the following steps:</span></span>

1.  <span data-ttu-id="75e17-143">Open the table for which you want to capture the **Before Change** event.</span><span class="sxs-lookup"><span data-stu-id="75e17-143">Open the table for which you want to capture the **Before Change** event.</span></span>

2.  <span data-ttu-id="75e17-144">[ **テーブル**] タブの [ **イベント前**] で、[ **変更前**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75e17-144">On the **Table** tab, in the **Before Events** group, click **Before Change**.</span></span>

<span data-ttu-id="75e17-145">空のデータ マクロがマクロ デザイナーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="75e17-145">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="75e17-146">例</span><span class="sxs-lookup"><span data-stu-id="75e17-146">Example</span></span>

<span data-ttu-id="75e17-147">次のコード例では、 **Before Change**イベントを使用して、状態フィールドを検証します。</span><span class="sxs-lookup"><span data-stu-id="75e17-147">The following code example uses the **Before Change** event to validate the Status fields.</span></span> <span data-ttu-id="75e17-148">An error is raised if an inappropriate value is contained in the Resolution field.</span><span class="sxs-lookup"><span data-stu-id="75e17-148">An error is raised if an inappropriate value is contained in the Resolution field.</span></span>

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

<span data-ttu-id="75e17-149">この例をマクロ デザイナーで表示するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="75e17-149">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="75e17-150">Open the table for which you want to capture the **Before Change** event.</span><span class="sxs-lookup"><span data-stu-id="75e17-150">Open the table for which you want to capture the **Before Change** event.</span></span>

2.  <span data-ttu-id="75e17-151">[ **テーブル**] タブの [ **イベント前**] で、[ **変更前**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="75e17-151">On the **Table** tab, in the **Before Events** group, click **Before Change**.</span></span>

3.  <span data-ttu-id="75e17-152">次のコード例のコードを選択し、 **CTRL + C**キーを押してクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="75e17-152">Select the code in the following code example and then press **CTRL+C** to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="75e17-153">[マクロデザイナー] ウィンドウをアクティブにして、CTRL キーを押し**ながら V**キーを押します。</span><span class="sxs-lookup"><span data-stu-id="75e17-153">Activate the macro designer window and then press **CTRL+V**.</span></span>



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

<span data-ttu-id="75e17-154">次の例は、" RaiseError" アクションを使用して Before Change データ マクロ イベントを取り消す方法を示します。</span><span class="sxs-lookup"><span data-stu-id="75e17-154">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="75e17-155">AssignedTo フィールドが更新されると、 LookupRecord データ ブロックを使用して、割り当てられた技術者が未解決サービス リクエストに現在割り当てられているかどうかが確認されます。</span><span class="sxs-lookup"><span data-stu-id="75e17-155">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="75e17-156">これが true の場合、Before Change イベントは取り消され、レコードは更新されません。</span><span class="sxs-lookup"><span data-stu-id="75e17-156">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="75e17-157">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="75e17-157">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
