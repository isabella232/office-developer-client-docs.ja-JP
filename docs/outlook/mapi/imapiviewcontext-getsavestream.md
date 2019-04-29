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
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="dac30-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="dac30-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="dac30-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dac30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dac30-105">現在のメッセージを保存するために使用するストリームを取得します。</span><span class="sxs-lookup"><span data-stu-id="dac30-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="dac30-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dac30-106">Parameters</span></span>

 <span data-ttu-id="dac30-107">_/フラグ_</span><span class="sxs-lookup"><span data-stu-id="dac30-107">_pulFlags_</span></span>
  
> <span data-ttu-id="dac30-108">読み上げメッセージテキストの保存方法を制御するフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="dac30-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="dac30-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="dac30-109">The following flag can be set:</span></span>
    
<span data-ttu-id="dac30-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="dac30-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="dac30-111">メッセージテキストは、Unicode 形式で保存されます。</span><span class="sxs-lookup"><span data-stu-id="dac30-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="dac30-112">MAPI_UNICODE フラグが設定されていない場合、テキストは ANSI 形式で保存されます。</span><span class="sxs-lookup"><span data-stu-id="dac30-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="dac30-113">_指定形式_</span><span class="sxs-lookup"><span data-stu-id="dac30-113">_pulFormat_</span></span>
  
> <span data-ttu-id="dac30-114">読み上げ保存されたテキストの形式を制御するフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="dac30-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="dac30-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="dac30-115">The following flags can be set:</span></span>
    
<span data-ttu-id="dac30-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="dac30-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="dac30-117">メッセージテキストは、リッチテキスト形式 (RTF) で書式設定されたテキストとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="dac30-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="dac30-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="dac30-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="dac30-119">メッセージテキストは、プレーンテキストとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="dac30-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="dac30-120">_ppstm_</span><span class="sxs-lookup"><span data-stu-id="dac30-120">_ppstm_</span></span>
  
> <span data-ttu-id="dac30-121">読み上げ保存されたメッセージを格納するストリームへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="dac30-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dac30-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="dac30-122">Return value</span></span>

<span data-ttu-id="dac30-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="dac30-123">S_OK</span></span> 
  
> <span data-ttu-id="dac30-124">ストリームが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="dac30-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dac30-125">注釈</span><span class="sxs-lookup"><span data-stu-id="dac30-125">Remarks</span></span>

<span data-ttu-id="dac30-126">form オブジェクトは、 **imapiviewcontext:: GetSaveStream**メソッドを呼び出して、フォームビューアーでの [名前を付けて保存の操作をサポートする**IStream**インターフェイスを実装するオブジェクトをストリームを取得します。</span><span class="sxs-lookup"><span data-stu-id="dac30-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="dac30-127">[imapiform::D overb](imapiform-doverb.md)メソッドは、フォームサーバーに実装され、動詞を呼び出すためにフォームビューアーによって呼び出されます。メッセージが完全に適切なテキスト形式に変換され、適切なストリームに配置されるまで、戻りません。</span><span class="sxs-lookup"><span data-stu-id="dac30-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dac30-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="dac30-128">Notes to callers</span></span>

<span data-ttu-id="dac30-129">**GetSaveStream**を呼び出す前に、 _ppstm_が指すストリームに書き込みを行わないでください。</span><span class="sxs-lookup"><span data-stu-id="dac30-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="dac30-130">**GetSaveStream**が返された場合、シークポインターの位置をリセットしません。</span><span class="sxs-lookup"><span data-stu-id="dac30-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="dac30-131">このポインターは、保存されたメッセージテキストの末尾に置いておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="dac30-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dac30-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="dac30-132">See also</span></span>



[<span data-ttu-id="dac30-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dac30-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

