---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f534912377aadb3c342030fc02fce26693857476
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417673"
---
# <a name="imessagecreateattach"></a><span data-ttu-id="f0bbf-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="f0bbf-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="f0bbf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0bbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0bbf-105">新しい添付ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="f0bbf-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f0bbf-106">Parameters</span></span>

 <span data-ttu-id="f0bbf-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f0bbf-107">_lpInterface_</span></span>
  
> <span data-ttu-id="f0bbf-108">[in]メッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="f0bbf-109">NULL を渡すと、メッセージの標準インターフェイス **(IMessage)** が返されます。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="f0bbf-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f0bbf-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f0bbf-111">[in]添付ファイルの作成方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="f0bbf-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-112">The following flag can be set:</span></span>
    
<span data-ttu-id="f0bbf-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="f0bbf-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="f0bbf-114">**CreateAttach を** 正常に返す (おそらく、呼び出し元のクライアントが添付ファイルに完全にアクセスできる前に) 許可します。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="f0bbf-115">添付ファイルにアクセスできない場合は、後続の呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="f0bbf-116">_lpulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="f0bbf-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="f0bbf-117">[out]新しく作成された添付ファイルを識別するインデックス番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="f0bbf-118">この番号は、メッセージが開いている場合にのみ有効で、添付ファイルのプロパティ **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティPR_ATTACH_NUM基になります。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="f0bbf-119">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="f0bbf-119">_lppAttach_</span></span>
  
> <span data-ttu-id="f0bbf-120">[out]開いている添付ファイル オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f0bbf-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="f0bbf-121">Return value</span></span>

<span data-ttu-id="f0bbf-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0bbf-122">S_OK</span></span> 
  
> <span data-ttu-id="f0bbf-123">添付ファイルが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f0bbf-124">注釈</span><span class="sxs-lookup"><span data-stu-id="f0bbf-124">Remarks</span></span>

<span data-ttu-id="f0bbf-125">**IMessage::CreateAttach メソッドは**、メッセージに新しい添付ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="f0bbf-126">新しい添付ファイルと設定されているプロパティは、クライアントが添付ファイルの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドとメッセージの **IMAPIProp::SaveChanges** メソッドの両方を呼び出すまで使用できません。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="f0bbf-127">_lpulAttachmentNum_ が指す添付ファイル番号は一意であり、メッセージのコンテキスト内でのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="f0bbf-128">つまり、2 つの異なるメッセージ内の 2 つの添付ファイルは同じ番号を持ち、同じメッセージ内の 2 つの添付ファイルは使用できません。</span><span class="sxs-lookup"><span data-stu-id="f0bbf-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f0bbf-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0bbf-129">See also</span></span>



[<span data-ttu-id="f0bbf-130">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f0bbf-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

