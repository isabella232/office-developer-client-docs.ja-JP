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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 47ea122fce7969b326dbd48f875696b91de464f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568575"
---
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="93a35-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="93a35-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="93a35-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93a35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93a35-105">現在のメッセージを保存するために使用するストリームを取得します。</span><span class="sxs-lookup"><span data-stu-id="93a35-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="93a35-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="93a35-106">Parameters</span></span>

 <span data-ttu-id="93a35-107">_pulFlags_</span><span class="sxs-lookup"><span data-stu-id="93a35-107">_pulFlags_</span></span>
  
> <span data-ttu-id="93a35-108">[out]メッセージ テキストを保存する方法を制御するフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="93a35-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="93a35-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="93a35-109">The following flag can be set:</span></span>
    
<span data-ttu-id="93a35-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="93a35-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="93a35-111">メッセージ文字列は、Unicode 形式で保存されます。</span><span class="sxs-lookup"><span data-stu-id="93a35-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="93a35-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のテキストが保存されます。</span><span class="sxs-lookup"><span data-stu-id="93a35-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="93a35-113">_pulFormat_</span><span class="sxs-lookup"><span data-stu-id="93a35-113">_pulFormat_</span></span>
  
> <span data-ttu-id="93a35-114">[out]保存したテキストの書式を制御するフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="93a35-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="93a35-115">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="93a35-115">The following flags can be set:</span></span>
    
<span data-ttu-id="93a35-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="93a35-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="93a35-117">メッセージのテキストは、書式設定されたテキストで、リッチ テキスト形式式 (RTF) として保存するのには。</span><span class="sxs-lookup"><span data-stu-id="93a35-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="93a35-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="93a35-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="93a35-119">メッセージのテキストは、プレーン テキストとして保存するのには。</span><span class="sxs-lookup"><span data-stu-id="93a35-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="93a35-120">_ppstm_</span><span class="sxs-lookup"><span data-stu-id="93a35-120">_ppstm_</span></span>
  
> <span data-ttu-id="93a35-121">[out]保存されたメッセージを格納するストリームへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="93a35-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="93a35-122">�߂�l</span><span class="sxs-lookup"><span data-stu-id="93a35-122">Return value</span></span>

<span data-ttu-id="93a35-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="93a35-123">S_OK</span></span> 
  
> <span data-ttu-id="93a35-124">ストリームが正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="93a35-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="93a35-125">注釈</span><span class="sxs-lookup"><span data-stu-id="93a35-125">Remarks</span></span>

<span data-ttu-id="93a35-126">フォーム オブジェクトは、ストリーム形式のビューアーで、名前を付けて動詞の処理をサポートするために**IStream**インターフェイスを実装するオブジェクトを取得する**IMAPIViewContext::GetSaveStream**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="93a35-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="93a35-127">メッセージが完全に適切な文字列形式に変換し、適切なストリームに配置されるまで、 [IMAPIForm::DoVerb](imapiform-doverb.md)メソッドは、フォームのサーバーに実装されているし、動詞を呼び出すフォーム ビューアーによって呼び出されます、する必要があります返されません。</span><span class="sxs-lookup"><span data-stu-id="93a35-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="93a35-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="93a35-128">Notes to callers</span></span>

<span data-ttu-id="93a35-129">**GetSaveStream**を呼び出す前に_ppstm_で指定されたストリームに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="93a35-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="93a35-130">**GetSaveStream**が返されるときは、シーク ポインターの位置はリセットされません。</span><span class="sxs-lookup"><span data-stu-id="93a35-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="93a35-131">このポインターは必要があります保存されているメッセージのテキストの最後に残ります。</span><span class="sxs-lookup"><span data-stu-id="93a35-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="93a35-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="93a35-132">See also</span></span>



[<span data-ttu-id="93a35-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="93a35-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

