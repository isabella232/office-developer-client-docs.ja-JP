---
title: SERVICEWIZARDDLGPROC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SERVICEWIZARDDLGPROC
api_type:
- COM
ms.assetid: 3e2d5190-e67a-470d-8177-0f0ba20c7b82
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fdd5d01b96c9ea756ee64f113ccb5119a9693668
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594468"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="a1c41-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="a1c41-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="a1c41-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1c41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1c41-105">プロバイダーのプロパティ シートまたはページが表示されているときに、ユーザー イベントに応答するサービス プロバイダーを使用してプロファイル ウィザードによって呼び出されるコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1c41-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a1c41-106">Header file:</span></span>  <br/> |<span data-ttu-id="a1c41-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="a1c41-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="a1c41-108">によって実装される関数の定義:</span><span class="sxs-lookup"><span data-stu-id="a1c41-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="a1c41-109">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a1c41-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="a1c41-110">によって呼び出される関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="a1c41-111">MAPI プロファイル ウィザード</span><span class="sxs-lookup"><span data-stu-id="a1c41-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="a1c41-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a1c41-112">Parameters</span></span>

<span data-ttu-id="a1c41-113">_hDlg_</span><span class="sxs-lookup"><span data-stu-id="a1c41-113">_hDlg_</span></span>
  
> <span data-ttu-id="a1c41-114">[in]プロファイル ウィザード] ダイアログ ボックスのウィンドウ ハンドルです。</span><span class="sxs-lookup"><span data-stu-id="a1c41-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="a1c41-115">_wMsgID_</span><span class="sxs-lookup"><span data-stu-id="a1c41-115">_wMsgID_</span></span>
  
> <span data-ttu-id="a1c41-116">[in]ウィンドウ メッセージを処理します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-116">[in] The window message to be processed.</span></span> <span data-ttu-id="a1c41-117">モーダル ダイアログ ボックスで、通常のウィンドウ メッセージの他、次のメッセージを受信できます。</span><span class="sxs-lookup"><span data-stu-id="a1c41-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="a1c41-118">WM_CLOSE</span><span class="sxs-lookup"><span data-stu-id="a1c41-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="a1c41-119">プロファイル ウィザードが完了しました。</span><span class="sxs-lookup"><span data-stu-id="a1c41-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="a1c41-120">サービス プロバイダーは、割り当てられたメモリのいずれかを動的に割り当て解除など、すべての必要なクリーンアップを行います。</span><span class="sxs-lookup"><span data-stu-id="a1c41-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="a1c41-121">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="a1c41-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="a1c41-122">プロバイダーのコントロールのいずれかが選択されているか、[**次へ**] または [**戻る**] ボタンがクリックしてされました。</span><span class="sxs-lookup"><span data-stu-id="a1c41-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="a1c41-123">_WParam_パラメーターの値は、これらのユーザー イベントが発生したを示します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="a1c41-124">WM_INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="a1c41-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="a1c41-125">ユーザーは、ダイアログ ボックスを初期化する必要があります別のプロパティ ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="a1c41-126">プロバイダーは、プロファイル ウィザード、ダイアログ ボックスに追加したコントロールを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1c41-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="a1c41-127">WIZ_QUERYNUMPAGES</span><span class="sxs-lookup"><span data-stu-id="a1c41-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="a1c41-128">プロファイル ウィザードはページを表示する必要のあるプロバイダーの数のメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="a1c41-129">プロバイダーには、TRUE または FALSE の代わりにページ数を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1c41-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="a1c41-130">たとえば、3 つのページを表示する必要があることを示すために次の return ステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="a1c41-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="a1c41-131">_wParam_</span></span>
  
> <span data-ttu-id="a1c41-132">[in]ウィンドウのメッセージに関連付けられている 32 ビットのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="a1c41-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="a1c41-133">使用可能な値は、 _wMsgID_パラメーターで指定されたメッセージに依存します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="a1c41-134">値に加え、モーダル ダイアログ ボックスの通常のウィンドウ メッセージが期待どおり、次の値を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="a1c41-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="a1c41-135">WIZ_NEXT</span><span class="sxs-lookup"><span data-stu-id="a1c41-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="a1c41-136">_WMsgID_に WM_COMMAND が含まれている場合、[**次へ**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a1c41-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="a1c41-137">WIZ_PREV</span><span class="sxs-lookup"><span data-stu-id="a1c41-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="a1c41-138">_WMsgID_に WM_COMMAND が含まれている場合、[**戻る**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a1c41-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="a1c41-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="a1c41-139">_lParam_</span></span>
  
> <span data-ttu-id="a1c41-140">[in]ウィンドウのメッセージに関連付けられている 32 ビットのパラメーター。</span><span class="sxs-lookup"><span data-stu-id="a1c41-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="a1c41-141">使用可能な値は、 _wMsgID_パラメーターで指定されたメッセージに依存します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a1c41-142">戻り値</span><span class="sxs-lookup"><span data-stu-id="a1c41-142">Return value</span></span>

<span data-ttu-id="a1c41-143">**SERVICEWIZARDDLGPROC**ベースの関数によって返される値は、ウィンドウ メッセージを受信しました。</span><span class="sxs-lookup"><span data-stu-id="a1c41-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="a1c41-144">比類のない WIZ_QUERYNUMPAGES メッセージの値を返すに特に注意してください。</span><span class="sxs-lookup"><span data-stu-id="a1c41-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="a1c41-145">通常の戻り値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a1c41-145">The normal return values are:</span></span> 
  
<span data-ttu-id="a1c41-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="a1c41-146">TRUE</span></span> 
  
> <span data-ttu-id="a1c41-147">サービス プロバイダーが、受信ウィンドウ メッセージを処理します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="a1c41-148">FALSE</span><span class="sxs-lookup"><span data-stu-id="a1c41-148">FALSE</span></span> 
  
> <span data-ttu-id="a1c41-149">サービス プロバイダーは、受信されたウィンドウ メッセージを処理していません。</span><span class="sxs-lookup"><span data-stu-id="a1c41-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a1c41-150">注釈</span><span class="sxs-lookup"><span data-stu-id="a1c41-150">Remarks</span></span>

<span data-ttu-id="a1c41-151">ユーザーを移動する 1 つのプロパティ ページから、ときに、プロバイダーは、次または前のページのコントロールの表示と古いページのコントロールを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="a1c41-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="a1c41-152">ユーザーは、[**次へ**] をクリックすると、 **SERVICEWIZARDDLGPROC**ベースの機能、 _wParam_パラメーターに WM_COMMAND メッセージと WIZ_NEXT で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a1c41-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="a1c41-153">次の手順では、最初のプロバイダーの構成ページが表示される時間と、ユーザーは**次**をクリックすると時間の間で行われる処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="a1c41-154">プロファイル ウィザードでは、ウィンドウ上にあるすべてのコントロールを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="a1c41-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="a1c41-155">プロファイル ウィザードでは、プロバイダーの非表示のコントロールをページに追加します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="a1c41-156">プロファイル ウィザードでは、 **SERVICEWIZARDDLGPROC**プロバイダーは、コントロールを初期化できるように、WM_INITDIALOG メッセージの送信を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="a1c41-157">プロファイル ウィザードでは、 **SERVICEWIZARDDLGPROC**、WIZ_QUERYNUMPAGES メッセージを送信を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="a1c41-158">プロバイダーは、表示されるページの数を返します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="a1c41-159">プロファイル ウィザードでは、 **SERVICEWIZARDDLGPROC**、WIZ_NEXT または WIZ_PREV のいずれかに設定、 _wParam_パラメーターを持つ WM_COMMAND メッセージを送信を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="a1c41-160">この時点では、プロバイダーか、{エラー} の FALSE を返しますまたはそのコントロールが表示し、{成功} は TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="a1c41-161">プロファイル ウィザードは、ID_NEXT に合格した場合は、プロバイダーの最初のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a1c41-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="a1c41-162">ID_PREV が渡されると、最後のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a1c41-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="a1c41-163">プロファイル ウィザードでは、WIZ_NEXT または (ボタンによって、ユーザーがクリックした) WIZ_PREV のいずれかに設定、 _wParam_パラメーターを持つ WM_COMMAND メッセージを送信するプロバイダーの**SERVICEWIZARDDLGPROC**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a1c41-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="a1c41-164">プロバイダーは、そのコントロールを非表示のページのシーケンスをステップ実行するにはプロファイル ウィザードに渡される**IMAPIProp**にそのデータを記述します.</span><span class="sxs-lookup"><span data-stu-id="a1c41-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="a1c41-165">プロバイダーする必要があります TRUE を返す場合は、次または前のページが正常に表示すると、次または前のページもない場合に FALSE が表示される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a1c41-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="a1c41-166">プロバイダーは、その一連のページの外部でステップ実行するのに注意してくださいし、そのコントロールを非表示し、プロファイル データの書き込みが適切に応答する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1c41-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="a1c41-167">プロバイダーの範囲のページの手順は、ユーザー、プロファイル ウィザード] ダイアログ ボックスからプロバイダーの非表示のコントロールを削除し、次のプロバイダーを呼び出してか最後のプロバイダーをされている場合、次のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a1c41-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

