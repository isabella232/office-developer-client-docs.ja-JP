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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e5f329ef0d3483683d5c94ed38c6631d86e77b93
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800706"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="5f698-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="5f698-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="5f698-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5f698-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5f698-105">現在のプロファイルのセクションを開き、さらにアクセスするための[IProfSect](iprofsectimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="5f698-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="5f698-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5f698-106">Parameters</span></span>

 <span data-ttu-id="5f698-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="5f698-107">_lpUID_</span></span>
  
> <span data-ttu-id="5f698-108">[in]プロファイル セクションを識別する[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5f698-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="5f698-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="5f698-109">_lpInterface_</span></span>
  
> <span data-ttu-id="5f698-110">[in]プロファイル セクションにアクセスするためのインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5f698-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="5f698-111">プロファイル セクションの標準的なインターフェイス、 **IProfSect**へのポインターを返すに_lppProfSect_パラメーターは、NULL を渡すことです。</span><span class="sxs-lookup"><span data-stu-id="5f698-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="5f698-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5f698-112">_ulFlags_</span></span>
  
> <span data-ttu-id="5f698-113">[in]プロファイル セクションへのアクセスを制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="5f698-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="5f698-114">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5f698-114">The following flags can be set:</span></span>
    
<span data-ttu-id="5f698-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5f698-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5f698-116">正常に完了するのには**OpenProfileSection**では、可能性のあるプロファイルする前にセクションは、呼び出し側のクライアントに完全に使用可能。</span><span class="sxs-lookup"><span data-stu-id="5f698-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="5f698-117">プロファイル セクションが利用できない場合は、それ以降の呼び出しを行うとエラーが発生することができます。</span><span class="sxs-lookup"><span data-stu-id="5f698-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="5f698-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5f698-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="5f698-119">プロバイダーに属していないプロファイル セクションへのアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="5f698-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="5f698-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="5f698-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="5f698-121">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="5f698-121">Requests read/write permission.</span></span> <span data-ttu-id="5f698-122">既定では、読み取り専用のアクセス許可を持つプロファイルのセクションを開くし、クライアントが読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f698-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="5f698-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="5f698-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="5f698-124">[out]プロファイル セクションへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5f698-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5f698-125">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5f698-125">Return value</span></span>

<span data-ttu-id="5f698-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="5f698-126">S_OK</span></span> 
  
> <span data-ttu-id="5f698-127">プロファイル セクションが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="5f698-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="5f698-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="5f698-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="5f698-129">呼び出し元が十分なアクセス許可を持っているプロファイル セクションにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="5f698-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="5f698-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="5f698-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="5f698-131">要求したプロファイル セクションが存在しません。</span><span class="sxs-lookup"><span data-stu-id="5f698-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5f698-132">注釈</span><span class="sxs-lookup"><span data-stu-id="5f698-132">Remarks</span></span>

<span data-ttu-id="5f698-133">**IMAPISession::OpenProfileSection**メソッドは、プロファイルのセクションまたは**IProfSect**インターフェイスをサポートするオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="5f698-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="5f698-134">プロファイルのセクションでは、情報の読み込みおよびセッション ・ プロファイル情報を書き込むのために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5f698-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="5f698-135">_UlFlags_パラメーターで MAPI_FORCE_ACCESS を指定しない限り、その個々 のサービス プロバイダーを独自でプロファイルのセクションを開くには、 **OpenProfileSection**を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="5f698-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5f698-136">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="5f698-136">Notes to callers</span></span>

<span data-ttu-id="5f698-137">複数のクライアントが読み取り専用のアクセス許可を持つプロファイル セクションを開くことができますが、1 つのクライアントは、読み取り/書き込みアクセス許可を持つプロファイル セクションを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="5f698-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="5f698-138">プロファイルのセクションを開くには、MAPI_MODIFY フラグを設定して**OpenProfileSection**を呼び出すことで開こうとすると、別のクライアントの場合は、MAPI_E_NO_ACCESS を返す呼び出しが失敗します。</span><span class="sxs-lookup"><span data-stu-id="5f698-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="5f698-139">セクションが書き込み用に開いている場合、読み取り専用ファイルを開く操作が失敗します。</span><span class="sxs-lookup"><span data-stu-id="5f698-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="5f698-140">MAPI_MODIFY フラグと、 _lpUID_パラメーターに存在しない**MAPIUID**構造体の**OpenProfileSection**を呼び出すことによって、プロファイルのセクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="5f698-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="5f698-141">MAPI_MODIFY を指定することを確認します。</span><span class="sxs-lookup"><span data-stu-id="5f698-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="5f698-142">存在しない**MAPIUID**を指すように_lpUID_を設定すると、 **OpenProfileSection**は読み取り専用の既定のアクセス モードを使用する設定は、MAPI_E_NOT_FOUND の呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="5f698-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f698-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="5f698-143">See also</span></span>



[<span data-ttu-id="5f698-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5f698-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="5f698-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5f698-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="5f698-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="5f698-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="5f698-147">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5f698-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

