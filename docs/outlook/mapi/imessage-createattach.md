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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6351be353100649e38a14543a44df5e115c9408b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800898"
---
# <a name="imessagecreateattach"></a><span data-ttu-id="ab200-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="ab200-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="ab200-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ab200-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ab200-105">新しい添付ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab200-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="ab200-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ab200-106">Parameters</span></span>

 <span data-ttu-id="ab200-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="ab200-107">_lpInterface_</span></span>
  
> <span data-ttu-id="ab200-108">[in]メッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab200-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="ab200-109">パラメーターに NULL が返されるメッセージの標準的なインタ フェース、または**IMessage**、発生します。</span><span class="sxs-lookup"><span data-stu-id="ab200-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="ab200-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ab200-110">_ulFlags_</span></span>
  
> <span data-ttu-id="ab200-111">[in]添付ファイルを作成する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ab200-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="ab200-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ab200-112">The following flag can be set:</span></span>
    
<span data-ttu-id="ab200-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ab200-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ab200-114">正常に戻す、可能性のある添付ファイルが呼び出し側のクライアントに完全にアクセスする前に**CreateAttach**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ab200-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="ab200-115">添付ファイルがアクセスできない場合は、エラーにつながるに後続の呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="ab200-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="ab200-116">_lpulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="ab200-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="ab200-117">[out]新しく作成された添付ファイルを識別するインデックス番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab200-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="ab200-118">この番号は、メッセージ、添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) のプロパティの基礎となる場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="ab200-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="ab200-119">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="ab200-119">_lppAttach_</span></span>
  
> <span data-ttu-id="ab200-120">[out]添付ファイルを開くオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ab200-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ab200-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ab200-121">Return value</span></span>

<span data-ttu-id="ab200-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab200-122">S_OK</span></span> 
  
> <span data-ttu-id="ab200-123">添付ファイルが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="ab200-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab200-124">注釈</span><span class="sxs-lookup"><span data-stu-id="ab200-124">Remarks</span></span>

<span data-ttu-id="ab200-125">**IMessage::CreateAttach**メソッドでは、メッセージに新しい添付ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="ab200-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="ab200-126">新しい添付ファイルと、それに設定されている任意のプロパティは利用可能な添付ファイルの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドとメッセージの**IMAPIProp::SaveChanges**メソッドの両方にクライアントが呼び出されるまで。</span><span class="sxs-lookup"><span data-stu-id="ab200-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="ab200-127">_LpulAttachmentNum_で指定された添付ファイル数は、一意であり、メッセージのコンテキスト内でのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="ab200-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="ab200-128">2 種類のメッセージで 2 つの添付ファイルは同じメッセージに添付ファイルを 2 つ、同じ番号を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="ab200-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab200-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="ab200-129">See also</span></span>



[<span data-ttu-id="ab200-130">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ab200-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

