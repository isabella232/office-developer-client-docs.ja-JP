---
title: IMAPIContainerOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9598e0c90c16db14cdc3a46d2b2ae74e0d9a9300
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286933"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="95315-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="95315-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="95315-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95315-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95315-105">コンテナー内のオブジェクトを開き、さらにアクセスするためのインターフェイスポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="95315-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="95315-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="95315-106">Parameters</span></span>

 <span data-ttu-id="95315-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="95315-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="95315-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="95315-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="95315-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="95315-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="95315-110">順番開くオブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="95315-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="95315-111">_lな tryid_が NULL に設定されている場合、コンテナーの階層の最上位のコンテナーが開かれます。</span><span class="sxs-lookup"><span data-stu-id="95315-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="95315-112">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="95315-112">_lpInterface_</span></span>
  
> <span data-ttu-id="95315-113">順番オブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="95315-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="95315-114">返されるオブジェクトの標準インターフェイスの識別子に NULL 結果が渡されます。</span><span class="sxs-lookup"><span data-stu-id="95315-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="95315-115">メッセージの場合、標準インターフェイスは[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md);フォルダーの場合は、 [imapifolder: IMAPIContainer](imapifolderimapicontainer.md)になります。</span><span class="sxs-lookup"><span data-stu-id="95315-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="95315-116">アドレス帳オブジェクトの標準インターフェイスは[idistlist: IMAPIContainer](idistlistimapicontainer.md)の配布リストと[idistlist: imapiprop](imailuserimapiprop.md)がメッセージングユーザーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="95315-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="95315-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="95315-117">_ulFlags_</span></span>
  
> <span data-ttu-id="95315-118">順番オブジェクトを開く方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="95315-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="95315-119">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="95315-119">The following flags can be set:</span></span>
    
<span data-ttu-id="95315-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="95315-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="95315-121">ユーザーに対して許可される最大のネットワークアクセス許可と、クライアントアプリケーションの最大アクセス権を使用して、オブジェクトが開かれることを要求します。</span><span class="sxs-lookup"><span data-stu-id="95315-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="95315-122">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、読み取り/書き込みアクセス許可を使用してオブジェクトを開く必要があります。クライアントが読み取り専用のアクセス権を持っている場合は、オブジェクトを読み取り専用アクセスで開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="95315-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="95315-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="95315-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="95315-124">呼び出し元のクライアントがオブジェクトを完全に使用できるようになる前に、 **openentry**が正常に返されることを許可します。</span><span class="sxs-lookup"><span data-stu-id="95315-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="95315-125">オブジェクトが使用できない場合は、その後のオブジェクト呼び出しでエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="95315-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="95315-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="95315-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="95315-127">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="95315-127">Requests read/write permission.</span></span> <span data-ttu-id="95315-128">既定では、オブジェクトは読み取り専用アクセスで開かれ、読み取り/書き込みアクセス許可が与えられているという前提でクライアントを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="95315-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="95315-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="95315-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="95315-130">現在、削除済みアイテムの保存期間の段階にあるとマークされているアイテムを表示します。</span><span class="sxs-lookup"><span data-stu-id="95315-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="95315-131">_lpulobjtype_</span><span class="sxs-lookup"><span data-stu-id="95315-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="95315-132">読み上げ開かれているオブジェクトの種類へのポインター。</span><span class="sxs-lookup"><span data-stu-id="95315-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="95315-133">_lppunk_</span><span class="sxs-lookup"><span data-stu-id="95315-133">_lppUnk_</span></span>
  
> <span data-ttu-id="95315-134">読み上げ開いているオブジェクトへのアクセスに使用するインターフェイス実装へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="95315-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="95315-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="95315-135">Return value</span></span>

<span data-ttu-id="95315-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="95315-136">S_OK</span></span> 
  
> <span data-ttu-id="95315-137">オブジェクトが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="95315-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="95315-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="95315-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="95315-139">ユーザーがオブジェクトを開くための十分な権限を持っていないか、読み取り/書き込みアクセス許可を持つ読み取り専用オブジェクトを開こうとしています。</span><span class="sxs-lookup"><span data-stu-id="95315-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="95315-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="95315-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="95315-141">_lな tryid_で指定されたエントリ識別子は、オブジェクトを表していません。</span><span class="sxs-lookup"><span data-stu-id="95315-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="95315-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="95315-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="95315-143">_lな tryid_パラメーターのエントリ識別子が、コンテナーで認識される形式ではありません。</span><span class="sxs-lookup"><span data-stu-id="95315-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="95315-144">解説</span><span class="sxs-lookup"><span data-stu-id="95315-144">Remarks</span></span>

<span data-ttu-id="95315-145">**IMAPIContainer:: openentry**メソッドは、コンテナー全体でオブジェクトを開き、さらにアクセスするために使用するインターフェイス実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="95315-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="95315-146">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="95315-146">Notes to callers</span></span>

<span data-ttu-id="95315-147">_lpinterface_パラメーターのインターフェイス識別子によって指定された型のインターフェイス実装を返す必要がないため、サービスプロバイダーは_lpulobjtype_パラメーターで示されている値を確認します。</span><span class="sxs-lookup"><span data-stu-id="95315-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="95315-148">必要に応じて、 _lppunk_で返されたポインターを、適切な型のポインターにキャストします。</span><span class="sxs-lookup"><span data-stu-id="95315-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="95315-149">既定では、MAPI_MODIFY または MAPI_BEST_ACCESS フラグのどちらかを設定しない限り、サービスプロバイダーは読み取り専用アクセスでオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="95315-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="95315-150">これらのフラグのいずれかが設定されている場合、サービスプロバイダーは変更可能なオブジェクトを取得しようとします。</span><span class="sxs-lookup"><span data-stu-id="95315-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="95315-151">ただし、開いているオブジェクトが読み取り/書き込みアクセス許可を持つ変更可能なオブジェクトを要求したため、このことを前提としていません。</span><span class="sxs-lookup"><span data-stu-id="95315-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="95315-152">その後の変更が失敗するかどうかを計画するか、またはオブジェクトの**PR_ACCESS_LEVEL**プロパティを取得して、 **openentry**によって付与されるアクセスレベルを判断します。</span><span class="sxs-lookup"><span data-stu-id="95315-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="95315-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="95315-153">See also</span></span>



[<span data-ttu-id="95315-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="95315-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

