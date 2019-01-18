---
title: CancelEvent マクロ アクション
TOCTitle: CancelEvent macro action
ms:assetid: d9d3ea99-c9fb-2524-c570-e3ee6d20af98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835110(v=office.15)
ms:contentKeyID: 48548066
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm78430
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b55fc51f70bcc2c9d2f7e93cf9c79228cd2fe440
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710175"
---
# <a name="cancelevent-macro-action"></a><span data-ttu-id="c1538-102">CancelEvent マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="c1538-102">CancelEvent macro action</span></span>

<span data-ttu-id="c1538-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c1538-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c1538-p101">" **CancelEvent/イベントのキャンセル** " アクションを使用して、このアクションが定義されたマクロが Access で実行される原因となったイベントを取り消すことができます。" **BeforeUpdate/更新前処理** "、" **OnOpen/開く時** "、" **OnUnload/読み込み解除時** "、" **OnPrint/印刷時** " などのイベント プロパティに、このマクロ名を設定します。</span><span class="sxs-lookup"><span data-stu-id="c1538-p101">You can use the **CancelEvent** action to cancel the event that caused Access to run the macro containing this action. The macro name is the setting of an event property such as **BeforeUpdate**, **OnOpen**, **OnUnload**, or **OnPrint**.</span></span>

## <a name="setting"></a><span data-ttu-id="c1538-106">設定値</span><span class="sxs-lookup"><span data-stu-id="c1538-106">Setting</span></span>

<span data-ttu-id="c1538-107">**モーダル**引数はありません。</span><span class="sxs-lookup"><span data-stu-id="c1538-107">The **CancelEvent** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1538-108">解説</span><span class="sxs-lookup"><span data-stu-id="c1538-108">Remarks</span></span>

<span data-ttu-id="c1538-109">フォームでは、通常に、 **BeforeUpdate**イベントのプロパティに入力検査マクロで**イベントのキャンセル**操作を使用します。</span><span class="sxs-lookup"><span data-stu-id="c1538-109">In a form, you typically use the **CancelEvent** action in a validation macro with the **BeforeUpdate** event property.</span></span> <span data-ttu-id="c1538-110">コントロールまたはレコードにデータを入力すると、ときに、データベースにデータを追加する前にマクロが実行されます。</span><span class="sxs-lookup"><span data-stu-id="c1538-110">When a user enters data in a control or record, Access runs the macro before adding the data to the database.</span></span> <span data-ttu-id="c1538-111">データには、マクロの入力検査の条件が失敗した場合、**イベントのキャンセル**操作は、開始する前に更新処理をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="c1538-111">If the data fails the validation conditions in the macro, the **CancelEvent** action cancels the update process before it starts.</span></span>

<span data-ttu-id="c1538-112">多くの場合、アクションを使用するこのアクションが**メッセージ ボックス**で、データの入力検査の条件が失敗したことを示すために、入力されるデータの種類に関する有用な情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="c1538-112">Often, you use this action with the **MessageBox** action to indicate that the data has failed the validation conditions and to provide helpful information about the kind of data that should be entered.</span></span>

<span data-ttu-id="c1538-113">次のイベントは、**イベントのキャンセル**操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="c1538-113">The following events can be canceled by the **CancelEvent** action.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1538-114"><strong>ApplyFilter</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-114"><strong>ApplyFilter</strong></span></span></p></td>
<td><p><span data-ttu-id="c1538-115"><strong>Dirty</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-115"><strong>Dirty</strong></span></span></p></td>
<td><p><span data-ttu-id="c1538-116"><strong>MouseDown</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-116"><strong>MouseDown</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1538-117"><strong>BeforeDelConfirm</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-117"><strong>BeforeDelConfirm</strong></span></span></p></td>
<td><p><span data-ttu-id="c1538-118"><strong>Exit</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-118"><strong>Exit</strong></span></span></p></td>
<td><p><span data-ttu-id="c1538-119"><strong>NoData</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-119"><strong>NoData</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1538-120"><strong>BeforeInsert</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-120"><strong>BeforeInsert</strong></span></span></p></td>
<td><p><span data-ttu-id="c1538-121"><strong>Filter</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-121"><strong>Filter</strong></span></span></p></td>
<td><p><span data-ttu-id="c1538-122"><strong>Open</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-122"><strong>Open</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1538-123"><strong>BeforeUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-123"><strong>BeforeUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="c1538-124"><strong>Format</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-124"><strong>Format</strong></span></span></p></td>
<td><p><span data-ttu-id="c1538-125"><strong>Print</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-125"><strong>Print</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1538-126"><strong>DblClick</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-126"><strong>DblClick</strong></span></span></p></td>
<td><p><span data-ttu-id="c1538-127"><strong>KeyPress</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-127"><strong>KeyPress</strong></span></span></p></td>
<td><p><span data-ttu-id="c1538-128"><strong>Unload</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-128"><strong>Unload</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1538-129"><strong>Delete</strong></span><span class="sxs-lookup"><span data-stu-id="c1538-129"><strong>Delete</strong></span></span></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c1538-130">**MouseDown**イベントと**イベントのキャンセル**操作を使用するにはオブジェクトを右クリックしたときに発生するイベントをキャンセルするだけです。</span><span class="sxs-lookup"><span data-stu-id="c1538-130">You can use the **CancelEvent** action with the **MouseDown** event only to cancel the event that occurs when you right-click an object.</span></span>

<span data-ttu-id="c1538-131">コントロールの**OnDblClick**イベント プロパティの設定は、**イベントのキャンセル**操作を含むマクロを指定する場合、アクションは、 **DblClick**イベントをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="c1538-131">If a control's **OnDblClick** event property setting specifies a macro containing the **CancelEvent** action, the action cancels the **DblClick** event.</span></span>

<span data-ttu-id="c1538-p103">取り消し可能なイベントでは、イベントのマクロが実行された後に、イベントの既定の動作 (イベント発生時の通常の動作) が実行されます。したがって、既定の動作を取り消すことができます。たとえば、テキスト ボックスでカーソル位置にある単語をダブルクリックすると、通常は、その単語が選択されます。 **DblClick** イベントのマクロで、この既定の動作を取り消し、テキスト ボックスのデータに関する情報を表示するフォームを開くなどの別のアクションを実行することができます。取り消し不可能なイベントでは、イベントのマクロが実行される前に、既定の動作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="c1538-p103">For events that can be canceled, the default behavior for the event (that is, what Access typically does when the event occurs) occurs after the macro for the event runs. This enables you to cancel the default behavior. For example, when you double-click a word that the insertion point is on in a text box, Access normally selects the word. You can cancel this default behavior in the macro for the **DblClick** event and perform some other action, such as opening a form containing information about the data in the text box. For events that can't be canceled, the default behavior occurs before the macro runs.</span></span>

> [!NOTE]
> <span data-ttu-id="c1538-137">フォームの**OnUnload**イベント プロパティは、**イベントのキャンセル**操作を実行するマクロを指定する場合、フォームを閉じることはできません。</span><span class="sxs-lookup"><span data-stu-id="c1538-137">If a form's **OnUnload** event property specifies a macro that carries out a **CancelEvent** action, you won't be able to close the form.</span></span> <span data-ttu-id="c1538-138">**イベントのキャンセル**操作を実行するか、マクロを開くし、**イベントのキャンセル**操作を削除する原因となった条件を修正する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="c1538-138">You must either correct the condition that caused the **CancelEvent** action to be carried out or open the macro and delete the **CancelEvent** action.</span></span> <span data-ttu-id="c1538-139">フォームがモーダル フォームの場合は、マクロを開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="c1538-139">If the form is a modal form, you won't be able to open the macro.</span></span>

<span data-ttu-id="c1538-140">アクションを実行するには、**イベントのキャンセル**Visual Basic for Applications (VBA) のモジュールで、 **DoCmd**オブジェクトの**CancelEvent**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="c1538-140">To carry out the **CancelEvent** action in a Visual Basic for Applications (VBA) module, use the **CancelEvent** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="c1538-141">使用例</span><span class="sxs-lookup"><span data-stu-id="c1538-141">Example</span></span>

<span data-ttu-id="c1538-142">マクロによるデータの入力検査</span><span class="sxs-lookup"><span data-stu-id="c1538-142">Validate data by using a macro</span></span>

<span data-ttu-id="c1538-143">次の入力検査マクロでは、"仕入先" フォームで入力された郵便番号を確認します。</span><span class="sxs-lookup"><span data-stu-id="c1538-143">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="c1538-144">このマクロでは、" **StopMacro/マクロの中止** "、" **MessageBox/メッセージボックス** "、" **CancelEvent/イベントのキャンセル** "、および " **GoToControl/コントロールの移動** " の各アクションの使い方を示します。</span><span class="sxs-lookup"><span data-stu-id="c1538-144">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="c1538-145">条件式では、フォームのレコードに入力された都道府県と郵便番号を確認します。</span><span class="sxs-lookup"><span data-stu-id="c1538-145">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="c1538-146">都道府県に対して郵便番号が正しく入力されていない場合、マクロはメッセージ ボックスを表示して、レコードの保存を取り消します。</span><span class="sxs-lookup"><span data-stu-id="c1538-146">If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="c1538-147">これは、し、郵便番号] コントロールに戻り、エラーを修正することができます。</span><span class="sxs-lookup"><span data-stu-id="c1538-147">It then returns you to the Postal Code control, where you can correct the error.</span></span> <span data-ttu-id="c1538-148">このマクロは "仕入先" フォームの " **BeforeUpdate/更新前処理** " プロパティに設定します。</span><span class="sxs-lookup"><span data-stu-id="c1538-148">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c1538-149">条件</span><span class="sxs-lookup"><span data-stu-id="c1538-149">Condition</span></span></p></th>
<th><p><span data-ttu-id="c1538-150">アクション</span><span class="sxs-lookup"><span data-stu-id="c1538-150">Action</span></span></p></th>
<th><p><span data-ttu-id="c1538-151">引数: 設定値</span><span class="sxs-lookup"><span data-stu-id="c1538-151">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="c1538-152">コメント</span><span class="sxs-lookup"><span data-stu-id="c1538-152">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c1538-153">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="c1538-153">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="c1538-154">StopMacro</span><span class="sxs-lookup"><span data-stu-id="c1538-154">StopMacro</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c1538-155">[都道府県] が<strong>Null</strong>の場合は、郵便番号を検証できません。</span><span class="sxs-lookup"><span data-stu-id="c1538-155">If CountryRegion is <strong>Null</strong>, postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1538-156">[都道府県](&quot;フランス&quot;、&quot;イタリア&quot;、&quot;スペイン&quot;) と Len ([郵便番号]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="c1538-156">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="c1538-157">MessageBox</span><span class="sxs-lookup"><span data-stu-id="c1538-157">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="c1538-p106">"Message/メッセージ": 郵便番号は 7 文字である必要があります。 "Beep/警告音": <strong>はい</strong> Type/メッセージの種類: <strong>情報</strong> Title/メッセージ タイトル: 郵便番号エラー  </span><span class="sxs-lookup"><span data-stu-id="c1538-p106">Message: The postal code must be 5 characters. Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="c1538-160">郵便番号が 7 文字でない場合にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="c1538-160">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1538-161">...</span><span class="sxs-lookup"><span data-stu-id="c1538-161"></span></span></p></td>
<td><p><span data-ttu-id="c1538-162">CancelEvent</span><span class="sxs-lookup"><span data-stu-id="c1538-162">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c1538-163">イベントを取り消します。</span><span class="sxs-lookup"><span data-stu-id="c1538-163">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="c1538-164">GoToControl</span><span class="sxs-lookup"><span data-stu-id="c1538-164">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="c1538-165">"Control Name/コントロール名": 郵便番号</span><span class="sxs-lookup"><span data-stu-id="c1538-165">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1538-166">[都道府県](&quot;オーストラリア&quot;、&quot;シンガポール&quot;) と Len ([郵便番号]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="c1538-166">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="c1538-167">MessageBox</span><span class="sxs-lookup"><span data-stu-id="c1538-167">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="c1538-p107">"Message/メッセージ": 郵便番号は 7 文字である必要があります。 "Beep/警告音": <strong>はい</strong> Type/メッセージの種類: <strong>情報</strong> Title/メッセージ タイトル: 郵便番号エラー  </span><span class="sxs-lookup"><span data-stu-id="c1538-p107">Message: The postal code must be 4 characters. Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="c1538-170">郵便番号が 7 文字でない場合にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="c1538-170">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1538-171">...</span><span class="sxs-lookup"><span data-stu-id="c1538-171"></span></span></p></td>
<td><p><span data-ttu-id="c1538-172">CancelEvent</span><span class="sxs-lookup"><span data-stu-id="c1538-172">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c1538-173">イベントを取り消します。</span><span class="sxs-lookup"><span data-stu-id="c1538-173">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="c1538-174">GoToControl</span><span class="sxs-lookup"><span data-stu-id="c1538-174">GoToControl</span></span></p></td>
<td><p><span data-ttu-id="c1538-175">"Control Name/コントロール名": 郵便番号</span><span class="sxs-lookup"><span data-stu-id="c1538-175">Control Name: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c1538-176">([都道府県] =&quot;カナダ&quot;)([郵便番号] が気に入らない&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="c1538-176">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="c1538-177">MessageBox</span><span class="sxs-lookup"><span data-stu-id="c1538-177">MessageBox</span></span></p></td>
<td><p><span data-ttu-id="c1538-p108">"Message/メッセージ": 郵便番号が無効です。たとえば、広島県の郵便番号の上 3 桁は 720 ～ 739 です。 Beep/警告音: <strong>はい</strong> Type/メッセージの種類: <strong>情報</strong> Title/メッセージ タイトル: 郵便番号エラー  </span><span class="sxs-lookup"><span data-stu-id="c1538-p108">Message: The postal code is not valid. Example of Canadian code: H1J 1C3 Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="c1538-p109">[都道府県] が広島県で、郵便番号の上 3 桁が 720 ～ 739 でない場合にメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="c1538-p109">If the postal code isn't correct for Canada, display a message. (Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c1538-182">...</span><span class="sxs-lookup"><span data-stu-id="c1538-182"></span></span></p></td>
<td><p><span data-ttu-id="c1538-183">CancelEvent</span><span class="sxs-lookup"><span data-stu-id="c1538-183">CancelEvent</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c1538-184">イベントを取り消します。</span><span class="sxs-lookup"><span data-stu-id="c1538-184">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

