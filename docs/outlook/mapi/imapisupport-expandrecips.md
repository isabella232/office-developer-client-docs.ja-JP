---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 105219fe430cd8746c3aa6cf5cd90629d5f72080
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411247"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="49c22-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="49c22-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="49c22-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49c22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49c22-105">メッセージの受信者リストを完了し、特定の配布リストを展開します。</span><span class="sxs-lookup"><span data-stu-id="49c22-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="49c22-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="49c22-106">Parameters</span></span>

 <span data-ttu-id="49c22-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="49c22-107">_lpMessage_</span></span>
  
> <span data-ttu-id="49c22-108">[in]処理する受信者リストを持つメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="49c22-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="49c22-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="49c22-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="49c22-110">[out]発生する処理の種類を制御するフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="49c22-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="49c22-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="49c22-111">The following flags can be set:</span></span>
    
<span data-ttu-id="49c22-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="49c22-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="49c22-113">メッセージを送信する前に、メッセージを前処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49c22-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="49c22-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="49c22-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="49c22-115">MAPI スプーラー (呼び出し元が緊密に結合されているトランスポート プロバイダーではなく) は、メッセージを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49c22-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="49c22-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="49c22-116">Return value</span></span>

<span data-ttu-id="49c22-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="49c22-117">S_OK</span></span> 
  
> <span data-ttu-id="49c22-118">メッセージの受信者リストが正常に処理されました。</span><span class="sxs-lookup"><span data-stu-id="49c22-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49c22-119">注釈</span><span class="sxs-lookup"><span data-stu-id="49c22-119">Remarks</span></span>

<span data-ttu-id="49c22-120">**IMAPISupport::ExpandRecips** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="49c22-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="49c22-121">メッセージ ストア プロバイダーは **ExpandRecips を呼び出して** 、MAPI に次のタスクを実行するように求めるプロンプトを表示します。</span><span class="sxs-lookup"><span data-stu-id="49c22-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="49c22-122">特定の個人用配布リストをコンポーネントの受信者に展開します。</span><span class="sxs-lookup"><span data-stu-id="49c22-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="49c22-123">変更された表示名を元の名前に置き換える。</span><span class="sxs-lookup"><span data-stu-id="49c22-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="49c22-124">重複するエントリをマークします。</span><span class="sxs-lookup"><span data-stu-id="49c22-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="49c22-125">すべての一時アドレスを解決します。</span><span class="sxs-lookup"><span data-stu-id="49c22-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="49c22-126">メッセージに前処理が必要かどうかを確認し、メッセージが処理する場合は  _、lpulFlags_ が示すフラグを NEEDS_PREPROCESSING。</span><span class="sxs-lookup"><span data-stu-id="49c22-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="49c22-127">**ExpandRecips は** 、MAPIPDL のメッセージング アドレスの種類を持つ配布リストを展開します。</span><span class="sxs-lookup"><span data-stu-id="49c22-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="49c22-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="49c22-128">Notes to callers</span></span>

<span data-ttu-id="49c22-129">メッセージ処理の **一部として ExpandRecips** を常に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="49c22-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="49c22-130">**ExpandRecips への呼び出しは**[、IMessage::SubmitMessage](imessage-submitmessage.md)メソッド実装の最初の呼び出しの 1 つを行います。</span><span class="sxs-lookup"><span data-stu-id="49c22-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="49c22-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="49c22-131">See also</span></span>



[<span data-ttu-id="49c22-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="49c22-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="49c22-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="49c22-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

