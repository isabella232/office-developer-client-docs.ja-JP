---
title: imapiprop IUnknown
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
ms.openlocfilehash: 6b0a8923ee5efe22584170ce9853698885527ee8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282472"
---
# <a name="imapiprop--iunknown"></a><span data-ttu-id="2abed-103">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2abed-103">IMAPIProp : IUnknown</span></span>

  
  
<span data-ttu-id="2abed-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2abed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2abed-105">クライアント、サービスプロバイダ、MAPI がプロパティを使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="2abed-105">Enables clients, service providers, and MAPI to work with properties.</span></span> <span data-ttu-id="2abed-106">プロパティをサポートするすべてのオブジェクトは、このインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="2abed-106">All objects that support properties implement this interface.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2abed-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2abed-107">Header file:</span></span>  <br/> |<span data-ttu-id="2abed-108">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2abed-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2abed-109">公開者:</span><span class="sxs-lookup"><span data-stu-id="2abed-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="2abed-110">このインターフェイスを直接公開するオブジェクトはありません。</span><span class="sxs-lookup"><span data-stu-id="2abed-110">No object exposes this interface directly.</span></span>  <br/> |
|<span data-ttu-id="2abed-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="2abed-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="2abed-112">サービスプロバイダーと MAPI</span><span class="sxs-lookup"><span data-stu-id="2abed-112">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="2abed-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="2abed-113">Called by:</span></span>  <br/> |<span data-ttu-id="2abed-114">クライアントアプリケーション、サービスプロバイダー、MAPI</span><span class="sxs-lookup"><span data-stu-id="2abed-114">Client applications, service providers, and MAPI</span></span>  <br/> |
|<span data-ttu-id="2abed-115">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="2abed-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2abed-116">IID_IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2abed-116">IID_IMAPIProp</span></span>  <br/> |
|<span data-ttu-id="2abed-117">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="2abed-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="2abed-118">LPMAPIPROP</span><span class="sxs-lookup"><span data-stu-id="2abed-118">LPMAPIPROP</span></span>  <br/> |
|<span data-ttu-id="2abed-119">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="2abed-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="2abed-120">抽象クラス、実装されていません</span><span class="sxs-lookup"><span data-stu-id="2abed-120">Abstract class, never implemented</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2abed-121">v の順序</span><span class="sxs-lookup"><span data-stu-id="2abed-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2abed-122">GetLastError</span><span class="sxs-lookup"><span data-stu-id="2abed-122">GetLastError</span></span>](imapiprop-getlasterror.md) <br/> |<span data-ttu-id="2abed-123">前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="2abed-123">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span>  <br/> |
|[<span data-ttu-id="2abed-124">SaveChanges</span><span class="sxs-lookup"><span data-stu-id="2abed-124">SaveChanges</span></span>](imapiprop-savechanges.md) <br/> |<span data-ttu-id="2abed-125">前回の保存操作以降にオブジェクトに加えられたすべての変更を永続的に行います。</span><span class="sxs-lookup"><span data-stu-id="2abed-125">Makes permanent any changes that were made to an object since the last save operation.</span></span>  <br/> |
|[<span data-ttu-id="2abed-126">GetProps</span><span class="sxs-lookup"><span data-stu-id="2abed-126">GetProps</span></span>](imapiprop-getprops.md) <br/> |<span data-ttu-id="2abed-127">オブジェクトの1つ以上のプロパティのプロパティ値を取得します。</span><span class="sxs-lookup"><span data-stu-id="2abed-127">Retrieves the property value of one or more properties of an object.</span></span>  <br/> |
|[<span data-ttu-id="2abed-128">getproplist</span><span class="sxs-lookup"><span data-stu-id="2abed-128">GetPropList</span></span>](imapiprop-getproplist.md) <br/> |<span data-ttu-id="2abed-129">すべてのプロパティのプロパティタグを返します。</span><span class="sxs-lookup"><span data-stu-id="2abed-129">Returns property tags for all properties.</span></span>  <br/> |
|[<span data-ttu-id="2abed-130">openproperty</span><span class="sxs-lookup"><span data-stu-id="2abed-130">OpenProperty</span></span>](imapiprop-openproperty.md) <br/> |<span data-ttu-id="2abed-131">プロパティへのアクセスに使用できるインターフェイスへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="2abed-131">Returns a pointer to an interface that can be used to access a property.</span></span>  <br/> |
|[<span data-ttu-id="2abed-132">setprops による</span><span class="sxs-lookup"><span data-stu-id="2abed-132">SetProps</span></span>](imapiprop-setprops.md) <br/> |<span data-ttu-id="2abed-133">1つまたは複数のプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="2abed-133">Updates one or more properties.</span></span>  <br/> |
|[<span data-ttu-id="2abed-134">deleteprops</span><span class="sxs-lookup"><span data-stu-id="2abed-134">DeleteProps</span></span>](imapiprop-deleteprops.md) <br/> |<span data-ttu-id="2abed-135">オブジェクトから1つ以上のプロパティを削除します。</span><span class="sxs-lookup"><span data-stu-id="2abed-135">Deletes one or more properties from an object.</span></span>  <br/> |
|[<span data-ttu-id="2abed-136">CopyTo</span><span class="sxs-lookup"><span data-stu-id="2abed-136">CopyTo</span></span>](imapiprop-copyto.md) <br/> |<span data-ttu-id="2abed-137">明示的に除外されているプロパティ以外のすべてのプロパティをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="2abed-137">Copies or moves all properties, except for specifically excluded properties.</span></span>  <br/> |
|[<span data-ttu-id="2abed-138">copyprops</span><span class="sxs-lookup"><span data-stu-id="2abed-138">CopyProps</span></span>](imapiprop-copyprops.md) <br/> |<span data-ttu-id="2abed-139">選択されたプロパティをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="2abed-139">Copies or moves selected properties.</span></span>  <br/> |
|[<span data-ttu-id="2abed-140">GetNamesFromIDs</span><span class="sxs-lookup"><span data-stu-id="2abed-140">GetNamesFromIDs</span></span>](imapiprop-getnamesfromids.md) <br/> |<span data-ttu-id="2abed-141">1つまたは複数のプロパティ識別子に対応するプロパティ名を提供します。</span><span class="sxs-lookup"><span data-stu-id="2abed-141">Provides the property names that correspond to one or more property identifiers.</span></span>  <br/> |
|[<span data-ttu-id="2abed-142">getidsfromnames</span><span class="sxs-lookup"><span data-stu-id="2abed-142">GetIDsFromNames</span></span>](imapiprop-getidsfromnames.md) <br/> |<span data-ttu-id="2abed-143">1つまたは複数のプロパティ名に対応するプロパティ識別子を提供します。</span><span class="sxs-lookup"><span data-stu-id="2abed-143">Provides the property identifiers that correspond to one or more property names.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2abed-144">解説</span><span class="sxs-lookup"><span data-stu-id="2abed-144">Remarks</span></span>

 <span data-ttu-id="2abed-145">**imapiprop**は、次のインターフェイスの基本インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="2abed-145">**IMAPIProp** is the base interface for the following interfaces:</span></span> 
  
- [<span data-ttu-id="2abed-146">iattach</span><span class="sxs-lookup"><span data-stu-id="2abed-146">IAttach</span></span>](iattachimapiprop.md)
    
- [<span data-ttu-id="2abed-147">imailuser</span><span class="sxs-lookup"><span data-stu-id="2abed-147">IMailUser</span></span>](imailuserimapiprop.md)
    
- [<span data-ttu-id="2abed-148">IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="2abed-148">IMAPIContainer</span></span>](imapicontainerimapiprop.md)
    
- [<span data-ttu-id="2abed-149">imapiforminfo</span><span class="sxs-lookup"><span data-stu-id="2abed-149">IMAPIFormInfo</span></span>](imapiforminfoimapiprop.md)
    
- [<span data-ttu-id="2abed-150">IMAPIStatus</span><span class="sxs-lookup"><span data-stu-id="2abed-150">IMAPIStatus</span></span>](imapistatusimapiprop.md)
    
- [<span data-ttu-id="2abed-151">IMessage</span><span class="sxs-lookup"><span data-stu-id="2abed-151">IMessage</span></span>](imessageimapiprop.md)
    
- [<span data-ttu-id="2abed-152">IMsgStore</span><span class="sxs-lookup"><span data-stu-id="2abed-152">IMsgStore</span></span>](imsgstoreimapiprop.md)
    
- [<span data-ttu-id="2abed-153">IProfSect</span><span class="sxs-lookup"><span data-stu-id="2abed-153">IProfSect</span></span>](iprofsectimapiprop.md)
    
- [<span data-ttu-id="2abed-154">ipropdata</span><span class="sxs-lookup"><span data-stu-id="2abed-154">IPropData</span></span>](ipropdataimapiprop.md)
    
## <a name="see-also"></a><span data-ttu-id="2abed-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="2abed-155">See also</span></span>



[<span data-ttu-id="2abed-156">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="2abed-156">MAPI Interfaces</span></span>](mapi-interfaces.md)

