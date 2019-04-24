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
ms.openlocfilehash: e43a1d7c57668ba930b4c4af7194bd298971e6ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356414"
---
# <a name="servicewizarddlgproc"></a><span data-ttu-id="a3e01-103">SERVICEWIZARDDLGPROC</span><span class="sxs-lookup"><span data-stu-id="a3e01-103">SERVICEWIZARDDLGPROC</span></span>
 
<span data-ttu-id="a3e01-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3e01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3e01-105">プロバイダーのプロパティシートまたはページが表示されているときに、サービスプロバイダーがユーザーイベントに反応できるようにするために、プロファイルウィザードによって呼び出されるコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="a3e01-105">Defines a callback function invoked by the Profile Wizard to allow a service provider to react to user events when the provider's property sheets or pages are being shown.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3e01-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a3e01-106">Header file:</span></span>  <br/> |<span data-ttu-id="a3e01-107">Mapiwz</span><span class="sxs-lookup"><span data-stu-id="a3e01-107">Mapiwz.h</span></span>  <br/> |
|<span data-ttu-id="a3e01-108">定義された関数の実装:</span><span class="sxs-lookup"><span data-stu-id="a3e01-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="a3e01-109">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a3e01-109">Service providers</span></span>  <br/> |
|<span data-ttu-id="a3e01-110">によって呼び出された定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="a3e01-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="a3e01-111">MAPI プロファイルウィザード</span><span class="sxs-lookup"><span data-stu-id="a3e01-111">MAPI Profile Wizard</span></span>  <br/> |
   
```cpp
BOOL SERVICEWIZARDDLGPROC(
  HWND hDlg,
  UINT wMsgID,
  WPARAM wParam,
  LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="a3e01-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a3e01-112">Parameters</span></span>

<span data-ttu-id="a3e01-113">_hdlg_</span><span class="sxs-lookup"><span data-stu-id="a3e01-113">_hDlg_</span></span>
  
> <span data-ttu-id="a3e01-114">順番[プロファイルウィザード] ダイアログボックスへのウィンドウハンドル。</span><span class="sxs-lookup"><span data-stu-id="a3e01-114">[in] Window handle to the Profile Wizard dialog box.</span></span> 
    
<span data-ttu-id="a3e01-115">_wMsgID_</span><span class="sxs-lookup"><span data-stu-id="a3e01-115">_wMsgID_</span></span>
  
> <span data-ttu-id="a3e01-116">順番処理するウィンドウメッセージを指定します。</span><span class="sxs-lookup"><span data-stu-id="a3e01-116">[in] The window message to be processed.</span></span> <span data-ttu-id="a3e01-117">モーダルダイアログボックスで想定される通常のウィンドウメッセージに加えて、次のメッセージを受信できます。</span><span class="sxs-lookup"><span data-stu-id="a3e01-117">In addition to the regular window messages expected by a modal dialog box, the following messages can be received:</span></span>
    
<span data-ttu-id="a3e01-118">WM_CLOSE</span><span class="sxs-lookup"><span data-stu-id="a3e01-118">WM_CLOSE</span></span> 
  
> <span data-ttu-id="a3e01-119">プロファイルウィザードが完了しました。</span><span class="sxs-lookup"><span data-stu-id="a3e01-119">The Profile Wizard has completed.</span></span> <span data-ttu-id="a3e01-120">サービスプロバイダーは、動的に割り当てられたメモリを解放するなど、必要なすべてのクリーンアップを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3e01-120">The service provider should do all required cleanup such as deallocating any dynamically allocated memory.</span></span> 
    
<span data-ttu-id="a3e01-121">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="a3e01-121">WM_COMMAND</span></span> 
  
> <span data-ttu-id="a3e01-122">プロバイダーのコントロールのいずれかが選択されているか、 **[次へ**] または [**戻る**] ボタンがクリックされました。</span><span class="sxs-lookup"><span data-stu-id="a3e01-122">One of the provider's controls has been selected, or the **Next** or **Back** button has been clicked.</span></span> <span data-ttu-id="a3e01-123">_wParam_パラメーターの値は、これらのユーザーイベントが発生したことを示します。</span><span class="sxs-lookup"><span data-stu-id="a3e01-123">The value in the  _wParam_ parameter indicates which of these user events has occurred.</span></span> 
    
<span data-ttu-id="a3e01-124">WM_INITDIALOG</span><span class="sxs-lookup"><span data-stu-id="a3e01-124">WM_INITDIALOG</span></span> 
  
> <span data-ttu-id="a3e01-125">ユーザーは、ダイアログボックスを初期化する必要がある別のプロパティページに移動しました。</span><span class="sxs-lookup"><span data-stu-id="a3e01-125">The user has moved to another property page, for which the dialog box must be initialized.</span></span> <span data-ttu-id="a3e01-126">プロバイダーは、プロファイルウィザードによってダイアログボックスに追加されたコントロールを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3e01-126">The provider should initialize the controls that the Profile Wizard has added to the dialog box.</span></span> 
    
<span data-ttu-id="a3e01-127">WIZ_QUERYNUMPAGES</span><span class="sxs-lookup"><span data-stu-id="a3e01-127">WIZ_QUERYNUMPAGES</span></span> 
  
> <span data-ttu-id="a3e01-128">プロファイルウィザードは、プロバイダーが表示する必要があるページ数の入力を求めます。</span><span class="sxs-lookup"><span data-stu-id="a3e01-128">The Profile Wizard is prompting for the number of pages that the provider needs to display.</span></span> <span data-ttu-id="a3e01-129">プロバイダーは、TRUE または FALSE ではなく、ページの数を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3e01-129">The provider should return the number of pages instead of TRUE or FALSE.</span></span> <span data-ttu-id="a3e01-130">たとえば、次の return ステートメントを使用して、3つのページが表示されるように指定します。</span><span class="sxs-lookup"><span data-stu-id="a3e01-130">For example, use the following return statement to indicate that three pages should to be displayed:</span></span>
    
   ```cpp
return (BOOL)3;

   ```

<span data-ttu-id="a3e01-131">_wParam_</span><span class="sxs-lookup"><span data-stu-id="a3e01-131">_wParam_</span></span>
  
> <span data-ttu-id="a3e01-132">順番ウィンドウメッセージに関連付けられている32ビットパラメーター。</span><span class="sxs-lookup"><span data-stu-id="a3e01-132">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="a3e01-133">使用可能な値は、 _wMsgID_パラメーターで指定されたメッセージによって異なります。</span><span class="sxs-lookup"><span data-stu-id="a3e01-133">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> <span data-ttu-id="a3e01-134">モーダルダイアログボックスの通常のウィンドウメッセージに必要な値に加えて、次の値を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="a3e01-134">In addition to the values expected with the regular window messages for a modal dialog box, the following values can be received:</span></span> 
    
<span data-ttu-id="a3e01-135">WIZ_NEXT</span><span class="sxs-lookup"><span data-stu-id="a3e01-135">WIZ_NEXT</span></span> 
  
> <span data-ttu-id="a3e01-136">_wMsgID_に WM_COMMAND が含まれている場合、ユーザーは **[次へ**] ボタンをクリックしています。</span><span class="sxs-lookup"><span data-stu-id="a3e01-136">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Next** button.</span></span> 
    
<span data-ttu-id="a3e01-137">WIZ_PREV</span><span class="sxs-lookup"><span data-stu-id="a3e01-137">WIZ_PREV</span></span> 
  
> <span data-ttu-id="a3e01-138">_wMsgID_に WM_COMMAND が含まれている場合、ユーザーは [**戻る**] ボタンをクリックしています。</span><span class="sxs-lookup"><span data-stu-id="a3e01-138">When  _wMsgID_ contains WM_COMMAND, the user has clicked the **Back** button.</span></span> 
    
<span data-ttu-id="a3e01-139">_lParam_</span><span class="sxs-lookup"><span data-stu-id="a3e01-139">_lParam_</span></span>
  
> <span data-ttu-id="a3e01-140">順番ウィンドウメッセージに関連付けられている32ビットパラメーター。</span><span class="sxs-lookup"><span data-stu-id="a3e01-140">[in] A 32-bit parameter associated with window messages.</span></span> <span data-ttu-id="a3e01-141">使用可能な値は、 _wMsgID_パラメーターで指定されたメッセージによって異なります。</span><span class="sxs-lookup"><span data-stu-id="a3e01-141">Possible values depend on the message specified in the  _wMsgID_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a3e01-142">戻り値</span><span class="sxs-lookup"><span data-stu-id="a3e01-142">Return value</span></span>

<span data-ttu-id="a3e01-143">**servicewizarddlgproc**に基づく関数によって返される値は、受信したウィンドウメッセージによって異なります。</span><span class="sxs-lookup"><span data-stu-id="a3e01-143">The value returned by a **SERVICEWIZARDDLGPROC** based function is dependent on the window message received.</span></span> <span data-ttu-id="a3e01-144">特に、WIZ_QUERYNUMPAGES メッセージの例外的な戻り値に注意してください。</span><span class="sxs-lookup"><span data-stu-id="a3e01-144">Note in particular the exceptional return value for the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="a3e01-145">通常の戻り値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a3e01-145">The normal return values are:</span></span> 
  
<span data-ttu-id="a3e01-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="a3e01-146">TRUE</span></span> 
  
> <span data-ttu-id="a3e01-147">サービスプロバイダーが受信したウィンドウメッセージを処理しました。</span><span class="sxs-lookup"><span data-stu-id="a3e01-147">The service provider has processed the received window message.</span></span> 
    
<span data-ttu-id="a3e01-148">FALSE</span><span class="sxs-lookup"><span data-stu-id="a3e01-148">FALSE</span></span> 
  
> <span data-ttu-id="a3e01-149">サービスプロバイダーが受信したウィンドウメッセージを処理していません。</span><span class="sxs-lookup"><span data-stu-id="a3e01-149">The service provider has not processed the received window message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3e01-150">解説</span><span class="sxs-lookup"><span data-stu-id="a3e01-150">Remarks</span></span>

<span data-ttu-id="a3e01-151">ユーザーがあるプロパティページから別のページに移動すると、プロバイダーは古いページのコントロールを非表示にし、次または前のページのコントロールを表示します。</span><span class="sxs-lookup"><span data-stu-id="a3e01-151">When the user moves from one property page to another, the provider is responsible for hiding the old page's controls and showing the controls for the next or previous page.</span></span> <span data-ttu-id="a3e01-152">ユーザーが **[次へ**] ボタンをクリックすると、WIZ_NEXT パラメーターで、WM_COMMAND メッセージとを使用して__ **servicewizarddlgproc**ベースの関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a3e01-152">When the user clicks the **Next** button, the **SERVICEWIZARDDLGPROC** based function is called with the WM_COMMAND message and WIZ_NEXT in the  _wParam_ parameter.</span></span> <span data-ttu-id="a3e01-153">次の手順では、ユーザーが **[次へ**] をクリックしてから最初のプロバイダーの構成ページが表示されるまでの時間について説明します。</span><span class="sxs-lookup"><span data-stu-id="a3e01-153">The following steps describe what occurs between the time the user clicks **Next** and the time the first provider's configuration pages are rendered.</span></span> 
  
1. <span data-ttu-id="a3e01-154">プロファイルウィザードは、ウィンドウにあるコントロールを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="a3e01-154">The Profile Wizard hides any controls that are on the window.</span></span> 
    
2. <span data-ttu-id="a3e01-155">プロファイルウィザードによって、プロバイダーの隠しコントロールがページに追加されます。</span><span class="sxs-lookup"><span data-stu-id="a3e01-155">The Profile Wizard adds the provider's hidden controls to the page.</span></span> 
    
3. <span data-ttu-id="a3e01-156">プロファイルウィザードは、WM_INITDIALOG メッセージを送信して**servicewizarddlgproc**を呼び出して、プロバイダーがコントロールを初期化できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a3e01-156">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_INITDIALOG message, so that the provider can initialize the controls.</span></span> 
    
4. <span data-ttu-id="a3e01-157">プロファイルウィザードは、 **servicewizarddlgproc**を呼び出して、WIZ_QUERYNUMPAGES メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="a3e01-157">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WIZ_QUERYNUMPAGES message.</span></span> <span data-ttu-id="a3e01-158">プロバイダーは、表示されるページ数を返します。</span><span class="sxs-lookup"><span data-stu-id="a3e01-158">The provider returns the number of pages that are to be shown.</span></span> 
    
5. <span data-ttu-id="a3e01-159">プロファイルウィザードは、 **servicewizarddlgproc**を呼び出し、 _wParam_パラメーターが WIZ_NEXT または WIZ_PREV のいずれかに設定された WM_COMMAND メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="a3e01-159">The Profile Wizard calls **SERVICEWIZARDDLGPROC**, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV.</span></span> <span data-ttu-id="a3e01-160">この時点で、プロバイダーは FALSE {error} を返すか、またはそのコントロールを調べ、TRUE {success} を返します。</span><span class="sxs-lookup"><span data-stu-id="a3e01-160">At this point, the provider either returns FALSE {error} or reveals its controls and returns TRUE {success}.</span></span> <span data-ttu-id="a3e01-161">プロファイルウィザードが ID_NEXT に合格すると、プロバイダーの最初のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3e01-161">If the Profile Wizard passes in ID_NEXT, the provider's first page is displayed.</span></span> <span data-ttu-id="a3e01-162">ID_PREV が渡された場合は、最後のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3e01-162">If ID_PREV is passed in, the last page is displayed.</span></span> 
    
6. <span data-ttu-id="a3e01-163">プロファイルウィザードは、プロバイダーの**servicewizarddlgproc**関数を呼び出し、 _wParam_パラメーターが WIZ_NEXT または WIZ_PREV (ユーザーがクリックしたボタンに応じて) に設定された WM_COMMAND メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="a3e01-163">The Profile Wizard calls the provider's **SERVICEWIZARDDLGPROC** function, sending the WM_COMMAND message with the  _wParam_ parameter set to either WIZ_NEXT or WIZ_PREV (depending on which button the user clicked).</span></span> <span data-ttu-id="a3e01-164">プロバイダーは、そのコントロールを表示または非表示にし、そのデータをプロファイルウィザードに渡された**imapiprop**に書き込んでページの順序をステップ実行します。</span><span class="sxs-lookup"><span data-stu-id="a3e01-164">The provider is responsible for showing or hiding its controls and writing its data to the **IMAPIProp** passed to the Profile Wizard to step through its sequence of pages.</span></span> <span data-ttu-id="a3e01-165">プロバイダーは、次のページまたは前のページが正常に表示された場合は TRUE を返し、次のページまたは前のページが表示されない場合は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="a3e01-165">The provider should return TRUE if the next or previous page was successfully shown, and FALSE if neither the next nor previous page could be shown.</span></span> <span data-ttu-id="a3e01-166">プロバイダーは、ページのシーケンス外でのステップ実行時に認識し、コントロールを非表示にして、プロファイルにデータを書き込むことによって適切に応答する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3e01-166">The provider needs to be aware of when it is stepping outside of its sequence of pages, and respond appropriately by hiding its controls and writing its data to the profile.</span></span> 
    
7. <span data-ttu-id="a3e01-167">ユーザーがプロバイダーのページ範囲外で手順を実行すると、プロファイルウィザードはプロバイダーの非表示のコントロールをダイアログボックスから削除し、次のプロバイダーがある場合は次のページを表示します。</span><span class="sxs-lookup"><span data-stu-id="a3e01-167">If the user steps outside the provider's range of pages, the Profile Wizard deletes the provider's hidden controls from the dialog box and calls the next provider or displays its next page if that was the last provider.</span></span> 
    

