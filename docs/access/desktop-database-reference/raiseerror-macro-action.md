---
title: RaiseError マクロ アクション
TOCTitle: RaiseError macro action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e3e778c8dce83ecad32328f0d7ad762d9f825a6d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919781"
---
# <a name="raiseerror-macro-action"></a><span data-ttu-id="132f1-102">RaiseError マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="132f1-102">RaiseError macro action</span></span>

<span data-ttu-id="132f1-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="132f1-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="132f1-104">**RaiseError**アクションは、**[エラー時](onerror-macro-action.md)** のマクロ アクションで処理できる例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="132f1-104">The **RaiseError** action throws an exception that can be handled by the **[OnError](onerror-macro-action.md)** macro action.</span></span>

> [!NOTE]
> <span data-ttu-id="132f1-105">[!メモ] " **RaiseError** /エラーの生成" アクションは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="132f1-105">The **RaiseError** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="132f1-106">設定</span><span class="sxs-lookup"><span data-stu-id="132f1-106">Setting</span></span>

<span data-ttu-id="132f1-107">**RaiseError**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="132f1-107">The **RaiseError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="132f1-108">引数</span><span class="sxs-lookup"><span data-stu-id="132f1-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="132f1-109">必須</span><span class="sxs-lookup"><span data-stu-id="132f1-109">Required</span></span></p></th>
<th><p><span data-ttu-id="132f1-110">説明</span><span class="sxs-lookup"><span data-stu-id="132f1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="132f1-111">Error Number/エラー番号</span><span class="sxs-lookup"><span data-stu-id="132f1-111">Error Number</span></span></p></td>
<td><p><span data-ttu-id="132f1-112">はい</span><span class="sxs-lookup"><span data-stu-id="132f1-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="132f1-113">長整数型のデータ入力に解決される数値または式。</span><span class="sxs-lookup"><span data-stu-id="132f1-113">A number or an expression that resolves to the Long data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="132f1-114">Error Description/エラー説明</span><span class="sxs-lookup"><span data-stu-id="132f1-114">Error Description</span></span></p></td>
<td><p><span data-ttu-id="132f1-115">いいえ</span><span class="sxs-lookup"><span data-stu-id="132f1-115">No</span></span></p></td>
<td><p><span data-ttu-id="132f1-116">エラーを説明する文字列式。</span><span class="sxs-lookup"><span data-stu-id="132f1-116">A string expression that describes the error.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="132f1-117">備考</span><span class="sxs-lookup"><span data-stu-id="132f1-117">Remarks</span></span>

<span data-ttu-id="132f1-118">**RaiseError**アクションは、**[前に変更](before-change-macro-event.md)** または**[削除をする前に](before-delete-macro-event.md)** マクロのイベントで呼び出されると、イベントはキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="132f1-118">If the **RaiseError** action is called in a **[Before Change](before-change-macro-event.md)** or **[Before Delete](before-delete-macro-event.md)** macro event, the event is cancelled.</span></span>

<span data-ttu-id="132f1-119">エラーの処理は、**エラー時**のアクティブなステートメントがない場合、 **RaiseError**操作によってスローされたエラーは、 **USysApplicationLog**システム ・ テーブルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="132f1-119">If there is not an active **OnError** statment that is handling errors, then the error thrown by the **RaiseError** action is added to the **USysApplicationLog** system table.</span></span> <span data-ttu-id="132f1-120">**RaiseError**の動作は、 **USysApplicationLog**テーブルに書き込み、 **[カテゴリ**] 列が自動的に**実行**する設定します。</span><span class="sxs-lookup"><span data-stu-id="132f1-120">When the **RaiseError** action to writes to the **USysApplicationLog** table, the **Category** column is automatically set to **Execution**.</span></span>

<span data-ttu-id="132f1-121">**USysApplicationLog**テーブルを表示するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="132f1-121">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="132f1-122">[**ファイル**] メニューのをクリックし、[**オプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="132f1-122">Click the **File** menu, and then click **Options**.</span></span>

2.  <span data-ttu-id="132f1-123">[ **Access のオプション**] ダイアログ ボックスで [ **カレント データベース**] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="132f1-123">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="132f1-124">[ **ナビゲーション**] セクションで [ **ナビゲーション オプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="132f1-124">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="132f1-125">[ **ナビゲーション オプション**] ダイアログ ボックスで [ **システム オブジェクトの表示**] をクリックし、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="132f1-125">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="132f1-126">[ **OK**] をクリックして [ **Access のオプション**] ダイアログ ボックスを終了します。</span><span class="sxs-lookup"><span data-stu-id="132f1-126">Click **OK** to dismiss the **Access Options** dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="132f1-127">例</span><span class="sxs-lookup"><span data-stu-id="132f1-127">Example</span></span>

<span data-ttu-id="132f1-128">次の例は、" RaiseError" アクションを使用して Before Change データ マクロ イベントを取り消す方法を示します。</span><span class="sxs-lookup"><span data-stu-id="132f1-128">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="132f1-129">AssignedTo フィールドが更新されると、 LookupRecord データ ブロックを使用して、割り当てられた技術者が未解決サービス リクエストに現在割り当てられているかどうかが確認されます。</span><span class="sxs-lookup"><span data-stu-id="132f1-129">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="132f1-130">これが true の場合は、変更する前にイベントをキャンセルするとレコードは更新されません。</span><span class="sxs-lookup"><span data-stu-id="132f1-130">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="132f1-131">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="132f1-131">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
