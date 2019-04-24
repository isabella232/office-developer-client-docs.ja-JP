---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 154d6e4a4e333f3a6165c3875bdcd57957ebf70c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348735"
---
# <a name="itnefopentaggedbody"></a><span data-ttu-id="24677-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="24677-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="24677-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24677-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24677-105">カプセル化されたメッセージのテキストにストリームインターフェイスを開きます。</span><span class="sxs-lookup"><span data-stu-id="24677-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="24677-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="24677-106">Parameters</span></span>

 <span data-ttu-id="24677-107">_lpmessage_</span><span class="sxs-lookup"><span data-stu-id="24677-107">_lpMessage_</span></span>
  
> <span data-ttu-id="24677-108">順番stream が関連付けられているメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="24677-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="24677-109">このメッセージは、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の呼び出しで渡されるメッセージと同じである必要はありません。</span><span class="sxs-lookup"><span data-stu-id="24677-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="24677-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="24677-110">_ulFlags_</span></span>
  
> <span data-ttu-id="24677-111">順番stream インターフェイスを開く方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="24677-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="24677-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="24677-112">The following flags can be set:</span></span>
    
<span data-ttu-id="24677-113">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="24677-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="24677-114">プロパティが現在のメッセージ内に存在しない場合は、作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24677-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="24677-115">プロパティが存在する場合、プロパティの現在のデータは、トランスポートに中立的なカプセル化形式 (TNEF) ストリームのデータに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="24677-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="24677-116">実装で MAPI_CREATE フラグが設定されている場合は、MAPI_MODIFY フラグも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24677-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="24677-117">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="24677-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="24677-118">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="24677-118">Requests read/write permission.</span></span> <span data-ttu-id="24677-119">既定のインターフェイスは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="24677-119">The default interface is read-only.</span></span> <span data-ttu-id="24677-120">MAPI_CREATE が設定されている場合は常に、MAPI_MODIFY を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="24677-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="24677-121">_lppstream_</span><span class="sxs-lookup"><span data-stu-id="24677-121">_lppStream_</span></span>
  
> <span data-ttu-id="24677-122">読み上げ渡されたカプセル化されたメッセージの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティから、 [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream)インターフェイスをサポートするテキストを含む stream オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="24677-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="24677-123">戻り値</span><span class="sxs-lookup"><span data-stu-id="24677-123">Return value</span></span>

<span data-ttu-id="24677-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="24677-124">S_OK</span></span> 
  
> <span data-ttu-id="24677-125">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="24677-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="24677-126">解説</span><span class="sxs-lookup"><span data-stu-id="24677-126">Remarks</span></span>

<span data-ttu-id="24677-127">トランスポートプロバイダー、メッセージストアプロバイダー、およびゲートウェイは、 **ITnef:: OpenTaggedBody**メソッドを呼び出して、カプセル化されたメッセージ (つまり TNEF オブジェクト) のテキストのストリームインターフェイスを開きます。</span><span class="sxs-lookup"><span data-stu-id="24677-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="24677-128">**OpenTaggedBody**は、処理の一環として、メッセージテキスト内の添付ファイルまたは OLE オブジェクトの位置を示す添付ファイルタグを挿入または解析します。</span><span class="sxs-lookup"><span data-stu-id="24677-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="24677-129">添付ファイルタグは、次の形式になります。</span><span class="sxs-lookup"><span data-stu-id="24677-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="24677-130">**[[** 添付ファイル_名_ **:** _n_ \*\*\*\* _添付ファイルコンテナー名_ **]]**</span><span class="sxs-lookup"><span data-stu-id="24677-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="24677-131">_添付ファイル名_添付ファイルオブジェクトについて説明します。 _n_は、シーケンスの一部である添付ファイルを識別する数値で、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の_lpkey_パラメーターで渡された値を増分します。_添付ファイルコンテナー名_は、attachment オブジェクトが存在する物理コンポーネントを表します。</span><span class="sxs-lookup"><span data-stu-id="24677-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="24677-132">**OpenTaggedBody**は、メッセージテキストを読み取り、添付ファイルオブジェクトが最初にテキストに表示された場所に添付ファイルのタグを挿入します。</span><span class="sxs-lookup"><span data-stu-id="24677-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="24677-133">元のメッセージテキストは変更されません。</span><span class="sxs-lookup"><span data-stu-id="24677-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="24677-134">タグを持つメッセージが stream に渡されると、タグが削除され、添付ファイルオブジェクトがストリーム内のタグの位置に移動されます。</span><span class="sxs-lookup"><span data-stu-id="24677-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="24677-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="24677-135">See also</span></span>



[<span data-ttu-id="24677-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="24677-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="24677-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="24677-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="24677-138">PidTagBody 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="24677-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="24677-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="24677-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

