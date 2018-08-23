---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2f45028219f0f5f4cc881db3bc512626b3ad2f4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800772"
---
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="45fc3-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="45fc3-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="45fc3-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45fc3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45fc3-105">現在のプロファイルのセクションを開き、さらにアクセスするための[IProfSect](iprofsectimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="45fc3-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="45fc3-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="45fc3-106">Parameters</span></span>

 <span data-ttu-id="45fc3-107">_lpUid_</span><span class="sxs-lookup"><span data-stu-id="45fc3-107">_lpUid_</span></span>
  
> <span data-ttu-id="45fc3-108">[in]プロファイルのセクションを開くことを識別する[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="45fc3-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="45fc3-109">_LpUid_パラメーターに NULL を渡すことと、呼び出し元のプロファイル セクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="45fc3-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="45fc3-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="45fc3-110">_ulFlags_</span></span>
  
> <span data-ttu-id="45fc3-111">[in]プロファイル セクションを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="45fc3-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="45fc3-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="45fc3-112">The following flags can be set:</span></span>
    
<span data-ttu-id="45fc3-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="45fc3-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="45fc3-114">正常に完了するのには**OpenProfileSection**では、可能性のあるプロファイルする前にセクションでは、呼び出し元に完全にアクセス可能です。</span><span class="sxs-lookup"><span data-stu-id="45fc3-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="45fc3-115">プロファイル セクションがアクセスできない場合は、後続のオブジェクトの呼び出しを行うことができますと、エラーです。</span><span class="sxs-lookup"><span data-stu-id="45fc3-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="45fc3-116">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="45fc3-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="45fc3-117">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="45fc3-117">Requests read/write permission.</span></span> <span data-ttu-id="45fc3-118">既定では、オブジェクトが読み取り専用で開いているし、呼び出し元は読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="45fc3-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="45fc3-119">_lppProfileObj_</span><span class="sxs-lookup"><span data-stu-id="45fc3-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="45fc3-120">[out]開かれているプロファイル セクションへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="45fc3-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="45fc3-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="45fc3-121">Return value</span></span>

<span data-ttu-id="45fc3-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="45fc3-122">S_OK</span></span> 
  
> <span data-ttu-id="45fc3-123">プロファイル セクションが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="45fc3-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="45fc3-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="45fc3-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="45fc3-125">しようとは、読み取り専用のプロファイル セクションを変更するか、呼び出し元が十分なアクセス許可を持っているオブジェクトへのアクセスにしました。</span><span class="sxs-lookup"><span data-stu-id="45fc3-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="45fc3-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="45fc3-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="45fc3-127">_LpEntryID_に渡されたエントリの識別子に関連付けられているプロファイルのセクションではありません。</span><span class="sxs-lookup"><span data-stu-id="45fc3-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="45fc3-128">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="45fc3-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="45fc3-129">予約またはサポートされていないフラグを使用し、操作が完了しなかったため、します。</span><span class="sxs-lookup"><span data-stu-id="45fc3-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="45fc3-130">注釈</span><span class="sxs-lookup"><span data-stu-id="45fc3-130">Remarks</span></span>

<span data-ttu-id="45fc3-131">サポートのすべてのオブジェクトの**IMAPISupport::OpenProfileSection**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="45fc3-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="45fc3-132">サービス プロバイダーおよびメッセージ サービスは、プロファイルのセクションを開くし、 **IProfSect**インターフェイスの実装へのポインターを取得する**OpenProfileSection**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="45fc3-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="45fc3-133">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="45fc3-133">Notes to callers</span></span>

 <span data-ttu-id="45fc3-134">_UlFlags_パラメーターで MAPI_MODIFY フラグを設定して、アクセス許可が十分でない限り、 **OpenProfileSection**は読み取り専用のプロファイル セクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="45fc3-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="45fc3-135">このフラグを設定した場合、読み取り/書き込みアクセス許可は保証されません。付与されたアクセス許可は、現在のアクセス権とオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="45fc3-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="45fc3-136">**OpenProfileSection**は、読み取り専用で存在しないプロファイル セクションを開こうとすると、MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="45fc3-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="45fc3-137">場合は**OpenProfileSection**は、読み取り/書き込みとして存在しないプロファイル セクションを開こうとすると、プロファイルのセクションを作成し、 **IProfSect**ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="45fc3-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="45fc3-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="45fc3-138">See also</span></span>



[<span data-ttu-id="45fc3-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="45fc3-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="45fc3-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="45fc3-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="45fc3-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="45fc3-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="45fc3-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="45fc3-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

