---
title: IMAPIProp IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a397ac9110429911755552298ffe244343d54a8a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583730"
---
# <a name="imapiprop--iunknown"></a><span data-ttu-id="8a4aa-103">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a4aa-103">IMAPIProp : IUnknown</span></span>

  
  
<span data-ttu-id="8a4aa-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a4aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a4aa-105">プロパティを操作するには、クライアント、サービス プロバイダー、および MAPI を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-105">Enables clients, service providers, and MAPI to work with properties.</span></span> <span data-ttu-id="8a4aa-106">プロパティをサポートするすべてのオブジェクトは、このインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-106">All objects that support properties implement this interface.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8a4aa-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8a4aa-107">Header file:</span></span>  <br/> |<span data-ttu-id="8a4aa-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8a4aa-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8a4aa-109">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="8a4aa-110">オブジェクトは直接このインターフェイスを公開しません。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-110">No object exposes this interface directly.</span></span>  <br/> |
|<span data-ttu-id="8a4aa-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="8a4aa-112">サービス プロバイダーおよび MAPI</span><span class="sxs-lookup"><span data-stu-id="8a4aa-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="8a4aa-113">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-113">Called by:</span></span>  <br/> |<span data-ttu-id="8a4aa-114">クライアント アプリケーション、サービス プロバイダー、および MAPI</span><span class="sxs-lookup"><span data-stu-id="8a4aa-114">Client applications, service providers, and MAPI</span></span>  <br/> |
|<span data-ttu-id="8a4aa-115">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8a4aa-116">IID_IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8a4aa-116">IID_IMAPIProp</span></span>  <br/> |
|<span data-ttu-id="8a4aa-117">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="8a4aa-118">LPMAPIPROP</span><span class="sxs-lookup"><span data-stu-id="8a4aa-118">LPMAPIPROP</span></span>  <br/> |
|<span data-ttu-id="8a4aa-119">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="8a4aa-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="8a4aa-120">抽象クラスで実装されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8a4aa-121">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="8a4aa-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8a4aa-122">発生しました</span><span class="sxs-lookup"><span data-stu-id="8a4aa-122">GetLastError</span></span>](imapiprop-getlasterror.md) <br/> |<span data-ttu-id="8a4aa-123">前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-123">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span>  <br/> |
|[<span data-ttu-id="8a4aa-124">SaveChanges</span><span class="sxs-lookup"><span data-stu-id="8a4aa-124">SaveChanges</span></span>](imapiprop-savechanges.md) <br/> |<span data-ttu-id="8a4aa-125">前回の保存操作以降は、オブジェクトに対して行われた変更を永続的になります。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-125">Makes permanent any changes that were made to an object since the last save operation.</span></span>  <br/> |
|[<span data-ttu-id="8a4aa-126">GetProps</span><span class="sxs-lookup"><span data-stu-id="8a4aa-126">GetProps</span></span>](imapiprop-getprops.md) <br/> |<span data-ttu-id="8a4aa-127">オブジェクトの 1 つまたは複数のプロパティのプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-127">Retrieves the property value of one or more properties of an object.</span></span>  <br/> |
|[<span data-ttu-id="8a4aa-128">Getproplist メソッド</span><span class="sxs-lookup"><span data-stu-id="8a4aa-128">GetPropList</span></span>](imapiprop-getproplist.md) <br/> |<span data-ttu-id="8a4aa-129">すべてのプロパティのプロパティ タグを返します。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-129">Returns property tags for all properties.</span></span>  <br/> |
|[<span data-ttu-id="8a4aa-130">OpenProperty</span><span class="sxs-lookup"><span data-stu-id="8a4aa-130">OpenProperty</span></span>](imapiprop-openproperty.md) <br/> |<span data-ttu-id="8a4aa-131">プロパティにアクセスするために使用するインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-131">Returns a pointer to an interface that can be used to access a property.</span></span>  <br/> |
|[<span data-ttu-id="8a4aa-132">SetProps</span><span class="sxs-lookup"><span data-stu-id="8a4aa-132">SetProps</span></span>](imapiprop-setprops.md) <br/> |<span data-ttu-id="8a4aa-133">1 つまたは複数のプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-133">Updates one or more properties.</span></span>  <br/> |
|[<span data-ttu-id="8a4aa-134">DeleteProps</span><span class="sxs-lookup"><span data-stu-id="8a4aa-134">DeleteProps</span></span>](imapiprop-deleteprops.md) <br/> |<span data-ttu-id="8a4aa-135">オブジェクトから 1 つまたは複数のプロパティを削除します。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-135">Deletes one or more properties from an object.</span></span>  <br/> |
|[<span data-ttu-id="8a4aa-136">CopyTo</span><span class="sxs-lookup"><span data-stu-id="8a4aa-136">CopyTo</span></span>](imapiprop-copyto.md) <br/> |<span data-ttu-id="8a4aa-137">明確に除外されたプロパティ以外のすべてのプロパティを移動またはコピーします。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-137">Copies or moves all properties, except for specifically excluded properties.</span></span>  <br/> |
|[<span data-ttu-id="8a4aa-138">CopyProps</span><span class="sxs-lookup"><span data-stu-id="8a4aa-138">CopyProps</span></span>](imapiprop-copyprops.md) <br/> |<span data-ttu-id="8a4aa-139">選択したプロパティのコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-139">Copies or moves selected properties.</span></span>  <br/> |
|[<span data-ttu-id="8a4aa-140">GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="8a4aa-140">GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md) <br/> |<span data-ttu-id="8a4aa-141">1 つまたは複数のプロパティの識別子に対応するプロパティ名を提供します。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-141">Provides the property names that correspond to one or more property identifiers.</span></span>  <br/> |
|[<span data-ttu-id="8a4aa-142">GetIDsFromNames</span><span class="sxs-lookup"><span data-stu-id="8a4aa-142">GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md) <br/> |<span data-ttu-id="8a4aa-143">1 つまたは複数のプロパティ名に対応するプロパティの識別子を提供します。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-143">Provides the property identifiers that correspond to one or more property names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a4aa-144">注釈</span><span class="sxs-lookup"><span data-stu-id="8a4aa-144">Remarks</span></span>

 <span data-ttu-id="8a4aa-145">**IMAPIProp**は、次のインターフェイスの基本インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="8a4aa-145">**IMAPIProp** is the base interface for the following interfaces:</span></span> 
  
- [<span data-ttu-id="8a4aa-146">IAttach</span><span class="sxs-lookup"><span data-stu-id="8a4aa-146">IAttach</span></span>](iattachimapiprop.md)
    
- [<span data-ttu-id="8a4aa-147">IMailUser</span><span class="sxs-lookup"><span data-stu-id="8a4aa-147">IMailUser</span></span>](imailuserimapiprop.md)
    
- [<span data-ttu-id="8a4aa-148">IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="8a4aa-148">IMAPIContainer</span></span>](imapicontainerimapiprop.md)
    
- [<span data-ttu-id="8a4aa-149">IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="8a4aa-149">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md)
    
- [<span data-ttu-id="8a4aa-150">IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="8a4aa-150">IMAPIStatus</span></span>](imapistatusimapiprop.md)
    
- [<span data-ttu-id="8a4aa-151">IMessage</span><span class="sxs-lookup"><span data-stu-id="8a4aa-151">IMessage</span></span>](imessageimapiprop.md)
    
- [<span data-ttu-id="8a4aa-152">IMsgStore</span><span class="sxs-lookup"><span data-stu-id="8a4aa-152">IMsgStore</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="8a4aa-153">IProfSect</span><span class="sxs-lookup"><span data-stu-id="8a4aa-153">IProfSect</span></span>](iprofsectimapiprop.md)
    
- [<span data-ttu-id="8a4aa-154">IPropData</span><span class="sxs-lookup"><span data-stu-id="8a4aa-154">IPropData</span></span>](ipropdataimapiprop.md)
    
## <a name="see-also"></a><span data-ttu-id="8a4aa-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="8a4aa-155">See also</span></span>



[<span data-ttu-id="8a4aa-156">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8a4aa-156">MAPI Interfaces</span></span>](mapi-interfaces.md)

