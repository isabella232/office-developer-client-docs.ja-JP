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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e43a1d7c57668ba930b4c4af7194bd298971e6ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432381"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="6742c-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="6742c-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="6742c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6742c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6742c-105">プロファイル ウィザードによって呼び出されるコールバック関数を定義し、プロバイダーのプロパティ シートまたはページが表示されているときにサービス プロバイダーがユーザー イベントに対応できます。</span><span class="sxs-lookup"><span data-stu-id="6742c-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6742c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6742c-106">Header file:</span></span>  <br/> |<span data-ttu-id="6742c-107">Mapiwz.h</span><span class="sxs-lookup"><span data-stu-id="6742c-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="6742c-108">定義された関数は、次の方法で実装されます。</span><span class="sxs-lookup"><span data-stu-id="6742c-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="6742c-109">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="6742c-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="6742c-110">によって呼び出される定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="6742c-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="6742c-111">MAPI プロファイル ウィザード</span><span class="sxs-lookup"><span data-stu-id="6742c-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="6742c-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6742c-112">Parameters</span></span>

<span data-ttu-id="6742c-113">_hDlg_</span><span class="sxs-lookup"><span data-stu-id="6742c-113">_hDlg_</span></span>
  
> <span data-ttu-id="6742c-114">[in][プロファイル ウィザード] ダイアログ ボックスのウィンドウ ハンドル。</span><span class="sxs-lookup"><span data-stu-id="6742c-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="6742c-115">_wMsgID_</span><span class="sxs-lookup"><span data-stu-id="6742c-115">_wMsgID_</span></span>
  
> <span data-ttu-id="6742c-116">[in]処理するウィンドウ メッセージ。</span><span class="sxs-lookup"><span data-stu-id="6742c-116">[in] The window message to be processed.</span></span> <span data-ttu-id="6742c-117">モーダル ダイアログ ボックスで予期される通常のウィンドウ メッセージに加えて、次のメッセージを受信できます。</span><span class="sxs-lookup"><span data-stu-id="6742c-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="6742c-118">WM_CLOSE</span><span class="sxs-lookup"><span data-stu-id="6742c-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="6742c-119">プロファイル ウィザードが完了しました。</span><span class="sxs-lookup"><span data-stu-id="6742c-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="6742c-120">サービス プロバイダーは、動的に割り当てられたメモリの割り当ての解放など、必要なすべてのクリーンアップを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6742c-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="6742c-121">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="6742c-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="6742c-122">プロバイダーのコントロールの 1 つが選択されている、または[次へ] または [戻 **る]** ボタンがクリックされています。</span><span class="sxs-lookup"><span data-stu-id="6742c-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="6742c-123">_wParam パラメーターの値_ は、これらのユーザー イベントが発生したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6742c-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="6742c-124">WM_INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="6742c-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="6742c-125">ユーザーが別のプロパティ ページに移動し、ダイアログ ボックスを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6742c-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="6742c-126">プロバイダーは、プロファイル ウィザードがダイアログ ボックスに追加したコントロールを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6742c-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="6742c-127">WIZ_QUERYNUMPAGES</span><span class="sxs-lookup"><span data-stu-id="6742c-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="6742c-128">プロファイル ウィザードでは、プロバイダーが表示する必要があるページ数を求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6742c-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="6742c-129">プロバイダーは、TRUE または FALSE の代わりにページ数を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6742c-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="6742c-130">たとえば、次の return ステートメントを使用して、3 つのページを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6742c-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="6742c-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="6742c-131">_wParam_</span></span>
  
> <span data-ttu-id="6742c-132">[in]ウィンドウ メッセージに関連付けられた 32 ビット のパラメーター。</span><span class="sxs-lookup"><span data-stu-id="6742c-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="6742c-133">指定できる値は  _、wMsgID パラメーターで指定されたメッセージによって異_ なっています。</span><span class="sxs-lookup"><span data-stu-id="6742c-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="6742c-134">モーダル ダイアログ ボックスの通常のウィンドウ メッセージで予期される値に加えて、次の値を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="6742c-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="6742c-135">WIZ_NEXT</span><span class="sxs-lookup"><span data-stu-id="6742c-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="6742c-136">_wMsgID に_ WM_COMMAND、ユーザーは [次へ] ボタン **をクリック** します。</span><span class="sxs-lookup"><span data-stu-id="6742c-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="6742c-137">WIZ_PREV</span><span class="sxs-lookup"><span data-stu-id="6742c-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="6742c-138">_wMsgID に_ ファイルがWM_COMMAND、ユーザーは [戻る] ボタンを **クリック** します。</span><span class="sxs-lookup"><span data-stu-id="6742c-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="6742c-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="6742c-139">_lParam_</span></span>
  
> <span data-ttu-id="6742c-140">[in]ウィンドウ メッセージに関連付けられた 32 ビット のパラメーター。</span><span class="sxs-lookup"><span data-stu-id="6742c-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="6742c-141">指定できる値は  _、wMsgID パラメーターで指定されたメッセージによって異_ なっています。</span><span class="sxs-lookup"><span data-stu-id="6742c-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6742c-142">戻り値</span><span class="sxs-lookup"><span data-stu-id="6742c-142">Return value</span></span>

<span data-ttu-id="6742c-143">**SERVICEWIZARDDLGPROC ベースの関数** によって返される値は、受信したウィンドウ メッセージに依存します。</span><span class="sxs-lookup"><span data-stu-id="6742c-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="6742c-144">特に、メッセージの例外の戻り値WIZ_QUERYNUMPAGESしてください。</span><span class="sxs-lookup"><span data-stu-id="6742c-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="6742c-145">通常の戻り値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6742c-145">The normal return values are:</span></span> 
  
<span data-ttu-id="6742c-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="6742c-146">TRUE</span></span> 
  
> <span data-ttu-id="6742c-147">サービス プロバイダーが受信ウィンドウ メッセージを処理しました。</span><span class="sxs-lookup"><span data-stu-id="6742c-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="6742c-148">FALSE</span><span class="sxs-lookup"><span data-stu-id="6742c-148">FALSE</span></span> 
  
> <span data-ttu-id="6742c-149">サービス プロバイダーは、受信したウィンドウ メッセージを処理していない。</span><span class="sxs-lookup"><span data-stu-id="6742c-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6742c-150">注釈</span><span class="sxs-lookup"><span data-stu-id="6742c-150">Remarks</span></span>

<span data-ttu-id="6742c-151">ユーザーがプロパティ ページ間を移動すると、プロバイダーは古いページのコントロールを非表示にし、次のページまたは前のページのコントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="6742c-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="6742c-152">ユーザーが [次へ] ボタンをクリックすると **、SERVICEWIZARDDLGPROC** ベースの関数が _wParam_ パラメーターの WM_COMMAND メッセージと WIZ_NEXTで呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6742c-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="6742c-153">次の手順では、ユーザーが [次へ] をクリックした時刻と、最初のプロバイダーの構成ページが表示される時間の間に発生する処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="6742c-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="6742c-154">プロファイル ウィザードは、ウィンドウ上にあるコントロールを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="6742c-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="6742c-155">プロファイル ウィザードは、プロバイダーの非表示のコントロールをページに追加します。</span><span class="sxs-lookup"><span data-stu-id="6742c-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="6742c-156">プロファイル ウィザードは **SERVICEWIZARDDLGPROC** を呼び出し、プロバイダーがコントロールを初期化WM_INITDIALOGメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="6742c-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="6742c-157">プロファイル ウィザードは **SERVICEWIZARDDLGPROC** を呼び出し、メッセージをWIZ_QUERYNUMPAGESします。</span><span class="sxs-lookup"><span data-stu-id="6742c-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="6742c-158">プロバイダーは、表示するページ数を返します。</span><span class="sxs-lookup"><span data-stu-id="6742c-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="6742c-159">プロファイル ウィザードは **SERVICEWIZARDDLGPROC** を呼び出し  _、wParam_ パラメーターが WIZ_NEXT または WIZ_PREV に設定された WM_COMMAND メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="6742c-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="6742c-160">この時点で、プロバイダーは FALSE {error} を返すか、コントロールを表示し、TRUE {success} を返します。</span><span class="sxs-lookup"><span data-stu-id="6742c-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="6742c-161">プロファイル ウィザードがページにID_NEXT、プロバイダーの最初のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6742c-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="6742c-162">このID_PREV場合は、最後のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6742c-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="6742c-163">プロファイル ウィザードはプロバイダーの **SERVICEWIZARDDLGPROC** 関数を呼び出し  _、wParam_ パラメーターが WIZ_NEXT または WIZ_PREV に設定された WM_COMMAND メッセージを送信します (ユーザーがクリックしたボタンに応じて異なります)。</span><span class="sxs-lookup"><span data-stu-id="6742c-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="6742c-164">プロバイダーは、コントロールを表示または非表示にし、プロファイル ウィザードに渡された **IMAPIProp** にデータを書き込み、一連のページをステップ実行します。</span><span class="sxs-lookup"><span data-stu-id="6742c-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="6742c-165">プロバイダーは、次または前のページが正常に表示された場合は TRUE、次のページも前のページも表示しない場合は FALSE を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6742c-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="6742c-166">プロバイダーは、一連のページの外に出る際に注意し、コントロールを非表示にし、そのデータをプロファイルに書き込んで適切に対応する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6742c-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="6742c-167">ユーザーがプロバイダーのページ範囲の外側に移動すると、プロファイル ウィザードは、ダイアログ ボックスからプロバイダーの非表示のコントロールを削除し、次のプロバイダーを呼び出したり、最後のプロバイダーである場合は次のページを表示します。</span><span class="sxs-lookup"><span data-stu-id="6742c-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

