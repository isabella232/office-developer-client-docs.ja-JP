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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e7f13acc34a77b79057d32fd4049db7222dadf49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411387"
---
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="ee679-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="ee679-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="ee679-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee679-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee679-105">現在のプロファイルのセクションを開き、さらにアクセスできるように[IProfSect](iprofsectimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="ee679-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="ee679-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ee679-106">Parameters</span></span>

 <span data-ttu-id="ee679-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="ee679-107">_lpUid_</span></span>
  
> <span data-ttu-id="ee679-108">順番開くプロファイルセクションを識別する[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ee679-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="ee679-109">_lpuid_パラメーターに NULL を渡すと、呼び出し元のプロファイルセクションが開きます。</span><span class="sxs-lookup"><span data-stu-id="ee679-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="ee679-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee679-110">_ulFlags_</span></span>
  
> <span data-ttu-id="ee679-111">順番プロファイルセクションが開かれる方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ee679-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="ee679-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ee679-112">The following flags can be set:</span></span>
    
<span data-ttu-id="ee679-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ee679-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ee679-114">呼び出し\*\*\*\* 元がプロファイルセクションに完全にアクセスできるようになる前に、openプロファイルを正常に返すことができるようにします。</span><span class="sxs-lookup"><span data-stu-id="ee679-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="ee679-115">プロファイルセクションにアクセスできない場合は、次のオブジェクト呼び出しを行うとエラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="ee679-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="ee679-116">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="ee679-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="ee679-117">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="ee679-117">Requests read/write permission.</span></span> <span data-ttu-id="ee679-118">既定では、オブジェクトは読み取り専用として開かれ、読み取り/書き込みアクセス許可が付与されているという前提で呼び出し元は機能しません。</span><span class="sxs-lookup"><span data-stu-id="ee679-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="ee679-119">_lppprofileobj_</span><span class="sxs-lookup"><span data-stu-id="ee679-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="ee679-120">読み上げ開いているプロファイルセクションへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ee679-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ee679-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="ee679-121">Return value</span></span>

<span data-ttu-id="ee679-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee679-122">S_OK</span></span> 
  
> <span data-ttu-id="ee679-123">プロファイルセクションが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="ee679-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="ee679-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ee679-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ee679-125">読み取り専用プロファイルセクションを変更しようとしたか、呼び出し元が十分なアクセス許可を持っていないオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="ee679-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="ee679-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ee679-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ee679-127">_lな tryid_で渡されるエントリ識別子に関連付けられているプロファイルセクションはありません。</span><span class="sxs-lookup"><span data-stu-id="ee679-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="ee679-128">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="ee679-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="ee679-129">予約済みまたは未サポートのフラグが使用されたため、操作が完了しませんでした。</span><span class="sxs-lookup"><span data-stu-id="ee679-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee679-130">注釈</span><span class="sxs-lookup"><span data-stu-id="ee679-130">Remarks</span></span>

<span data-ttu-id="ee679-131">**imapisupport:: openプロファイル**のメソッドは、すべてのサポートオブジェクトに実装されています。</span><span class="sxs-lookup"><span data-stu-id="ee679-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="ee679-132">サービスプロバイダおよびメッセージサービスは\*\*\*\* 、openprofile を呼び出して、プロファイルセクションを開き、その**IProfSect**インターフェイス実装へのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="ee679-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ee679-133">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ee679-133">Notes to callers</span></span>

 <span data-ttu-id="ee679-134">**openprofile**の場合は、MAPI_MODIFY フラグを_ulflags_パラメーターに設定し、アクセス許可で十分でなければ、プロファイルセクションを読み取り専用として開きます。</span><span class="sxs-lookup"><span data-stu-id="ee679-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="ee679-135">このフラグを設定しても、読み取り/書き込みアクセス許可は保証されません。付与されるアクセス許可は、アクセスレベルとオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="ee679-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="ee679-136">**openprofile**が、存在しないプロファイルセクションを読み取り専用として開こうとした場合は、MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="ee679-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="ee679-137">**openprofile**が、存在しないプロファイルセクションを読み取り/書き込みとして開こうとした場合、プロファイルセクションを作成し、 **IProfSect**ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="ee679-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee679-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="ee679-138">See also</span></span>



[<span data-ttu-id="ee679-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee679-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="ee679-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ee679-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="ee679-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ee679-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ee679-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee679-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

