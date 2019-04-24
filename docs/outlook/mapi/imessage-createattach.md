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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351115"
---
# <a name="imessagecreateattach"></a><span data-ttu-id="c1d83-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="c1d83-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="c1d83-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1d83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1d83-105">新しい添付ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="c1d83-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="c1d83-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c1d83-106">Parameters</span></span>

 <span data-ttu-id="c1d83-107">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="c1d83-107">_lpInterface_</span></span>
  
> <span data-ttu-id="c1d83-108">順番メッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c1d83-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="c1d83-109">NULL 結果をメッセージの標準インターフェイスまたは**IMessage**に渡すと、返されます。</span><span class="sxs-lookup"><span data-stu-id="c1d83-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="c1d83-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c1d83-110">_ulFlags_</span></span>
  
> <span data-ttu-id="c1d83-111">順番添付ファイルの作成方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="c1d83-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="c1d83-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c1d83-112">The following flag can be set:</span></span>
    
<span data-ttu-id="c1d83-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c1d83-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c1d83-114">添付ファイルが呼び出し元クライアントに完全にアクセス可能になる前に、 **createattach**が正常に戻ることができるようにします。</span><span class="sxs-lookup"><span data-stu-id="c1d83-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="c1d83-115">添付ファイルにアクセスできない場合は、その後の呼び出しを行うとエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c1d83-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="c1d83-116">_lアウト attachmentnum_</span><span class="sxs-lookup"><span data-stu-id="c1d83-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="c1d83-117">読み上げ新しく作成された添付ファイルを識別するインデックス番号へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c1d83-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="c1d83-118">この番号は、メッセージが開いていて、添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティの基になっている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="c1d83-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="c1d83-119">_lppattach_</span><span class="sxs-lookup"><span data-stu-id="c1d83-119">_lppAttach_</span></span>
  
> <span data-ttu-id="c1d83-120">読み上げ開かれた attachment オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c1d83-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1d83-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="c1d83-121">Return value</span></span>

<span data-ttu-id="c1d83-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="c1d83-122">S_OK</span></span> 
  
> <span data-ttu-id="c1d83-123">添付ファイルが正常に作成されました。</span><span class="sxs-lookup"><span data-stu-id="c1d83-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1d83-124">解説</span><span class="sxs-lookup"><span data-stu-id="c1d83-124">Remarks</span></span>

<span data-ttu-id="c1d83-125">**IMessage:: createattach**メソッドは、メッセージに新しい添付ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="c1d83-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="c1d83-126">新しい添付ファイルと、そのオブジェクトに設定されているすべてのプロパティは、クライアントが添付ファイルの[imapiprop:: savechanges](imapiprop-savechanges.md)メソッドと、メッセージの**imapiprop:: savechanges**メソッドの両方を呼び出すまでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="c1d83-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="c1d83-127">_lアウト attachmentnum_が指す添付ファイルの番号は一意で、メッセージのコンテキスト内でのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="c1d83-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="c1d83-128">つまり、同じメッセージ内の2つの添付ファイルでは、2つの異なるメッセージの2つの添付ファイルを同じ数にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c1d83-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c1d83-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1d83-129">See also</span></span>



[<span data-ttu-id="c1d83-130">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c1d83-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

