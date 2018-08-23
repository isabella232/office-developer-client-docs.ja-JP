---
title: IMAPISupportOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8b122c98715bd2f6916fe6302fc0b7a01d2cc936
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584612"
---
# <a name="imapisupportopenentry"></a><span data-ttu-id="185d4-103">IMAPISupport::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="185d4-103">IMAPISupport::OpenEntry</span></span>

  
  
<span data-ttu-id="185d4-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="185d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="185d4-105">オブジェクトを開き、さらにアクセスするためのインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="185d4-105">Opens an object and returns an interface pointer for further access.</span></span> 
  
```cpp
HRESULT OpenEntry(
ULONG cbEntryID,
LPENTRYID lpEntryID,
LPCIID lpInterface,
ULONG ulOpenFlags,
ULONG FAR * lpulObjType,
LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a><span data-ttu-id="185d4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="185d4-106">Parameters</span></span>

 <span data-ttu-id="185d4-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="185d4-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="185d4-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="185d4-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="185d4-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="185d4-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="185d4-110">[in]開くにはオブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="185d4-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    
 <span data-ttu-id="185d4-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="185d4-111">_lpInterface_</span></span>
  
> <span data-ttu-id="185d4-112">[in]オブジェクトへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="185d4-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the object.</span></span> <span data-ttu-id="185d4-113">パラメーターに NULL が返されるオブジェクトの標準的なインタ フェースで発生します。</span><span class="sxs-lookup"><span data-stu-id="185d4-113">Passing NULL results in the object's standard interface being returned.</span></span> <span data-ttu-id="185d4-114">などのオブジェクトを開くことができませんが、メッセージの場合は、標準のインタ フェースは、 [IMessage](imessageimapiprop.md)です。フォルダー、 [IMAPIFolder](imapifolderimapicontainer.md)です。</span><span class="sxs-lookup"><span data-stu-id="185d4-114">For example, if the object to be opened is a message, the standard interface is [IMessage](imessageimapiprop.md); for folders, it is [IMAPIFolder](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="185d4-115">アドレス帳オブジェクトの標準的なインターフェイスは、配布リストおよび[IMailUser](imailuserimapiprop.md)のメッセージング ユーザーの[IDistList](idistlistimapicontainer.md)です。</span><span class="sxs-lookup"><span data-stu-id="185d4-115">The standard interfaces for address book objects are [IDistList](idistlistimapicontainer.md) for a distribution list and [IMailUser](imailuserimapiprop.md) for a messaging user.</span></span> 
    
 <span data-ttu-id="185d4-116">_ulOpenFlags_</span><span class="sxs-lookup"><span data-stu-id="185d4-116">_ulOpenFlags_</span></span>
  
> <span data-ttu-id="185d4-117">[in]オブジェクトを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="185d4-117">[in] A bitmask of flags that controls how the object is opened.</span></span> <span data-ttu-id="185d4-118">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="185d4-118">The following flags can be set:</span></span>
    
<span data-ttu-id="185d4-119">MAPI_BEST_ACCESS</span><span class="sxs-lookup"><span data-stu-id="185d4-119">MAPI_BEST_ACCESS</span></span> 
  
> <span data-ttu-id="185d4-120">呼び出し元で使用できる最大のネットワーク アクセス許可を持つオブジェクトを開くことを要求します。</span><span class="sxs-lookup"><span data-stu-id="185d4-120">Requests that the object be opened with the maximum network permissions allowed for the caller.</span></span> <span data-ttu-id="185d4-121">たとえば、呼び出し元に読み取り/書き込み権限がある場合は、オブジェクトで開いてください読み取り/書き込み。呼び出し元に読み取り専用のアクセス許可が設定されている場合は、読み取り専用で、オブジェクトを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="185d4-121">For example, if the caller has read/write permission, the object should be opened as read/write; if the caller has read-only permission, the object should be opened as read-only.</span></span> 
    
<span data-ttu-id="185d4-122">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="185d4-122">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="185d4-123">**OpenEntry**を正常に完了、可能性のあるオブジェクトが呼び出し元に完全にアクセス可能にするを使用できます。</span><span class="sxs-lookup"><span data-stu-id="185d4-123">Allows **OpenEntry** to return successfully, possibly before the object is fully accessible to the caller.</span></span> <span data-ttu-id="185d4-124">オブジェクトがアクセスできない場合は、後続のオブジェクトの呼び出しを行うことができますと、エラーです。</span><span class="sxs-lookup"><span data-stu-id="185d4-124">If the object is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="185d4-125">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="185d4-125">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="185d4-126">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="185d4-126">Requests read/write permission.</span></span> <span data-ttu-id="185d4-127">既定では、オブジェクトが読み取り専用で開いているし、呼び出し元は読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="185d4-127">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="185d4-128">_lpulObjType_</span><span class="sxs-lookup"><span data-stu-id="185d4-128">_lpulObjType_</span></span>
  
> <span data-ttu-id="185d4-129">[out]開かれたオブジェクトの型へのポインター。</span><span class="sxs-lookup"><span data-stu-id="185d4-129">[out] A pointer to the type of the opened object.</span></span>
    
 <span data-ttu-id="185d4-130">_lppUnk_</span><span class="sxs-lookup"><span data-stu-id="185d4-130">_lppUnk_</span></span>
  
> <span data-ttu-id="185d4-131">[out]開かれたオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="185d4-131">[out] A pointer to a pointer to the opened object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="185d4-132">�߂�l</span><span class="sxs-lookup"><span data-stu-id="185d4-132">Return value</span></span>

<span data-ttu-id="185d4-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="185d4-133">S_OK</span></span> 
  
> <span data-ttu-id="185d4-134">オブジェクトが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="185d4-134">The object was successfully opened.</span></span>
    
<span data-ttu-id="185d4-135">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="185d4-135">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="185d4-136">読み取り専用オブジェクトを変更しようとしましたまたは、ユーザーが十分なアクセス許可を持っているオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="185d4-136">An attempt was made to modify a read-only object, or an attempt was made to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="185d4-137">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="185d4-137">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="185d4-138">_LpEntryID_パラメーターで渡されたエントリの識別子に関連付けられているオブジェクトではありません。</span><span class="sxs-lookup"><span data-stu-id="185d4-138">There is not an object associated with the entry identifier passed in the  _lpEntryID_ parameter.</span></span> 
    
<span data-ttu-id="185d4-139">MAPI_E_UNKNOWN_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="185d4-139">MAPI_E_UNKNOWN_ENTRYID</span></span> 
  
> <span data-ttu-id="185d4-140">_LpEntryID_パラメーターで渡されたエントリ id が、認識できない形式です。</span><span class="sxs-lookup"><span data-stu-id="185d4-140">The entry identifier passed in the  _lpEntryID_ parameter is in an unrecognizable format.</span></span> <span data-ttu-id="185d4-141">この値は通常、オブジェクトが含まれるアドレス帳プロバイダーが開いていない場合に返されます。</span><span class="sxs-lookup"><span data-stu-id="185d4-141">This value is typically returned if the address book provider that contains the object is not open.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="185d4-142">注釈</span><span class="sxs-lookup"><span data-stu-id="185d4-142">Remarks</span></span>

<span data-ttu-id="185d4-143">サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::OpenEntry**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="185d4-143">The **IMAPISupport::OpenEntry** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="185d4-144">サービス プロバイダーは、特定のオブジェクトへのアクセスに使用できるインターフェイスへのポインターを取得するために**IMAPISupport::OpenEntry**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="185d4-144">Service providers call **IMAPISupport::OpenEntry** to retrieve a pointer to an interface that can be used to access a particular object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="185d4-145">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="185d4-145">Notes to callers</span></span>

<span data-ttu-id="185d4-146">開いているオブジェクトの種類がわからない場合にのみ、 **IMAPISupport::OpenEntry**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="185d4-146">Call **IMAPISupport::OpenEntry** only when you do not know what kind of object you are opening.</span></span> <span data-ttu-id="185d4-147">フォルダーまたはメッセージを開くことがわかっている場合は、代わりに[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="185d4-147">If you know you are opening a folder or a message, call [IMsgStore::OpenEntry](imsgstore-openentry.md) instead.</span></span> <span data-ttu-id="185d4-148">アドレス帳コンテナーである、メッセージング ユーザー、または配布リストを開くことがわかっている場合は、[アドレス帳コンテナー](iaddrbook-openentry.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="185d4-148">If you know you are opening an address book container, a messaging user, or a distribution list, call [IAddrBook::OpenEntry](iaddrbook-openentry.md).</span></span> <span data-ttu-id="185d4-149">これらの具体的な方法は、 **IMAPISupport::OpenEntry**よりも高速です。</span><span class="sxs-lookup"><span data-stu-id="185d4-149">These more specific methods are faster than **IMAPISupport::OpenEntry**.</span></span> 
  
 <span data-ttu-id="185d4-150">_UlFlags_パラメーターで、MAPI_MODIFY フラグまたは MAPI_BEST_ACCESS フラグを設定して、アクセス許可が十分でない限り、 **IMAPISupport::OpenEntry**は読み取り専用で、すべてのオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="185d4-150">**IMAPISupport::OpenEntry** opens all objects as read-only, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter and your permissions are sufficient.</span></span> <span data-ttu-id="185d4-151">これらのフラグのいずれかを設定では特定の種類のアクセスは保証されません。付与されたアクセス許可は、ユーザーのアクセス レベル、オブジェクト、およびオブジェクトを所有しているサービス プロバイダーによって異なります。</span><span class="sxs-lookup"><span data-stu-id="185d4-151">Setting one of these flags does not guarantee a particular type of access; the permissions that you are granted depend on your access level, the object, and the service provider that owns the object.</span></span> <span data-ttu-id="185d4-152">開かれたオブジェクトのアクセス レベルを決定するのには、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="185d4-152">To determine the access level of the opened object, retrieve its **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="185d4-153">返されるオブジェクトの種類では何が必要と判断するのには_lpulObjType_パラメーターで返される値を確認してください。</span><span class="sxs-lookup"><span data-stu-id="185d4-153">Check the value returned in the  _lpulObjType_ parameter to determine that the object type returned is what you expected.</span></span> <span data-ttu-id="185d4-154">オブジェクトの型が予期したとおりの場合は、 _lppUnk_パラメーターの適切な型のポインターへのポインターにキャストします。</span><span class="sxs-lookup"><span data-stu-id="185d4-154">If the object type is as expected, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type.</span></span> <span data-ttu-id="185d4-155">などのフォルダーを開いている場合は、LPMAPIFOLDER の型のポインターに_lppUnk_をキャストします。</span><span class="sxs-lookup"><span data-stu-id="185d4-155">For example, if you are opening a folder, cast  _lppUnk_ to a pointer of type LPMAPIFOLDER.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="185d4-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="185d4-156">See also</span></span>



[<span data-ttu-id="185d4-157">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="185d4-157">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

