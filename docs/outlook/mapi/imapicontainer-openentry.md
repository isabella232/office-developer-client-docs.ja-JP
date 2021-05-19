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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423637"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="f4b1f-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f4b1f-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="f4b1f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4b1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4b1f-105">コンテナー内のオブジェクトを開き、さらにアクセスするインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="f4b1f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f4b1f-106">Parameters</span></span>

 <span data-ttu-id="f4b1f-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f4b1f-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f4b1f-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f4b1f-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f4b1f-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f4b1f-110">[in]開くオブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="f4b1f-111">_lpEntryID が_ NULL に設定されている場合、コンテナーの階層内のトップ レベル のコンテナーが開きます。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="f4b1f-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f4b1f-112">_lpInterface_</span></span>
  
> <span data-ttu-id="f4b1f-113">[in]オブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="f4b1f-114">NULL を渡すと、オブジェクトの標準インターフェイスの識別子が返されます。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="f4b1f-115">メッセージの場合、標準インターフェイスは [IMAPIMessageSite : IUnknown です](imapimessagesiteiunknown.md)。フォルダーの場合 [、IMAPIFolder : IMAPIContainer です](imapifolderimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="f4b1f-116">アドレス帳オブジェクトの標準インターフェイスは、配布リストの [IDistList : IMAPIContainer、](idistlistimapicontainer.md) メッセージング ユーザーの [IMailUser : IMAPIProp](imailuserimapiprop.md) です。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="f4b1f-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f4b1f-117">_ulFlags_</span></span>
  
> <span data-ttu-id="f4b1f-118">[in]オブジェクトの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="f4b1f-119">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-119">The following flags can be set:</span></span>
    
<span data-ttu-id="f4b1f-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f4b1f-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="f4b1f-121">ユーザーに許可される最大ネットワークアクセス許可と最大クライアント アプリケーション アクセス権を使用してオブジェクトを開く要求。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="f4b1f-122">たとえば、クライアントに読み取り/書き込みアクセス許可がある場合は、オブジェクトを読み取り/書き込みアクセス許可で開く必要があります。クライアントに読み取り専用アクセス権がある場合は、オブジェクトを読み取り専用アクセスで開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="f4b1f-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="f4b1f-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="f4b1f-124">オブジェクトが呼び出し元のクライアントで完全に利用できる前に **、OpenEntry** が正常に返されるのを許可します。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="f4b1f-125">オブジェクトを使用できない場合は、後続のオブジェクト呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="f4b1f-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f4b1f-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="f4b1f-127">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-127">Requests read/write permission.</span></span> <span data-ttu-id="f4b1f-128">既定では、オブジェクトは読み取り専用アクセス権で開かれません。クライアントは、読み取り/書き込みアクセス許可が付与されているという前提で動作しません。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="f4b1f-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="f4b1f-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="f4b1f-130">現在、削除済みアイテムとしてマークされているアイテム、つまり削除済みアイテムの保持時間フェーズにあるアイテムを表示します。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="f4b1f-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="f4b1f-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="f4b1f-132">[out]開いたオブジェクトの型へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="f4b1f-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="f4b1f-133">_lppUnk_</span></span>
  
> <span data-ttu-id="f4b1f-134">[out]開いているオブジェクトへのアクセスに使用するインターフェイス実装へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f4b1f-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="f4b1f-135">Return value</span></span>

<span data-ttu-id="f4b1f-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="f4b1f-136">S_OK</span></span> 
  
> <span data-ttu-id="f4b1f-137">オブジェクトが正常に開かされました。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="f4b1f-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="f4b1f-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="f4b1f-139">ユーザーがオブジェクトを開くアクセス許可が不足しているか、読み取り/書き込みアクセス許可を持つ読み取り専用オブジェクトを開く試みが行われたかのどちらかです。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="f4b1f-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f4b1f-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="f4b1f-141">_lpEntryID で指定されたエントリ識別子は_、オブジェクトを表すではありません。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="f4b1f-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f4b1f-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="f4b1f-143">_lpEntryID_ パラメーターのエントリ識別子は、コンテナーによって認識される形式ではありません。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f4b1f-144">注釈</span><span class="sxs-lookup"><span data-stu-id="f4b1f-144">Remarks</span></span>

<span data-ttu-id="f4b1f-145">**IMAPIContainer::OpenEntry** メソッドは、コンテナー全体でオブジェクトを開き、さらにアクセスするために使用するインターフェイス実装へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f4b1f-146">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f4b1f-146">Notes to callers</span></span>

<span data-ttu-id="f4b1f-147">サービス プロバイダーは  _、lpInterface_ パラメーターのインターフェイス識別子で指定された型のインターフェイス実装を返す必要はないので  _、lpulObjType_ パラメーターが指す値を確認します。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="f4b1f-148">必要に応じて  _、lppUnk_ で返されたポインターを適切な型のポインターにキャストします。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="f4b1f-149">既定では、サービス プロバイダーは、読み取り専用のアクセス権を持つオブジェクトを開きます(既定では、MAPI_MODIFYまたはMAPI_BEST_ACCESSします。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="f4b1f-150">これらのフラグの 1 つが設定されている場合、サービス プロバイダーは変更可能なオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="f4b1f-151">ただし、開いたオブジェクトが読み取り/書き込みアクセス許可を持つ変更可能なオブジェクトを要求した場合は、このオブジェクトを想定しなさる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="f4b1f-152">後続の変更が失敗する可能性を計画するか、オブジェクトの **PR_ACCESS_LEVEL** プロパティを取得して **、OpenEntry** によって付与されるアクセス レベルを決定します。</span><span class="sxs-lookup"><span data-stu-id="f4b1f-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f4b1f-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="f4b1f-153">See also</span></span>



[<span data-ttu-id="f4b1f-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f4b1f-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

