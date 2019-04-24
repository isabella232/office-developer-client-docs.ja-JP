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
localization_priority: Normal
ms.openlocfilehash: 5051cfd74f2a745ee430f2ed8a20445d2f9965f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306756"
---
# <a name="removetempvar-macro-action"></a><span data-ttu-id="ca639-102">RemoveTempVar マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="ca639-102">RemoveTempVar macro action</span></span>


<span data-ttu-id="ca639-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca639-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="ca639-104">"RemoveTempVar/一時変数の削除" アクションは、"SetTempVar/一時変数の設定" アクションを使用して作成した １ つの一時変数を削除するために使用します。</span><span class="sxs-lookup"><span data-stu-id="ca639-104">You can use the **RemoveTempVar** action to remove a single temporary variable that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="ca639-105">Setting</span><span class="sxs-lookup"><span data-stu-id="ca639-105">Setting</span></span>

<span data-ttu-id="ca639-106">"RemoveTempVar/一時変数の削除" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ca639-106">The **RemoveTempVar** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca639-107">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="ca639-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ca639-108">説明</span><span class="sxs-lookup"><span data-stu-id="ca639-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca639-109"><strong>名前</strong></span><span class="sxs-lookup"><span data-stu-id="ca639-109"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ca639-110">削除する一時変数の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca639-110">Enter the name of the temporary variable you want to remove.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ca639-111">注釈</span><span class="sxs-lookup"><span data-stu-id="ca639-111">Remarks</span></span>

  - <span data-ttu-id="ca639-p101">一度に定義しておくことのできる一時変数は、最大 255 個です。一時変数は、削除しなければ、データベースを閉じるまでメモリに残ったままとなります。不要となった一時変数は削除することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ca639-p101">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database. It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="ca639-115">データベースまたはプロジェクトを閉じると、すべての一時変数が自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="ca639-115">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="ca639-p102">削除対象の変数の名前を誤って入力しても、エラーは表示されません。その削除対象の変数は、データベースを閉じるまでメモリに残ったままとなります。</span><span class="sxs-lookup"><span data-stu-id="ca639-p102">If you misspell the name of the variable to be removed, Access does not display an error. The variable you wanted to remove will remain in memory until you close the database.</span></span>

  - <span data-ttu-id="ca639-118">If you have created more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span><span class="sxs-lookup"><span data-stu-id="ca639-118">If you have created more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

  - <span data-ttu-id="ca639-119">To run the **RemoveTempVar** action in a VBA module, use the **Remove** method of the **TempVars** object.</span><span class="sxs-lookup"><span data-stu-id="ca639-119">To run the **RemoveTempVar** action in a VBA module, use the **Remove** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="ca639-120">例</span><span class="sxs-lookup"><span data-stu-id="ca639-120">Example</span></span>

<span data-ttu-id="ca639-121">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveTempVar** action.</span><span class="sxs-lookup"><span data-stu-id="ca639-121">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveTempVar** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca639-122">条件</span><span class="sxs-lookup"><span data-stu-id="ca639-122">Condition</span></span></p></th>
<th><p><span data-ttu-id="ca639-123">アクション</span><span class="sxs-lookup"><span data-stu-id="ca639-123">Action</span></span></p></th>
<th><p><span data-ttu-id="ca639-124">引数</span><span class="sxs-lookup"><span data-stu-id="ca639-124">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ca639-125"><strong>SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="ca639-125"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="ca639-126"><strong>名前</strong>: MyVar<strong>Expression</strong>: InputBox (&quot;0 以外の数値を入力し&quot;ます。)</span><span class="sxs-lookup"><span data-stu-id="ca639-126"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca639-127">[TempVars]![MyVar]&lt;&gt;0</span><span class="sxs-lookup"><span data-stu-id="ca639-127">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="ca639-128"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="ca639-128"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="ca639-129"><strong>メッセージ</strong>: =&quot;入力&quot; &amp;した [TempVars]!MyVar&amp; &quot;.&quot;<strong>警告音</strong>: <strong>yestype</strong>:<strong>情報</strong></span><span class="sxs-lookup"><span data-stu-id="ca639-129"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ca639-130"><strong>RemoveTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="ca639-130"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="ca639-131"><strong>Name/名前</strong>: MyVar</span><span class="sxs-lookup"><span data-stu-id="ca639-131"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

