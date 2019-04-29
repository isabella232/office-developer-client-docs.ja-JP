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
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="c8b22-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="c8b22-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="c8b22-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8b22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8b22-105">特定の配布リストを展開し、メッセージの受信者の一覧を完成させる。</span><span class="sxs-lookup"><span data-stu-id="c8b22-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c8b22-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c8b22-106">Parameters</span></span>

 <span data-ttu-id="c8b22-107">_lpmessage_</span><span class="sxs-lookup"><span data-stu-id="c8b22-107">_lpMessage_</span></span>
  
> <span data-ttu-id="c8b22-108">順番処理する受信者リストがあるメッセージへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c8b22-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="c8b22-109">_lアウトフラグ_</span><span class="sxs-lookup"><span data-stu-id="c8b22-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="c8b22-110">読み上げ発生する処理の種類を制御するフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c8b22-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="c8b22-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c8b22-111">The following flags can be set:</span></span>
    
<span data-ttu-id="c8b22-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="c8b22-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="c8b22-113">メッセージを送信する前に前処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8b22-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="c8b22-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="c8b22-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="c8b22-115">MAPI スプーラー (発信者が密接に結合されているトランスポートプロバイダーではない) は、メッセージを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8b22-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c8b22-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="c8b22-116">Return value</span></span>

<span data-ttu-id="c8b22-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="c8b22-117">S_OK</span></span> 
  
> <span data-ttu-id="c8b22-118">メッセージの宛先リストが正常に処理されました。</span><span class="sxs-lookup"><span data-stu-id="c8b22-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c8b22-119">注釈</span><span class="sxs-lookup"><span data-stu-id="c8b22-119">Remarks</span></span>

<span data-ttu-id="c8b22-120">**imapisupport:: ExpandRecips**メソッドは、メッセージストアプロバイダーサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="c8b22-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="c8b22-121">メッセージストアプロバイダーは**ExpandRecips**を呼び出して、次のタスクを実行するように MAPI に通知します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="c8b22-122">特定の個人用配布リストをコンポーネントの受信者に展開します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="c8b22-123">変更されたすべての表示名を元の名前に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="c8b22-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="c8b22-124">重複しているエントリをマークします。</span><span class="sxs-lookup"><span data-stu-id="c8b22-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="c8b22-125">1回限りのすべての住所を解決します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="c8b22-126">メッセージにプリプロセスが必要かどうかを確認し、実行されている場合は、 _lNEEDS_PREPROCESSING フラグ_が指すフラグをに設定します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="c8b22-127">**ExpandRecips**は、メッセージアドレスの種類が mapipdl であるすべての配布リストを展開します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c8b22-128">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="c8b22-128">Notes to callers</span></span>

<span data-ttu-id="c8b22-129">メッセージ処理の一部として**ExpandRecips**を常に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="c8b22-130">[IMessage:: submitmessage](imessage-submitmessage.md)メソッド実装の最初の呼び出しの1つを**ExpandRecips**に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c8b22-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c8b22-131">関連項目</span><span class="sxs-lookup"><span data-stu-id="c8b22-131">See also</span></span>



[<span data-ttu-id="c8b22-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="c8b22-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="c8b22-133">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c8b22-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

