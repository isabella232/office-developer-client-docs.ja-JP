---
title: "'RemoveAllTempVars/すべての一時変数の削除' マクロ アクション"
TOCTitle: RemoveAllTempVars Macro Action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 49b92f90fb26ea1f7ad5f0878a7479267b35bdaf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870794"
---
# <a name="removealltempvars-macro-action"></a><span data-ttu-id="a6d88-102">"RemoveAllTempVars/すべての一時変数の削除" マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="a6d88-102">RemoveAllTempVars Macro Action</span></span>


<span data-ttu-id="a6d88-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a6d88-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="a6d88-104">**SetTempVar**アクションを使用して作成したすべての一時変数を削除するのには**RemoveAllTempVars**アクションを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="a6d88-104">You can use the **RemoveAllTempVars** action to remove any temporary variables that you created by using the **SetTempVar** action.</span></span>

## <a name="setting"></a><span data-ttu-id="a6d88-105">設定値</span><span class="sxs-lookup"><span data-stu-id="a6d88-105">Setting</span></span>

<span data-ttu-id="a6d88-106">**RemoveAllTempVars**アクションの引数ではありません。</span><span class="sxs-lookup"><span data-stu-id="a6d88-106">The **RemoveAllTempVars** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6d88-107">解説</span><span class="sxs-lookup"><span data-stu-id="a6d88-107">Remarks</span></span>

  - <span data-ttu-id="a6d88-p101">一度に定義しておくことのできる一時変数は、最大 255 個です。一時変数は、削除しなければ、データベースまたはプロジェクトを閉じるまでメモリに残ったままとなります。不要となった一時変数は削除することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a6d88-p101">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database or project. It is a good practice to remove temporary variables when you are finished using them.</span></span>

  - <span data-ttu-id="a6d88-111">データベースまたはプロジェクトを閉じると、すべての一時変数が自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="a6d88-111">Access automatically removes all temporary variables when you close the database or project.</span></span>

  - <span data-ttu-id="a6d88-112">1 つの一時変数を削除するに**RemoveTempVar**アクションを使用して、その引数を削除する一時変数の名前に設定します。</span><span class="sxs-lookup"><span data-stu-id="a6d88-112">To remove a single temporary variable, use the **RemoveTempVar** action and set its argument to the name of the temporary variable you want to remove.</span></span>

  - <span data-ttu-id="a6d88-113">VBA モジュールで**RemoveAllTempVars**アクションを実行するには、**一時変数**オブジェクトの**RemoveAll**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a6d88-113">To run the **RemoveAllTempVars** action in a VBA module, use the **RemoveAll** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="a6d88-114">使用例</span><span class="sxs-lookup"><span data-stu-id="a6d88-114">Example</span></span>

<span data-ttu-id="a6d88-115">次のマクロでは、一時変数を作成し、条件とメッセージ ボックスで使用して、 **RemoveAllTempVars**アクションを使用して一時変数を削除する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="a6d88-115">The following macro demonstrates how to create a temporary variable, use it in a condition and a message box, and then remove the temporary variable by using the **RemoveAllTempVars** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a6d88-116">条件</span><span class="sxs-lookup"><span data-stu-id="a6d88-116">Condition</span></span></p></th>
<th><p><span data-ttu-id="a6d88-117">アクション</span><span class="sxs-lookup"><span data-stu-id="a6d88-117">Action</span></span></p></th>
<th><p><span data-ttu-id="a6d88-118">引数</span><span class="sxs-lookup"><span data-stu-id="a6d88-118">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="a6d88-119"><strong>SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="a6d88-119"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="a6d88-120"><strong>名前</strong>: MyVar<strong>式</strong>: InputBox (&quot;、0 以外の数値を入力してください&quot;)。</span><span class="sxs-lookup"><span data-stu-id="a6d88-120"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6d88-121">[TempVars]![MyVar]&lt;&gt;0</span><span class="sxs-lookup"><span data-stu-id="a6d88-121">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="a6d88-122"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="a6d88-122"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="a6d88-123"><strong>メッセージ</strong>: =&quot;を入力する&quot; &amp; [一時変数]![MyVar]&amp; &quot;.&quot;<strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>:<strong>情報</strong></span><span class="sxs-lookup"><span data-stu-id="a6d88-123"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="a6d88-124"><strong>RemoveAllTempVars</strong></span><span class="sxs-lookup"><span data-stu-id="a6d88-124"><strong>RemoveAllTempVars</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

