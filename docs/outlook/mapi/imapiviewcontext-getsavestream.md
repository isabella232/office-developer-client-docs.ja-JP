---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 68eb74f53d6cee4661c98604ec2ea37609e20ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408426"
---
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="37691-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="37691-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="37691-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37691-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37691-105">現在のメッセージの保存に使用するストリームを取得します。</span><span class="sxs-lookup"><span data-stu-id="37691-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="37691-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="37691-106">Parameters</span></span>

 <span data-ttu-id="37691-107">_pulFlags_</span><span class="sxs-lookup"><span data-stu-id="37691-107">_pulFlags_</span></span>
  
> <span data-ttu-id="37691-108">[out]メッセージ テキストの保存方法を制御するフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="37691-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="37691-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="37691-109">The following flag can be set:</span></span>
    
<span data-ttu-id="37691-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="37691-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="37691-111">メッセージ テキストは Unicode 形式で保存されます。</span><span class="sxs-lookup"><span data-stu-id="37691-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="37691-112">このフラグMAPI_UNICODE設定されていない場合、テキストは ANSI 形式で保存されます。</span><span class="sxs-lookup"><span data-stu-id="37691-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="37691-113">_pulFormat_</span><span class="sxs-lookup"><span data-stu-id="37691-113">_pulFormat_</span></span>
  
> <span data-ttu-id="37691-114">[out]保存されたテキストの形式を制御するフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="37691-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="37691-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="37691-115">The following flags can be set:</span></span>
    
<span data-ttu-id="37691-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="37691-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="37691-117">メッセージ テキストは、リッチ テキスト形式 (RTF) に書式設定されたテキストとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="37691-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="37691-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="37691-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="37691-119">メッセージ テキストはプレーン テキストとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="37691-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="37691-120">_ppstm_</span><span class="sxs-lookup"><span data-stu-id="37691-120">_ppstm_</span></span>
  
> <span data-ttu-id="37691-121">[out]保存されたメッセージを含むストリームへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="37691-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="37691-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="37691-122">Return value</span></span>

<span data-ttu-id="37691-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="37691-123">S_OK</span></span> 
  
> <span data-ttu-id="37691-124">ストリームが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="37691-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="37691-125">注釈</span><span class="sxs-lookup"><span data-stu-id="37691-125">Remarks</span></span>

<span data-ttu-id="37691-126">フォーム オブジェクトは **IMAPIViewContext::GetSaveStream** メソッドを呼び出して **、フォーム** ビューアーで Save As 動詞の処理をサポートするために IStream インターフェイスを実装するオブジェクトをストリームで取得します。</span><span class="sxs-lookup"><span data-stu-id="37691-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="37691-127">フォーム サーバーに実装され、動詞を呼び出すフォーム ビューアーによって呼び出される [IMAPIForm::D oVerb](imapiform-doverb.md) メソッドは、メッセージが完全に適切なテキスト形式に変換され、適切なストリームに配置されるまで返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="37691-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="37691-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="37691-128">Notes to callers</span></span>

<span data-ttu-id="37691-129">GetSaveStream を呼び出す前に  _、ppstm_ が指す **ストリームに書き込む必要があります**。</span><span class="sxs-lookup"><span data-stu-id="37691-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="37691-130">**GetSaveStream が** 返される場合は、シーク ポインターの位置をリセットしない。</span><span class="sxs-lookup"><span data-stu-id="37691-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="37691-131">このポインターは、保存されたメッセージ テキストの末尾に残る必要があります。</span><span class="sxs-lookup"><span data-stu-id="37691-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="37691-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="37691-132">See also</span></span>



[<span data-ttu-id="37691-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="37691-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

