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
# <a name="imapisupportopenprofilesection"></a><span data-ttu-id="2b634-103">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="2b634-103">IMAPISupport::OpenProfileSection</span></span>

  
  
<span data-ttu-id="2b634-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b634-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b634-105">現在のプロファイルのセクションを開き、さらにアクセスする [IProfSect](iprofsectimapiprop.md) ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="2b634-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a><span data-ttu-id="2b634-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2b634-106">Parameters</span></span>

 <span data-ttu-id="2b634-107">_lpUid_</span><span class="sxs-lookup"><span data-stu-id="2b634-107">_lpUid_</span></span>
  
> <span data-ttu-id="2b634-108">[in]開くプロファイル [セクションを識別する MAPIUID](mapiuid.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2b634-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section to be opened.</span></span> <span data-ttu-id="2b634-109">_lpUid_ パラメーターに NULL を渡すと、呼び出し元のプロファイル セクションが開きます。</span><span class="sxs-lookup"><span data-stu-id="2b634-109">Passing NULL for the  _lpUid_ parameter opens the caller's profile section.</span></span> 
    
 <span data-ttu-id="2b634-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2b634-110">_ulFlags_</span></span>
  
> <span data-ttu-id="2b634-111">[in]プロファイル セクションの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="2b634-111">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="2b634-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2b634-112">The following flags can be set:</span></span>
    
<span data-ttu-id="2b634-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="2b634-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="2b634-114">**OpenProfileSection は**、プロファイル セクションが呼び出し元から完全にアクセスできる前に、正常に戻ります。</span><span class="sxs-lookup"><span data-stu-id="2b634-114">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully accessible to the caller.</span></span> <span data-ttu-id="2b634-115">プロファイル セクションにアクセスできない場合は、後続のオブジェクト呼び出しを実行すると、エラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2b634-115">If the profile section is not accessible, making a subsequent object call can result in an error.</span></span> 
    
<span data-ttu-id="2b634-116">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="2b634-116">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="2b634-117">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="2b634-117">Requests read/write permission.</span></span> <span data-ttu-id="2b634-118">既定では、オブジェクトは読み取り専用として開かれません。呼び出し元は、読み取り/書き込みアクセス許可が付与されているという前提では動作しません。</span><span class="sxs-lookup"><span data-stu-id="2b634-118">By default, objects are opened as read-only, and callers should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="2b634-119">_lppProfileObj_</span><span class="sxs-lookup"><span data-stu-id="2b634-119">_lppProfileObj_</span></span>
  
> <span data-ttu-id="2b634-120">[out]開いたプロファイル セクションへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="2b634-120">[out] A pointer to a pointer to the opened profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2b634-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="2b634-121">Return value</span></span>

<span data-ttu-id="2b634-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="2b634-122">S_OK</span></span> 
  
> <span data-ttu-id="2b634-123">プロファイル セクションが正常に開かされました。</span><span class="sxs-lookup"><span data-stu-id="2b634-123">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="2b634-124">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="2b634-124">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="2b634-125">読み取り専用のプロファイル セクションを変更しようとしたり、呼び出し元が不十分なアクセス許可を持つオブジェクトにアクセスしようとしたりしました。</span><span class="sxs-lookup"><span data-stu-id="2b634-125">An attempt was made to modify a read-only profile section or to access an object for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="2b634-126">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2b634-126">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="2b634-127">lpEntryID で渡されたエントリ識別子に関連付  _けられたプロファイル セクションは含めではありません_。</span><span class="sxs-lookup"><span data-stu-id="2b634-127">There is not a profile section associated with the entry identifier passed in  _lpEntryID_.</span></span>
    
<span data-ttu-id="2b634-128">MAPI_E_UNKNOWN_FLAGS</span><span class="sxs-lookup"><span data-stu-id="2b634-128">MAPI_E_UNKNOWN_FLAGS</span></span> 
  
> <span data-ttu-id="2b634-129">予約済みまたはサポートされていないフラグが使用されたため、操作は完了しなかった。</span><span class="sxs-lookup"><span data-stu-id="2b634-129">Reserved or unsupported flags were used and, therefore, the operation did not complete.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2b634-130">注釈</span><span class="sxs-lookup"><span data-stu-id="2b634-130">Remarks</span></span>

<span data-ttu-id="2b634-131">**IMAPISupport::OpenProfileSection** メソッドは、すべてのサポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="2b634-131">The **IMAPISupport::OpenProfileSection** method is implemented for all support objects.</span></span> <span data-ttu-id="2b634-132">サービス プロバイダーとメッセージ サービスは **、OpenProfileSection** を呼び出してプロファイル セクションを開き、 **その IProfSect** インターフェイス実装へのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="2b634-132">Service providers and message services call **OpenProfileSection** to open a profile section and retrieve a pointer to its **IProfSect** interface implementation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2b634-133">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="2b634-133">Notes to callers</span></span>

 <span data-ttu-id="2b634-134">**OpenProfileSection** は  _、ulFlags_ パラメーターで MAPI_MODIFY フラグを設定し、アクセス許可が十分でない限り、プロファイル セクションを読み取り専用として開きます。</span><span class="sxs-lookup"><span data-stu-id="2b634-134">**OpenProfileSection** opens profile sections as read-only, unless you set the MAPI_MODIFY flag in the  _ulFlags_ parameter and your permission is sufficient.</span></span> <span data-ttu-id="2b634-135">このフラグを設定しても、読み取り/書き込みアクセス許可は保証されない。付与されるアクセス許可は、アクセス レベルとオブジェクトによって異なる。</span><span class="sxs-lookup"><span data-stu-id="2b634-135">Setting this flag does not guarantee read/write permission; the permissions that you are granted depend on your access level and the object.</span></span> 
  
<span data-ttu-id="2b634-136">**OpenProfileSection** が存在しないプロファイル セクションを読み取り専用として開くことを試みる場合、そのセクションはMAPI_E_NOT_FOUND。</span><span class="sxs-lookup"><span data-stu-id="2b634-136">If **OpenProfileSection** attempts to open a nonexistent profile section as read-only, it returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="2b634-137">**OpenProfileSection** が存在しないプロファイル セクションを読み取り/書き込みとして開く場合は、プロファイル セクションを作成し **、IProfSect** ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="2b634-137">If **OpenProfileSection** attempts to open a nonexistent profile section as read/write, it creates the profile section and returns the **IProfSect** pointer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2b634-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b634-138">See also</span></span>



[<span data-ttu-id="2b634-139">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2b634-139">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="2b634-140">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2b634-140">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="2b634-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="2b634-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="2b634-142">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2b634-142">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

