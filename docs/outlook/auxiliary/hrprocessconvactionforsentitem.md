---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: その PidTagConversationId のメール アイテムの送信の後の分類を実行します。
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389542"
---
# <a name="hrprocessconvactionforsentitem"></a><span data-ttu-id="07c05-103">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="07c05-103">HrProcessConvActionForSentItem</span></span>

<span data-ttu-id="07c05-104">その[PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx)のメール アイテムの送信の後の分類を実行します。</span><span class="sxs-lookup"><span data-stu-id="07c05-104">Performs post-send categorization on a mail item based on its [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="07c05-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="07c05-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07c05-106">によってエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="07c05-106">Exported by:</span></span>  <br/> |<span data-ttu-id="07c05-107">Outlook.exe</span><span class="sxs-lookup"><span data-stu-id="07c05-107">Outlook.exe</span></span>  <br/> |
|<span data-ttu-id="07c05-108">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="07c05-108">Called by:</span></span>  <br/> |<span data-ttu-id="07c05-109">クライアント</span><span class="sxs-lookup"><span data-stu-id="07c05-109">Client</span></span>  <br/> |
|<span data-ttu-id="07c05-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="07c05-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="07c05-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="07c05-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a><span data-ttu-id="07c05-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="07c05-112">Parameters</span></span>

<span data-ttu-id="07c05-113">_pmbinStoreEid_</span><span class="sxs-lookup"><span data-stu-id="07c05-113">_pmbinStoreEid_</span></span>
  
> <span data-ttu-id="07c05-114">[in]ストア、またはメール アイテムの[PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx)の[PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx)です。</span><span class="sxs-lookup"><span data-stu-id="07c05-114">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the store, or the [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="07c05-115">できませんが NULL または無効です。</span><span class="sxs-lookup"><span data-stu-id="07c05-115">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="07c05-116">_pmbinMsgEid_</span><span class="sxs-lookup"><span data-stu-id="07c05-116">_pmbinMsgEid_</span></span>
  
> <span data-ttu-id="07c05-117">[in]メール アイテムの[PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="07c05-117">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="07c05-118">できませんが NULL または無効です。</span><span class="sxs-lookup"><span data-stu-id="07c05-118">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="07c05-119">_pmbinConvID_</span><span class="sxs-lookup"><span data-stu-id="07c05-119">_pmbinConvID_</span></span>
  
> <span data-ttu-id="07c05-120">[in]メール アイテムの[PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="07c05-120">[in] The [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="07c05-121">できませんが NULL または無効です。</span><span class="sxs-lookup"><span data-stu-id="07c05-121">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="07c05-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="07c05-122">_dwFlags_</span></span>
  
> <span data-ttu-id="07c05-123">[in]メソッドの呼び出しに関する追加情報を指定するビットマスク。</span><span class="sxs-lookup"><span data-stu-id="07c05-123">[in] A bitmask that specifies additional information about the method call.</span></span>
    
   - <span data-ttu-id="07c05-124">0: このメソッドの呼び出しで追加のオプションは使用されません。</span><span class="sxs-lookup"><span data-stu-id="07c05-124">0—No additional options are used in this method call.</span></span> <span data-ttu-id="07c05-125">これは、推奨される値です。</span><span class="sxs-lookup"><span data-stu-id="07c05-125">This is the recommended value.</span></span> 
    
   - <span data-ttu-id="07c05-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**- _pmbinMsgEid_は、実際には、 [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx)のメッセージです。</span><span class="sxs-lookup"><span data-stu-id="07c05-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ is actually the [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) of the message.</span></span> <span data-ttu-id="07c05-127">の**PidTagSearchKey**を使用してリソース集中型ではの[PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx)がある場合は避ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="07c05-127">Using a **PidTagSearchKey** is resource intensive, and should be avoided if a [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) is available.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="07c05-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="07c05-128">Return values</span></span>

|<span data-ttu-id="07c05-129">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="07c05-129">**HRESULT**</span></span>|<span data-ttu-id="07c05-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="07c05-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07c05-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="07c05-131">S_OK</span></span>  <br/> |<span data-ttu-id="07c05-132">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="07c05-132">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="07c05-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="07c05-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="07c05-134">_dwFlags_には、不明なフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="07c05-134">_dwFlags_ contains an unknown flag.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07c05-135">備考</span><span class="sxs-lookup"><span data-stu-id="07c05-135">Remarks</span></span>

<span data-ttu-id="07c05-136">カテゴリでは、個人情報と見なされます、ユーザーのメールボックス以外の場所は転送されません。</span><span class="sxs-lookup"><span data-stu-id="07c05-136">Categories are considered personal information and should not be transmitted outside the mailbox of the user.</span></span> <span data-ttu-id="07c05-137">したがって、 **HrProcessConvActionForSentItem**をは、未送信のメール アイテムには呼び出さないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="07c05-137">Therefore, do not call **HrProcessConvActionForSentItem** on an unsent mail item.</span></span> <span data-ttu-id="07c05-138">代わりに、アイテムを送信し、アーカイブされたコピーで**HrProcessConvActionForSentItem**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="07c05-138">Instead, send the item, and then call **HrProcessConvActionForSentItem** on the archived copy.</span></span> <span data-ttu-id="07c05-139">アーカイブされたコピーは、送信済みアイテム フォルダー、または同等の場所に格納されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="07c05-139">The archived copy may be stored in the Sent Items folder, or an equivalent location.</span></span> 
  
<span data-ttu-id="07c05-140">アプリケーションはプロセス内である必要があります Outlook.exe など、COM アドイン、 **HrProcessConvActionForSentItem**を呼び出すとします。</span><span class="sxs-lookup"><span data-stu-id="07c05-140">Your application must be in-process with Outlook.exe, such as from a COM add-in, to call **HrProcessConvActionForSentItem**.</span></span> <span data-ttu-id="07c05-141">**HrProcessConvActionForSentItem**アウト プロセスの呼び出しを試みると、 **HrProcessConvActionForSentItem**は、アクセス違反の例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="07c05-141">If you attempt to call **HrProcessConvActionForSentItem** out-of-process, **HrProcessConvActionForSentItem** will throw an access-violation exception.</span></span> 
  

