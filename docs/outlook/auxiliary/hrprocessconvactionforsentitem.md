---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: PidTagConversationId に基づいてメール アイテムに対して送信後の分類を実行します。
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318901"
---
# <a name="hrprocessconvactionforsentitem"></a><span data-ttu-id="e1d65-103">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="e1d65-103">HrProcessConvActionForSentItem</span></span>

<span data-ttu-id="e1d65-104">[PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx)に基づいてメール アイテムに対して送信後の分類を実行します。</span><span class="sxs-lookup"><span data-stu-id="e1d65-104">Performs post-send categorization on a mail item based on its [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e1d65-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e1d65-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1d65-106">次の方法でエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="e1d65-106">Exported by:</span></span>  <br/> |<span data-ttu-id="e1d65-107">Outlook.exe</span><span class="sxs-lookup"><span data-stu-id="e1d65-107">Outlook.exe</span></span>  <br/> |
|<span data-ttu-id="e1d65-108">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e1d65-108">Called by:</span></span>  <br/> |<span data-ttu-id="e1d65-109">クライアント</span><span class="sxs-lookup"><span data-stu-id="e1d65-109">Client</span></span>  <br/> |
|<span data-ttu-id="e1d65-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="e1d65-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="e1d65-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="e1d65-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a><span data-ttu-id="e1d65-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e1d65-112">Parameters</span></span>

<span data-ttu-id="e1d65-113">_pmbinStoreEid_</span><span class="sxs-lookup"><span data-stu-id="e1d65-113">_pmbinStoreEid_</span></span>
  
> <span data-ttu-id="e1d65-114">[in]ストア[の PidTagEntryId、](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx)またはメール[アイテムの PidTagStoreEntryId。](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1d65-114">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the store, or the [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="e1d65-115">NULL または無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e1d65-115">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="e1d65-116">_pmbinMsgEid_</span><span class="sxs-lookup"><span data-stu-id="e1d65-116">_pmbinMsgEid_</span></span>
  
> <span data-ttu-id="e1d65-117">[in]メール[アイテムの PidTagEntryId。](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1d65-117">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="e1d65-118">NULL または無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e1d65-118">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="e1d65-119">_pmbinConvID_</span><span class="sxs-lookup"><span data-stu-id="e1d65-119">_pmbinConvID_</span></span>
  
> <span data-ttu-id="e1d65-120">[in]メール[アイテムの PidTagConversationId。](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1d65-120">[in] The [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="e1d65-121">NULL または無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e1d65-121">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="e1d65-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="e1d65-122">_dwFlags_</span></span>
  
> <span data-ttu-id="e1d65-123">[in]メソッド呼び出しに関する追加情報を指定するビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e1d65-123">[in] A bitmask that specifies additional information about the method call.</span></span>
    
   - <span data-ttu-id="e1d65-124">0 - このメソッド呼び出しでは、追加のオプションは使用されません。</span><span class="sxs-lookup"><span data-stu-id="e1d65-124">0—No additional options are used in this method call.</span></span> <span data-ttu-id="e1d65-125">これは推奨される値です。</span><span class="sxs-lookup"><span data-stu-id="e1d65-125">This is the recommended value.</span></span> 
    
   - <span data-ttu-id="e1d65-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ は、実際には [メッセージの PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) です。</span><span class="sxs-lookup"><span data-stu-id="e1d65-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ is actually the [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) of the message.</span></span> <span data-ttu-id="e1d65-127">**PidTagSearchKey** の使用はリソースの負荷が高く [、PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx)が使用可能な場合は避ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1d65-127">Using a **PidTagSearchKey** is resource intensive, and should be avoided if a [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) is available.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="e1d65-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="e1d65-128">Return values</span></span>

|<span data-ttu-id="e1d65-129">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="e1d65-129">**HRESULT**</span></span>|<span data-ttu-id="e1d65-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="e1d65-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e1d65-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="e1d65-131">S_OK</span></span>  <br/> |<span data-ttu-id="e1d65-132">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="e1d65-132">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="e1d65-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e1d65-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="e1d65-134">_dwFlags には_ 不明なフラグが含まれている。</span><span class="sxs-lookup"><span data-stu-id="e1d65-134">_dwFlags_ contains an unknown flag.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1d65-135">注釈</span><span class="sxs-lookup"><span data-stu-id="e1d65-135">Remarks</span></span>

<span data-ttu-id="e1d65-136">カテゴリは個人情報と見なされ、ユーザーのメールボックスの外部に送信される必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1d65-136">Categories are considered personal information and should not be transmitted outside the mailbox of the user.</span></span> <span data-ttu-id="e1d65-137">したがって、送信されていないメール アイテム **に対して HrProcessConvActionForSentItem** を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1d65-137">Therefore, do not call **HrProcessConvActionForSentItem** on an unsent mail item.</span></span> <span data-ttu-id="e1d65-138">代わりに、アイテムを送信し、アーカイブされたコピーで **HrProcessConvActionForSentItem** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e1d65-138">Instead, send the item, and then call **HrProcessConvActionForSentItem** on the archived copy.</span></span> <span data-ttu-id="e1d65-139">アーカイブされたコピーは、[送信済みアイテム] フォルダーまたは同等の場所に保存できます。</span><span class="sxs-lookup"><span data-stu-id="e1d65-139">The archived copy may be stored in the Sent Items folder, or an equivalent location.</span></span> 
  
<span data-ttu-id="e1d65-140">**HrProcessConvActionForSentItem** を呼び出Outlook.exe COM アドインなど、アプリケーションがプロセス内にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1d65-140">Your application must be in-process with Outlook.exe, such as from a COM add-in, to call **HrProcessConvActionForSentItem**.</span></span> <span data-ttu-id="e1d65-141">**HrProcessConvActionForSentItem** をアウトプロセスで呼び出す場合 **、HrProcessConvActionForSentItem** はアクセス違反例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="e1d65-141">If you attempt to call **HrProcessConvActionForSentItem** out-of-process, **HrProcessConvActionForSentItem** will throw an access-violation exception.</span></span> 
  

