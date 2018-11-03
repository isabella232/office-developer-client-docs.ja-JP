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
# <a name="lookuprecord-data-block"></a><span data-ttu-id="aaab9-102">不一致データのブロック</span><span class="sxs-lookup"><span data-stu-id="aaab9-102">LookupRecord data block</span></span>

<span data-ttu-id="aaab9-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="aaab9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aaab9-104">**LookupRecord** データ ブロックは、特定のレコードに対して一連のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="aaab9-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span>

> [!NOTE]
> <span data-ttu-id="aaab9-105">[!メモ] **LookupRecord** データ ブロックは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="aaab9-105">The **LookupRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="aaab9-106">設定</span><span class="sxs-lookup"><span data-stu-id="aaab9-106">Setting</span></span>

<span data-ttu-id="aaab9-107">**LookupRecord** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="aaab9-107">The **SetField** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aaab9-108">引数</span><span class="sxs-lookup"><span data-stu-id="aaab9-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="aaab9-109">必須</span><span class="sxs-lookup"><span data-stu-id="aaab9-109">Required</span></span></p></th>
<th><p><span data-ttu-id="aaab9-110">説明</span><span class="sxs-lookup"><span data-stu-id="aaab9-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aaab9-111">In</span><span class="sxs-lookup"><span data-stu-id="aaab9-111">In</span></span></p></td>
<td><p><span data-ttu-id="aaab9-112">はい</span><span class="sxs-lookup"><span data-stu-id="aaab9-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="aaab9-113">操作対象のレコードを識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="aaab9-113">A string that identifies the record to operate on.</span></span> <span data-ttu-id="aaab9-114"><em></em>引数は、テーブル、選択クエリ、または SQL ステートメントの名前を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="aaab9-114">The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p>

> [!NOTE]
> <span data-ttu-id="aaab9-115">指定したレコードには、リンク テーブルまたは ODBC データ ソース内のデータを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="aaab9-115">The specified record cannot include data stored in a linked table or ODBC data source.</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aaab9-116">Where Condition/Where 条件式</span><span class="sxs-lookup"><span data-stu-id="aaab9-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="aaab9-117">いいえ</span><span class="sxs-lookup"><span data-stu-id="aaab9-117">No</span></span></p></td>
<td><p><span data-ttu-id="aaab9-p102"><strong>LookupRecord</strong> データ ブロックを適用するデータの範囲を制限するための文字列式を指定します。たとえば、多くの場合、抽出条件は SQL 式の WHERE 句と同じ役割を果たします (ただし WHERE という語は使用しません)。抽出条件を省略すると、<strong>LookupRecord</strong> データ ブロックは <em>In</em> 引数で指定したドメイン全体に適用されます。抽出条件に含めるフィールドは、<em>In</em> にも含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="aaab9-p102">A string expression used to restrict the range of data on which the <strong>LookupRecord</strong> data block is performed. For example, criteria are often equivalent to the WHERE clause in an SQL expression, without the word WHERE. If criteria are omitted, the <strong>LookupRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument. Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aaab9-122">エイリアス</span><span class="sxs-lookup"><span data-stu-id="aaab9-122">Alias</span></span></p></td>
<td><p><span data-ttu-id="aaab9-123">いいえ</span><span class="sxs-lookup"><span data-stu-id="aaab9-123">No</span></span></p></td>
<td><p><span data-ttu-id="aaab9-124"><em></em>引数で指定されたレコードに別の名前を提供する文字列です。</span><span class="sxs-lookup"><span data-stu-id="aaab9-124">A string that provides an alternative name for the record specified by the <em>In</em> argument.</span></span> <span data-ttu-id="aaab9-125">あいまいな参照を防ぐへの参照のテーブル名を短くには、よく使用されます。</span><span class="sxs-lookup"><span data-stu-id="aaab9-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="aaab9-126"><em>エイリアス</em>が指定されていない場合、テーブルまたはクエリの名前がエイリアスとして使用します。</span><span class="sxs-lookup"><span data-stu-id="aaab9-126">If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="aaab9-127">備考</span><span class="sxs-lookup"><span data-stu-id="aaab9-127">Remarks</span></span>

<span data-ttu-id="aaab9-128">\*\* *条件*引数で指定した抽出条件は、複数のレコードを指定する場合、**不一致**のデータ ブロック、最初のレコードにのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="aaab9-128">If the criteria specified by the *In* and *Where Condition* arguments specifies more than one record, the **LookupRecord** data block will operate only on the first record.</span></span>

## <a name="example"></a><span data-ttu-id="aaab9-129">例</span><span class="sxs-lookup"><span data-stu-id="aaab9-129">Example</span></span>

<span data-ttu-id="aaab9-p104">次の例は、 SetReturnVar アクションを使用して名前付きデータ マクロから値を返す方法を示します。" CurrentServiceRequest" という名前の **ReturnVar** が、名前付きデータ マクロの呼び出し元であるマクロまたは Visual Basic for Applications (VBA) サブルーチンに返されます。</span><span class="sxs-lookup"><span data-stu-id="aaab9-p104">The following example shows how to use the SetReturnVar action to return a value from a named data macro. A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="aaab9-132">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="aaab9-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="aaab9-p105">次の例は、" RaiseError" アクションを使用して Before Change データ マクロ イベントを取り消す方法を示します。 AssignedTo フィールドが更新されると、 LookupRecord データ ブロックを使用して、割り当てられた技術者が未解決サービス リクエストに現在割り当てられているかどうかが確認されます。これが真の場合、 Before Change イベントが取り消されて、レコードは更新されません。</span><span class="sxs-lookup"><span data-stu-id="aaab9-p105">The following example shows how to use the RaiseError action to cancel the Before Change data macro event. When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request. If this is true, the Before Change event is cancelled and the record is not updated.</span></span>

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
