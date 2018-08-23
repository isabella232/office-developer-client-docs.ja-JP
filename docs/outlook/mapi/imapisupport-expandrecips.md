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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2e41701d3a739864b1eafc8001833b7df5c8908b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800745"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="d0d8d-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="d0d8d-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="d0d8d-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0d8d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0d8d-105">メッセージの受信者リスト、特定の配布リストの展開を完了します。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d0d8d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d0d8d-106">Parameters</span></span>

 <span data-ttu-id="d0d8d-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="d0d8d-107">_lpMessage_</span></span>
  
> <span data-ttu-id="d0d8d-108">[in]処理する受信者のリストがあるメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="d0d8d-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="d0d8d-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="d0d8d-110">[out]発生する処理の種類を制御するフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="d0d8d-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-111">The following flags can be set:</span></span>
    
<span data-ttu-id="d0d8d-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="d0d8d-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="d0d8d-113">メッセージが送信される前に前処理が必要に必要です。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="d0d8d-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="d0d8d-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="d0d8d-115">MAPI スプーラーではなく、トランスポート プロバイダーは、呼び出し元が密に結合されている) は、メッセージを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d0d8d-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d0d8d-116">Return value</span></span>

<span data-ttu-id="d0d8d-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0d8d-117">S_OK</span></span> 
  
> <span data-ttu-id="d0d8d-118">メッセージの受信者の一覧が正常に処理されました。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d0d8d-119">注釈</span><span class="sxs-lookup"><span data-stu-id="d0d8d-119">Remarks</span></span>

<span data-ttu-id="d0d8d-120">メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::ExpandRecips**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="d0d8d-121">メッセージ ストア プロバイダーは、次のタスクを実行するための MAPI メッセージを表示するのには**ExpandRecips**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="d0d8d-122">そのコンポーネントの受信者に、特定の個人用配布リストを展開します。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="d0d8d-123">変更されたすべての表示名を元の名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="d0d8d-124">重複するエントリをマークします。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="d0d8d-125">1 回限りのすべてのアドレスを解決します。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="d0d8d-126">かどうか、メッセージの前処理を必要し場合は、NEEDS_PREPROCESSING に_lpulFlags_で指定されたフラグを設定を確認してください。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="d0d8d-127">**ExpandRecips**は、MAPIPDL のメッセージのアドレスの種類を持つすべての配布リストを展開します。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d0d8d-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d0d8d-128">Notes to callers</span></span>

<span data-ttu-id="d0d8d-129">常に、メッセージの処理の一部として**ExpandRecips**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="d0d8d-130">[IMessage::SubmitMessage](imessage-submitmessage.md)メソッドの実装では、 **ExpandRecips** 1 つの最初の呼び出しへの呼び出しを確認します。</span><span class="sxs-lookup"><span data-stu-id="d0d8d-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d0d8d-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="d0d8d-131">See also</span></span>



[<span data-ttu-id="d0d8d-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="d0d8d-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="d0d8d-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d0d8d-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

