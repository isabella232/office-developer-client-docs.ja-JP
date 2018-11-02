---
title: SetTempVar マクロ アクション
TOCTitle: SetTempVar macro action
ms:assetid: 9c3b7bee-02c5-efbf-1276-4c4a1f7802d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198102(v=office.15)
ms:contentKeyID: 48546593
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm150219
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 342a4db4e2ed6e06dca917beb96b4562f1fc65da
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919445"
---
# <a name="settempvar-macro-action"></a><span data-ttu-id="aebf1-102">SetTempVar マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="aebf1-102">SetTempVar macro action</span></span>


<span data-ttu-id="aebf1-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="aebf1-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="aebf1-p101">**SetTempVar** アクションは、一時変数を作成し、特定の値に設定するために使用します。作成した変数は、後続のアクションで条件や引数として使用したり、別のマクロ、イベント プロシージャ、フォーム、またはレポートで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="aebf1-p101">You can use the **SetTempVar** action to create a temporary variable and set it to a specific value. The variable can then be used as a condition or argument in subsequent actions, or you can use the variable in another macro, in an event procedure, or on a form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="aebf1-106">設定</span><span class="sxs-lookup"><span data-stu-id="aebf1-106">Setting</span></span>

<span data-ttu-id="aebf1-107">**SetTempVar** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="aebf1-107">The **SetTempVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aebf1-108">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="aebf1-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="aebf1-109">説明</span><span class="sxs-lookup"><span data-stu-id="aebf1-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aebf1-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="aebf1-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="aebf1-111">一時変数の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="aebf1-111">Enter the name of the temporary variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aebf1-112"><strong>Expression/式</strong></span><span class="sxs-lookup"><span data-stu-id="aebf1-112"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="aebf1-113">この一時変数の値を設定するために使用する式を入力します。</span><span class="sxs-lookup"><span data-stu-id="aebf1-113">Enter an expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="aebf1-114">等号を含む式の前の操作を行います (<strong>=</strong>) 記号。</span><span class="sxs-lookup"><span data-stu-id="aebf1-114">Do not precede the expression with the equal (<strong>=</strong>) sign.</span></span> <span data-ttu-id="aebf1-115">[<strong>ビルド</strong>] ボタンをクリックすることができます。</span><span class="sxs-lookup"><span data-stu-id="aebf1-115">You can click the <strong>Build</strong> button</span></span> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> <span data-ttu-id="aebf1-117">(ビルド) をクリックすると、式ビルダーを使用してこの引数を設定できます。</span><span class="sxs-lookup"><span data-stu-id="aebf1-117">to use the Expression Builder to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="aebf1-118">解説</span><span class="sxs-lookup"><span data-stu-id="aebf1-118">Remarks</span></span>

- <span data-ttu-id="aebf1-p103">一度に定義しておくことのできる一時変数は、最大 255 個です。一時変数は、削除しなければ、データベースを閉じるまでメモリに残ったままとなります。不要になった一時変数は削除することをお勧めします。特定の一時変数を削除するには、削除する一時変数の名前を引数に指定して **[RemoveTempVar](removetempvar-macro-action.md)** アクションを実行します。複数の一時変数を一括して削除するには、 **RemoveAllTempVars** アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="aebf1-p103">You can have up to 255 temporary variables defined at one time. If you do not remove a temporary variable, it will remain in memory until you close the database. It is a good practice to remove temporary variables when you are finished using them. To remove a single temporary variable, use the **[RemoveTempVar](removetempvar-macro-action.md)** action and set its argument to the name of the temporary variable that you want to remove. If you have more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

- <span data-ttu-id="aebf1-124">一時変数はグローバルな変数です。</span><span class="sxs-lookup"><span data-stu-id="aebf1-124">Temporary variables are global.</span></span> <span data-ttu-id="aebf1-125">一時変数は、作成されると、イベント プロシージャ、Visual Basic for Applications (VBA) モジュール、クエリ、または式で参照できます。</span><span class="sxs-lookup"><span data-stu-id="aebf1-125">Once a temporary variable has been created, you can refer to it in an event procedure, a Visual Basic for Applications (VBA) module, a query, or an expression.</span></span> <span data-ttu-id="aebf1-126">たとえば、 *MyVar*をという名前の一時変数を作成した場合可能性があります変数を使用するコントロールのソースとしてテキスト ボックスの次の構文を使用しています。</span><span class="sxs-lookup"><span data-stu-id="aebf1-126">For example, if you created a temporary variable named *MyVar*, you could use the variable as the control source for a text box by using the following syntax:</span></span>
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > <span data-ttu-id="aebf1-127">[!メモ] マクロ、クエリ、およびイベント プロシージャでは、式の前に等号 (=) を付ける必要はありません。</span><span class="sxs-lookup"><span data-stu-id="aebf1-127">In macros, queries and event procedures, you do not need to precede the expression with an equal sign.</span></span>
 
  <span data-ttu-id="aebf1-128">一時変数は、アドインまたは参照先データベースでも参照できます。</span><span class="sxs-lookup"><span data-stu-id="aebf1-128">You can also refer to temporary variables in any add-ins or referenced databases.</span></span>

- <span data-ttu-id="aebf1-129">VBA モジュールで **SetTempVar** アクションを実行するには、 **TempVars** オブジェクトの **Add** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="aebf1-129">To run the **SetTempVar** action in a VBA module, use the **Add** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="aebf1-130">例</span><span class="sxs-lookup"><span data-stu-id="aebf1-130">Example</span></span>

<span data-ttu-id="aebf1-131">次のマクロでは、 **SetTempVar** アクションを使用して一時変数を作成し、条件およびメッセージ ボックスで一時変数を使用してから削除する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="aebf1-131">The following macro demonstrates how to create a temporary variable by using the **SetTempVar** action, then using the temporary variable in a condition and a message box, and then removing the temporary variable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aebf1-132">条件</span><span class="sxs-lookup"><span data-stu-id="aebf1-132">Condition</span></span></p></th>
<th><p><span data-ttu-id="aebf1-133">アクション</span><span class="sxs-lookup"><span data-stu-id="aebf1-133">Action</span></span></p></th>
<th><p><span data-ttu-id="aebf1-134">引数</span><span class="sxs-lookup"><span data-stu-id="aebf1-134">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="aebf1-135"><strong>SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="aebf1-135"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="aebf1-136"><strong>名前</strong>: MyVar<strong>式</strong>: InputBox (&quot;、0 以外の数値を入力してください&quot;)。</span><span class="sxs-lookup"><span data-stu-id="aebf1-136"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aebf1-137">[TempVars]![MyVar]&lt;&gt;0</span><span class="sxs-lookup"><span data-stu-id="aebf1-137">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="aebf1-138"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="aebf1-138"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="aebf1-139"><strong>メッセージ</strong>: =&quot;を入力する&quot; &amp; [一時変数]![MyVar]&amp; &quot;.&quot;<strong>ビープ音を鳴らす</strong>: <strong>YesType</strong>:<strong>情報</strong></span><span class="sxs-lookup"><span data-stu-id="aebf1-139"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="aebf1-140"><strong>RemoveTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="aebf1-140"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="aebf1-141"><strong>Name/名前</strong>: MyVar</span><span class="sxs-lookup"><span data-stu-id="aebf1-141"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

