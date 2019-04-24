---
title: RemoveAllTempVars マクロ アクション
TOCTitle: RemoveAllTempVars macro action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: eade809a6e3982dc0dc4cf94ae382af72e8f454e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306798"
---
# <a name="removealltempvars-macro-action"></a><span data-ttu-id="6ac84-102">RemoveAllTempVars マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="6ac84-102">RemoveAllTempVars macro action</span></span>


<span data-ttu-id="6ac84-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ac84-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="6ac84-104">"RemoveAllTempVars/すべての一時変数の削除" アクションは、"SetTempVar/一時変数の設定" アクションを使用して作成したすべての一時変数を削除するために使用します。</span><span class="sxs-lookup"><span data-stu-id="6ac84-104">You can use the **RemoveAllTempVars** action to remove any temporary variables that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="6ac84-105">Setting</span><span class="sxs-lookup"><span data-stu-id="6ac84-105">Setting</span></span>

<span data-ttu-id="6ac84-106">"RemoveAllTempVars/すべての一時変数の削除" アクションには、引数はありません。</span><span class="sxs-lookup"><span data-stu-id="6ac84-106">The **RemoveAllTempVars** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ac84-107">注釈</span><span class="sxs-lookup"><span data-stu-id="6ac84-107">Remarks</span></span>

  - <span data-ttu-id="6ac84-p101">一度に定義しておくことのできる一時変数は、最大 255 個です。一時変数は、削除しなければ、データベースまたはプロジェクトを閉じるまでメモリに残ったままとなります。不要となった一時変数は削除することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6ac84-p101">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database or project. It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="6ac84-111">データベースまたはプロジェクトを閉じると、すべての一時変数が自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="6ac84-111">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="6ac84-112">To remove a single temporary variable, use the **RemoveTempVar** action and set its argument to the name of the temporary variable you want to remove.</span><span class="sxs-lookup"><span data-stu-id="6ac84-112">To remove a single temporary variable, use the **RemoveTempVar** action and set its argument to the name of the temporary variable you want to remove.</span></span>

  - <span data-ttu-id="6ac84-113">To run the **RemoveAllTempVars** action in a VBA module, use the **RemoveAll** method of the **TempVars** object.</span><span class="sxs-lookup"><span data-stu-id="6ac84-113">To run the **RemoveAllTempVars** action in a VBA module, use the **RemoveAll** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="6ac84-114">例</span><span class="sxs-lookup"><span data-stu-id="6ac84-114">Example</span></span>

<span data-ttu-id="6ac84-115">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveAllTempVars** action.</span><span class="sxs-lookup"><span data-stu-id="6ac84-115">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveAllTempVars** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6ac84-116">条件</span><span class="sxs-lookup"><span data-stu-id="6ac84-116">Condition</span></span></p></th>
<th><p><span data-ttu-id="6ac84-117">アクション</span><span class="sxs-lookup"><span data-stu-id="6ac84-117">Action</span></span></p></th>
<th><p><span data-ttu-id="6ac84-118">引数</span><span class="sxs-lookup"><span data-stu-id="6ac84-118">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6ac84-119"><strong>SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="6ac84-119"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="6ac84-120"><strong>名前</strong>: MyVar<strong>Expression</strong>: InputBox (&quot;0 以外の数値を入力し&quot;ます。)</span><span class="sxs-lookup"><span data-stu-id="6ac84-120"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ac84-121">[TempVars]![MyVar]&lt;&gt;0</span><span class="sxs-lookup"><span data-stu-id="6ac84-121">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="6ac84-122"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="6ac84-122"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="6ac84-123"><strong>メッセージ</strong>: =&quot;入力&quot; &amp;した [TempVars]!MyVar&amp; &quot;.&quot;<strong>警告音</strong>: <strong>yestype</strong>:<strong>情報</strong></span><span class="sxs-lookup"><span data-stu-id="6ac84-123"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6ac84-124"><strong>RemoveAllTempVars</strong></span><span class="sxs-lookup"><span data-stu-id="6ac84-124"><strong>RemoveAllTempVars</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

