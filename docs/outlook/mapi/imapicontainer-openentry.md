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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c13ab9ce9c2564c39bfe9b2689f05439bc7b74ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800445"
---
# <a name="imapicontaineropenentry"></a><span data-ttu-id="29d80-103">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="29d80-103">IMAPIContainer::OpenEntry</span></span>

  
  
<span data-ttu-id="29d80-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="29d80-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="29d80-105">コンテナーで、さらにアクセスするためのインターフェイス ポインターを返すには、オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="29d80-105">Opens an object in the container, returning an interface pointer for further access.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="29d80-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="29d80-106">Parameters</span></span>

 <span data-ttu-id="29d80-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="29d80-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="29d80-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="29d80-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="29d80-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="29d80-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="29d80-110">[in]開くにはオブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="29d80-110">[in] A pointer to the entry identifier of the object to open.</span></span> <span data-ttu-id="29d80-111">_LpEntryID_は、NULL に設定されている場合は、コンテナーの階層の最上位のコンテナーが開かれます。</span><span class="sxs-lookup"><span data-stu-id="29d80-111">If  _lpEntryID_ is set to NULL, the top-level container in the container's hierarchy is opened.</span></span> 
    
 <span data-ttu-id="29d80-112">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="29d80-112">_lpInterface_</span></span>
  
> <span data-ttu-id="29d80-113">[in]オブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="29d80-113">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="29d80-114">パラメーターに NULL が返されるオブジェクトの標準的なインタ フェースの識別子で発生します。</span><span class="sxs-lookup"><span data-stu-id="29d80-114">Passing NULL results in the identifier for the object's standard interface being returned.</span></span> <span data-ttu-id="29d80-115">標準的なインタ フェースは、メッセージは、 [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)です。フォルダーの[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="29d80-115">For messages, the standard interface is [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); for folders, it is [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="29d80-116">標準インターフェイスを使用しているアドレス帳オブジェクト[IDistList: IMAPIContainer](idistlistimapicontainer.md)の配布リストと[IMailUser: IMAPIProp](imailuserimapiprop.md)メッセージング ユーザーのです。</span><span class="sxs-lookup"><span data-stu-id="29d80-116">The standard interfaces for address book objects are [IDistList : IMAPIContainer](idistlistimapicontainer.md) for a distribution list and [IMailUser : IMAPIProp](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="29d80-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="29d80-117">_ulFlags_</span></span>
  
> <span data-ttu-id="29d80-118">[in]オブジェクトを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="29d80-118">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="29d80-119">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="29d80-119">The following flags can be set:</span></span>
    
<span data-ttu-id="29d80-120">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="29d80-120">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="29d80-121">ユーザーおよび最大のクライアント アプリケーションへのアクセスに使用される最大ネットワークのアクセス許可を持つオブジェクトが開かれますことを要求します。</span><span class="sxs-lookup"><span data-stu-id="29d80-121">Requests that the object will be opened with the maximum network permissions allowed for the user and the maximum client application access.</span></span> <span data-ttu-id="29d80-122">たとえば、クライアントに読み取り/書き込み権限がある場合、オブジェクト開く必要があります読み取り/書き込みアクセス許可を持つクライアントに読み取り専用アクセスがある場合は、読み取り専用アクセス権を持つオブジェクトを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="29d80-122">For example, if the client has read/write permission, the object should be opened with read/write permission; if the client has read-only access, the object should be opened with read-only access.</span></span> 
    
<span data-ttu-id="29d80-123">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="29d80-123">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="29d80-124">**OpenEntry**を正常に戻す、可能性のあるオブジェクトが呼び出し元のクライアントに完全に利用できる前にするにを使用できます。</span><span class="sxs-lookup"><span data-stu-id="29d80-124">Allows **OpenEntry** to return successfully, possibly before the object is fully available to the calling client.</span></span> <span data-ttu-id="29d80-125">オブジェクトが使用できない場合は、後続のオブジェクトの呼び出しを行うとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="29d80-125">If the object is not available, making a subsequent object call can raise an error.</span></span> 
    
<span data-ttu-id="29d80-126">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="29d80-126">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="29d80-127">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="29d80-127">Requests read/write permission.</span></span> <span data-ttu-id="29d80-128">既定では、読み取り専用のアクセス権を持つオブジェクトが開いているし、クライアントが読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="29d80-128">By default, objects are opened with read-only access, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="29d80-129">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="29d80-129">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="29d80-130">ソフトとしてマークされているアイテムの削除を示しています-は削除済みアイテムの保存に時間の段階です。</span><span class="sxs-lookup"><span data-stu-id="29d80-130">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="29d80-131">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="29d80-131">_lpulObjType_</span></span>
  
> <span data-ttu-id="29d80-132">[out]開かれているオブジェクトの型へのポインター。</span><span class="sxs-lookup"><span data-stu-id="29d80-132">[out] A pointer to the opened object's type.</span></span>
    
 <span data-ttu-id="29d80-133">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="29d80-133">_lppUnk_</span></span>
  
> <span data-ttu-id="29d80-134">[out]開いているオブジェクトへのアクセスに使用するインターフェイスの実装へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="29d80-134">[out] A pointer to a pointer to the interface implementation to use to access the open object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="29d80-135">�߂�l</span><span class="sxs-lookup"><span data-stu-id="29d80-135">Return value</span></span>

<span data-ttu-id="29d80-136">S_OK</span><span class="sxs-lookup"><span data-stu-id="29d80-136">S_OK</span></span> 
  
> <span data-ttu-id="29d80-137">オブジェクトが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="29d80-137">The object was successfully opened.</span></span>
    
<span data-ttu-id="29d80-138">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="29d80-138">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="29d80-139">ユーザーがオブジェクトを開くに十分なアクセス許可を持っているか、読み取り/書き込みアクセス許可を持つ読み取り専用オブジェクトを開くしようとしました。</span><span class="sxs-lookup"><span data-stu-id="29d80-139">Either the user has insufficient permissions to open the object or an attempt was made to open a read-only object with read/write permission.</span></span>
    
<span data-ttu-id="29d80-140">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="29d80-140">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="29d80-141">_LpEntryID_で指定されたエントリの識別子は、オブジェクトを表していません。</span><span class="sxs-lookup"><span data-stu-id="29d80-141">The entry identifier specified by  _lpEntryID_ does not represent an object.</span></span> 
    
<span data-ttu-id="29d80-142">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="29d80-142">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="29d80-143">_LpEntryID_パラメーターのエントリの識別子は、コンテナーによって認識される形式のではありません。</span><span class="sxs-lookup"><span data-stu-id="29d80-143">The entry identifier in the  _lpEntryID_ parameter is not of a format recognized by the container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="29d80-144">注釈</span><span class="sxs-lookup"><span data-stu-id="29d80-144">Remarks</span></span>

<span data-ttu-id="29d80-145">**IMAPIContainer::OpenEntry**メソッドは、コンテナー全体にわたってオブジェクトを開き、さらにアクセスに使用するインターフェイスの実装にポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="29d80-145">The **IMAPIContainer::OpenEntry** method opens an object throughout a container and returns a pointer to an interface implementation to use for further access.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="29d80-146">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="29d80-146">Notes to callers</span></span>

<span data-ttu-id="29d80-147">サービス プロバイダーが、 _lpInterface_パラメーターにインターフェイス識別子で指定された型のインターフェイスの実装を取得する必要がないために、 _lpulObjType_パラメーターで指定された値を確認します。</span><span class="sxs-lookup"><span data-stu-id="29d80-147">Because service providers are not required to return an interface implementation of the type specified by the interface identifier in the  _lpInterface_ parameter, check the value pointed to by the  _lpulObjType_ parameter.</span></span> <span data-ttu-id="29d80-148">必要に応じて、適切な型のポインターに_lppUnk_で返されたポインターにキャストします。</span><span class="sxs-lookup"><span data-stu-id="29d80-148">If necessary, cast the pointer returned in  _lppUnk_ to a pointer of the appropriate type.</span></span> 
  
<span data-ttu-id="29d80-149">既定では、サービス ・ プロバイダーは MAPI_MODIFY または MAPI_BEST_ACCESS のいずれかのフラグを設定する場合を除き、読み取り専用アクセス権を持つオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="29d80-149">By default, service providers open objects with read-only access unless you set either the MAPI_MODIFY or MAPI_BEST_ACCESS flag.</span></span> <span data-ttu-id="29d80-150">これらのフラグのいずれかを設定すると、サービス ・ プロバイダーは変更可能なオブジェクトを取得しようとします。</span><span class="sxs-lookup"><span data-stu-id="29d80-150">When one of these flags is set, service providers attempt to return a modifiable object.</span></span> <span data-ttu-id="29d80-151">ただし、限りませんを変更可能なオブジェクトが開かれているオブジェクトが読み取り/書き込みアクセス許可を要求しました。</span><span class="sxs-lookup"><span data-stu-id="29d80-151">However, do not assume that because you requested a modifiable object that the opened object has read/write permission.</span></span> <span data-ttu-id="29d80-152">どちらか**OpenEntry**によって付与されたアクセス レベルを決定するのにはエラーが発生したり、オブジェクトの**PR_ACCESS_LEVEL**プロパティを取得後に変更されたことを計画します。</span><span class="sxs-lookup"><span data-stu-id="29d80-152">Either plan for the chance of a subsequent modification to fail or retrieve the object's **PR_ACCESS_LEVEL** property to determine the access level granted by **OpenEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="29d80-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="29d80-153">See also</span></span>



[<span data-ttu-id="29d80-154">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="29d80-154">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)

