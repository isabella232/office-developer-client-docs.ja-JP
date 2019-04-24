---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: メールアイテムの PidTagConversationId に基づいて、送信後の分類を実行します。
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318901"
---
# <a name="hrprocessconvactionforsentitem"></a><span data-ttu-id="fc1a9-103">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="fc1a9-103">HrProcessConvActionForSentItem</span></span>

<span data-ttu-id="fc1a9-104">メールアイテムの[PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx)に基づいて、送信後の分類を実行します。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-104">Performs post-send categorization on a mail item based on its [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fc1a9-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="fc1a9-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc1a9-106">エクスポート対象:</span><span class="sxs-lookup"><span data-stu-id="fc1a9-106">Exported by:</span></span>  <br/> |<span data-ttu-id="fc1a9-107">outlook.exe</span><span class="sxs-lookup"><span data-stu-id="fc1a9-107">Outlook.exe</span></span>  <br/> |
|<span data-ttu-id="fc1a9-108">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="fc1a9-108">Called by:</span></span>  <br/> |<span data-ttu-id="fc1a9-109">クライアント</span><span class="sxs-lookup"><span data-stu-id="fc1a9-109">Client</span></span>  <br/> |
|<span data-ttu-id="fc1a9-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="fc1a9-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="fc1a9-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="fc1a9-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a><span data-ttu-id="fc1a9-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fc1a9-112">Parameters</span></span>

<span data-ttu-id="fc1a9-113">_pmbinStoreEid_</span><span class="sxs-lookup"><span data-stu-id="fc1a9-113">_pmbinStoreEid_</span></span>
  
> <span data-ttu-id="fc1a9-114">順番ストアの[PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) 、またはメールアイテムの[PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-114">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the store, or the [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="fc1a9-115">NULL または無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-115">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="fc1a9-116">_pmbinmsgeid_</span><span class="sxs-lookup"><span data-stu-id="fc1a9-116">_pmbinMsgEid_</span></span>
  
> <span data-ttu-id="fc1a9-117">順番メールアイテムの[PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-117">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="fc1a9-118">NULL または無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-118">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="fc1a9-119">_pmbinconvid_</span><span class="sxs-lookup"><span data-stu-id="fc1a9-119">_pmbinConvID_</span></span>
  
> <span data-ttu-id="fc1a9-120">順番メールアイテムの[PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-120">[in] The [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="fc1a9-121">NULL または無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-121">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="fc1a9-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="fc1a9-122">_dwFlags_</span></span>
  
> <span data-ttu-id="fc1a9-123">順番メソッド呼び出しに関する追加情報を指定するビットマスク。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-123">[in] A bitmask that specifies additional information about the method call.</span></span>
    
   - <span data-ttu-id="fc1a9-124">0-このメソッド呼び出しでは、追加のオプションは使用されません。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-124">0—No additional options are used in this method call.</span></span> <span data-ttu-id="fc1a9-125">この値を指定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-125">This is the recommended value.</span></span> 
    
   - <span data-ttu-id="fc1a9-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinmsgeid_は、実際にはメッセージの[PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx)です。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ is actually the [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) of the message.</span></span> <span data-ttu-id="fc1a9-127">**PidTagSearchKey**を使用すると、リソースが大量に消費されるため、 [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx)を使用できる場合は回避する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-127">Using a **PidTagSearchKey** is resource intensive, and should be avoided if a [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) is available.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="fc1a9-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="fc1a9-128">Return values</span></span>

|<span data-ttu-id="fc1a9-129">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="fc1a9-129">**HRESULT**</span></span>|<span data-ttu-id="fc1a9-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="fc1a9-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fc1a9-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="fc1a9-131">S_OK</span></span>  <br/> |<span data-ttu-id="fc1a9-132">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-132">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="fc1a9-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="fc1a9-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="fc1a9-134">_dwFlags_に不明なフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-134">_dwFlags_ contains an unknown flag.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc1a9-135">解説</span><span class="sxs-lookup"><span data-stu-id="fc1a9-135">Remarks</span></span>

<span data-ttu-id="fc1a9-136">カテゴリは個人情報と見なされるため、ユーザーのメールボックスの外部に送信することはできません。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-136">Categories are considered personal information and should not be transmitted outside the mailbox of the user.</span></span> <span data-ttu-id="fc1a9-137">そのため、未送信のメールアイテムに対して**HrProcessConvActionForSentItem**を呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-137">Therefore, do not call **HrProcessConvActionForSentItem** on an unsent mail item.</span></span> <span data-ttu-id="fc1a9-138">代わりに、アイテムを送信してから、アーカイブコピーで**HrProcessConvActionForSentItem**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-138">Instead, send the item, and then call **HrProcessConvActionForSentItem** on the archived copy.</span></span> <span data-ttu-id="fc1a9-139">アーカイブされたコピーは、[送信済みアイテム] フォルダーまたは同等の場所に保存できます。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-139">The archived copy may be stored in the Sent Items folder, or an equivalent location.</span></span> 
  
<span data-ttu-id="fc1a9-140">アプリケーションは、 **HrProcessConvActionForSentItem**を呼び出すために、COM アドインからの場合など、outlook.exe を使用して処理されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-140">Your application must be in-process with Outlook.exe, such as from a COM add-in, to call **HrProcessConvActionForSentItem**.</span></span> <span data-ttu-id="fc1a9-141">プロセス外で**HrProcessConvActionForSentItem**を呼び出そうとすると、 **HrProcessConvActionForSentItem**によってアクセス違反例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="fc1a9-141">If you attempt to call **HrProcessConvActionForSentItem** out-of-process, **HrProcessConvActionForSentItem** will throw an access-violation exception.</span></span> 
  

