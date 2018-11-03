---
title: RemoveTempVar マクロ アクション
TOCTitle: RemoveTempVar macro action
ms:assetid: 7bcc5010-3e30-ecef-2c5d-a35e73c8e325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196352(v=office.15)
ms:contentKeyID: 48545822
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm147125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e43181626b885664eaf370decb7d471082c7a263
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928118"
---
# <a name="removetempvar-macro-action"></a><span data-ttu-id="b31a9-102">RemoveTempVar マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="b31a9-102">RemoveTempVar macro action</span></span>


<span data-ttu-id="b31a9-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b31a9-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="b31a9-104">**RemoveTempVar**アクションを使用すると、 **SetTempVar**アクションを使用して作成した 1 つの一時変数を削除します。</span><span class="sxs-lookup"><span data-stu-id="b31a9-104">You can use the **RemoveTempVar** action to remove a single temporary variable that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="b31a9-105">設定値</span><span class="sxs-lookup"><span data-stu-id="b31a9-105">Setting</span></span>

<span data-ttu-id="b31a9-106">**RemoveTempVar**アクションには、次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="b31a9-106">The **RemoveTempVar** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b31a9-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="b31a9-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b31a9-108">説明</span><span class="sxs-lookup"><span data-stu-id="b31a9-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b31a9-109"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="b31a9-109"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b31a9-110">削除する一時変数の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b31a9-110">Enter the name of the temporary variable you want to remove.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b31a9-111">解説</span><span class="sxs-lookup"><span data-stu-id="b31a9-111">Remarks</span></span>

  - <span data-ttu-id="b31a9-p101">一度に定義しておくことのできる一時変数は、最大 255 個です。一時変数は、削除しなければ、データベースを閉じるまでメモリに残ったままとなります。不要となった一時変数は削除することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b31a9-p101">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database. It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="b31a9-115">データベースまたはプロジェクトを閉じると、すべての一時変数が自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="b31a9-115">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="b31a9-p102">削除対象の変数の名前を誤って入力しても、エラーは表示されません。その削除対象の変数は、データベースを閉じるまでメモリに残ったままとなります。</span><span class="sxs-lookup"><span data-stu-id="b31a9-p102">If you misspell the name of the variable to be removed, Access does not display an error. The variable you wanted to remove will remain in memory until you close the database.</span></span>

  - <span data-ttu-id="b31a9-118">1 つ以上の一時的な変数を作成し、それらを一度にすべて削除する、 **RemoveAllTempVars**アクションを使用してください。</span><span class="sxs-lookup"><span data-stu-id="b31a9-118">If you have created more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

  - <span data-ttu-id="b31a9-119">VBA モジュールで**RemoveTempVar**アクションを実行するには、**一時変数**オブジェクトの**Remove**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b31a9-119">To run the **RemoveTempVar** action in a VBA module, use the **Remove** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="b31a9-120">使用例</span><span class="sxs-lookup"><span data-stu-id="b31a9-120">Example</span></span>

<span data-ttu-id="b31a9-121">次のマクロでは、一時変数を作成し、条件とメッセージ ボックスで使用して、 **RemoveTempVar**アクションを使用して一時変数を削除する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b31a9-121">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveTempVar** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b31a9-122">条件</span><span class="sxs-lookup"><span data-stu-id="b31a9-122">Condition</span></span></p></th>
<th><p><span data-ttu-id="b31a9-123">アクション</span><span class="sxs-lookup"><span data-stu-id="b31a9-123">Action</span></span></p></th>
<th><p><span data-ttu-id="b31a9-124">引数</span><span class="sxs-lookup"><span data-stu-id="b31a9-124">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b31a9-125"><strong>SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="b31a9-125"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="b31a9-126"><strong>名前</strong>: MyVar<strong>式</strong>: InputBox (&quot;、0 以外の数値を入力してください&quot;)。</span><span class="sxs-lookup"><span data-stu-id="b31a9-126"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b31a9-127">[TempVars]![MyVar]&lt;&gt;0</span><span class="sxs-lookup"><span data-stu-id="b31a9-127">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="b31a9-128"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="b31a9-128"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="b31a9-129"><strong>メッセージ</strong>: =&quot;を入力する&quot; &amp; [一時変数]![MyVar]&amp; &quot;.&quot;<strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>:<strong>情報</strong></span><span class="sxs-lookup"><span data-stu-id="b31a9-129"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b31a9-130"><strong>RemoveTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="b31a9-130"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="b31a9-131"><strong>Name/名前</strong>: MyVar</span><span class="sxs-lookup"><span data-stu-id="b31a9-131"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

