---
title: IMAPISessionOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenProfileSection
api_type:
- COM
ms.assetid: e2757028-27e7-4fc0-9674-e8e30737ef1d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9d7c1693dfb22ae89afed8cbe1426c1e186f8b2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439920"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="8aa5e-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="8aa5e-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="8aa5e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8aa5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8aa5e-105">現在のプロファイルのセクションを開き、さらにアクセスする [IProfSect](iprofsectimapiprop.md) ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="8aa5e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8aa5e-106">Parameters</span></span>

 <span data-ttu-id="8aa5e-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="8aa5e-107">_lpUID_</span></span>
  
> <span data-ttu-id="8aa5e-108">[in]プロファイル セクションを識別 [する MAPIUID](mapiuid.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="8aa5e-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8aa5e-109">_lpInterface_</span></span>
  
> <span data-ttu-id="8aa5e-110">[in]プロファイル セクションへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="8aa5e-111">NULL を渡す場合  _、lppProfSect_ パラメーターはプロファイル セクションの標準インターフェイス **IProfSect へのポインターを返します**。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="8aa5e-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8aa5e-112">_ulFlags_</span></span>
  
> <span data-ttu-id="8aa5e-113">[in]プロファイル セクションへのアクセスを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="8aa5e-114">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-114">The following flags can be set:</span></span>
    
<span data-ttu-id="8aa5e-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="8aa5e-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="8aa5e-116">プロファイル セクションが呼び出し元のクライアントで完全に使用できる前に **、OpenProfileSection** が正常に返されるのを許可します。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="8aa5e-117">プロファイル セクションを使用できない場合は、後続の呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="8aa5e-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8aa5e-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="8aa5e-119">プロバイダーに属していないプロファイル セクションへのアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="8aa5e-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="8aa5e-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="8aa5e-121">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-121">Requests read/write permission.</span></span> <span data-ttu-id="8aa5e-122">既定では、プロファイル セクションは読み取り専用のアクセス許可で開かれません。クライアントは、読み取り/書き込みアクセス許可が付与されているという前提で動作しません。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="8aa5e-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="8aa5e-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="8aa5e-124">[out]プロファイル セクションへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8aa5e-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="8aa5e-125">Return value</span></span>

<span data-ttu-id="8aa5e-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="8aa5e-126">S_OK</span></span> 
  
> <span data-ttu-id="8aa5e-127">プロファイル セクションが正常に開かされました。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="8aa5e-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8aa5e-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8aa5e-129">呼び出し元のアクセス許可が不十分なプロファイル セクションへのアクセスが試行されました。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="8aa5e-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8aa5e-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="8aa5e-131">要求されたプロファイル セクションが存在しません。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8aa5e-132">注釈</span><span class="sxs-lookup"><span data-stu-id="8aa5e-132">Remarks</span></span>

<span data-ttu-id="8aa5e-133">**IMAPISession::OpenProfileSection** メソッドは **、IProfSect** インターフェイスをサポートするプロファイル セクションまたはオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="8aa5e-134">プロファイル セクションは、セッション プロファイルからの情報の読み取りおよびセッション プロファイルへの書き込みに使用されます。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="8aa5e-135">**OpenProfileSection** を使用して _、ulFlags_ パラメーターでユーザー名を指定しない限り、個々のサービス プロバイダーが所有するプロファイル セクションMAPI_FORCE_ACCESS開くことができません。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8aa5e-136">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="8aa5e-136">Notes to callers</span></span>

<span data-ttu-id="8aa5e-137">複数のクライアントが読み取り専用アクセス許可を持つプロファイル セクションを開くことができますが、読み取り/書き込みアクセス許可を持つプロファイル セクションを開くことができるのは 1 つのクライアントのみです。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="8aa5e-138">MAPI_MODIFY フラグを設定して **OpenProfileSection** を呼び出して開くプロファイル セクションが別のクライアントにある場合、呼び出しは失敗し、MAPI_E_NO_ACCESS。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="8aa5e-139">セクションが書き込み用に開いている場合、読み取り専用の開く操作は失敗します。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="8aa5e-140">プロファイル セクションを作成するには **、openProfileSection** を呼び出して、MAPI_MODIFY フラグと _lpUID_ パラメーターに存在しない **MAPIUID** 構造を指定します。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="8aa5e-141">必ずユーザー設定を指定MAPI_MODIFY。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="8aa5e-142">存在しない _MAPIUID_ をポイントする lpUIDを設定し **、OpenProfileSection** が読み取り専用の既定のアクセス モードを使用するために設定されている場合、呼び出しは MAPI_E_NOT_FOUND で失敗します。</span><span class="sxs-lookup"><span data-stu-id="8aa5e-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8aa5e-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="8aa5e-143">See also</span></span>



[<span data-ttu-id="8aa5e-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8aa5e-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="8aa5e-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8aa5e-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="8aa5e-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="8aa5e-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="8aa5e-147">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8aa5e-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

