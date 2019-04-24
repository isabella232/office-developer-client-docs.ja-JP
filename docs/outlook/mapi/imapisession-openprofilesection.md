---
title: imapisessionopenプロファイルを開く
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329408"
---
# <a name="imapisessionopenprofilesection"></a><span data-ttu-id="a01b9-103">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="a01b9-103">IMAPISession::OpenProfileSection</span></span>

  
  
<span data-ttu-id="a01b9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a01b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a01b9-105">現在のプロファイルのセクションを開き、さらにアクセスできるように[IProfSect](iprofsectimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="a01b9-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="a01b9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a01b9-106">Parameters</span></span>

 <span data-ttu-id="a01b9-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="a01b9-107">_lpUID_</span></span>
  
> <span data-ttu-id="a01b9-108">順番プロファイルセクションを識別する[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a01b9-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="a01b9-109">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="a01b9-109">_lpInterface_</span></span>
  
> <span data-ttu-id="a01b9-110">順番プロファイルセクションへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a01b9-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="a01b9-111">NULL を渡すと、 _lppProfSect_パラメーターによって、プロファイルセクションの標準インターフェイスである**IProfSect**へのポインターが返されます。</span><span class="sxs-lookup"><span data-stu-id="a01b9-111">Passing NULL causes the  _lppProfSect_ parameter to return a pointer to the profile section's standard interface, **IProfSect**.</span></span>
    
 <span data-ttu-id="a01b9-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a01b9-112">_ulFlags_</span></span>
  
> <span data-ttu-id="a01b9-113">順番プロファイルセクションへのアクセスを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a01b9-113">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="a01b9-114">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a01b9-114">The following flags can be set:</span></span>
    
<span data-ttu-id="a01b9-115">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a01b9-115">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="a01b9-116">呼び出し\*\*\*\* 元クライアントがプロファイルセクションを完全に利用できるようになるまで、openprofile の開始を正常に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="a01b9-116">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="a01b9-117">プロファイルセクションを使用できない場合は、その後の呼び出しを行うとエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a01b9-117">If the profile section is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="a01b9-118">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a01b9-118">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="a01b9-119">プロバイダーに属さないプロファイルセクションへのアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="a01b9-119">Allows access to a profile section that does not belong to the provider.</span></span>
    
<span data-ttu-id="a01b9-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="a01b9-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="a01b9-121">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="a01b9-121">Requests read/write permission.</span></span> <span data-ttu-id="a01b9-122">既定では、プロファイルセクションは読み取り専用のアクセス許可で開かれ、読み取り/書き込みアクセス許可が与えられているという前提でクライアントを動作させることはできません。</span><span class="sxs-lookup"><span data-stu-id="a01b9-122">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
 <span data-ttu-id="a01b9-123">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="a01b9-123">_lppProfSect_</span></span>
  
> <span data-ttu-id="a01b9-124">読み上げプロファイルセクションへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a01b9-124">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a01b9-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="a01b9-125">Return value</span></span>

<span data-ttu-id="a01b9-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="a01b9-126">S_OK</span></span> 
  
> <span data-ttu-id="a01b9-127">プロファイルセクションが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="a01b9-127">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="a01b9-128">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a01b9-128">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="a01b9-129">発信者が十分なアクセス許可を持っていないプロファイルセクションにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="a01b9-129">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="a01b9-130">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a01b9-130">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a01b9-131">[要求されたプロファイル] セクションが存在しません。</span><span class="sxs-lookup"><span data-stu-id="a01b9-131">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a01b9-132">解説</span><span class="sxs-lookup"><span data-stu-id="a01b9-132">Remarks</span></span>

<span data-ttu-id="a01b9-133">**imapisession:: openプロファイル**のメソッドは、 **IProfSect**インターフェイスをサポートするプロファイルセクションまたはオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="a01b9-133">The **IMAPISession::OpenProfileSection** method opens a profile section or object that supports the **IProfSect** interface.</span></span> <span data-ttu-id="a01b9-134">プロファイルセクションは、セッションプロファイルに関する情報の読み取りおよび書き込みに使用されます。</span><span class="sxs-lookup"><span data-stu-id="a01b9-134">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
<span data-ttu-id="a01b9-135">_ulflags_パラメーター \*\*\*\* に MAPI_FORCE_ACCESS を指定しない限り、openprofile sections を使用して、個々のサービスプロバイダーが所有するプロファイルセクションを開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="a01b9-135">You cannot use **OpenProfileSection** to open profile sections that individual service providers own unless you specify MAPI_FORCE_ACCESS in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a01b9-136">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a01b9-136">Notes to callers</span></span>

<span data-ttu-id="a01b9-137">複数のクライアントが読み取り専用アクセス許可でプロファイルセクションを開くことはできますが、読み取り/書き込みアクセス許可を持つプロファイルセクションを開くことができるクライアントは1つだけです。</span><span class="sxs-lookup"><span data-stu-id="a01b9-137">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="a01b9-138">MAPI_MODIFY フラグセットを使用して openprofile を呼び出すことによっ\*\*\*\* て開こうとして、別のクライアントでプロファイルセクションが開いている場合、呼び出しは失敗し、MAPI_E_NO_ACCESS が返されます。</span><span class="sxs-lookup"><span data-stu-id="a01b9-138">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="a01b9-139">読み取り専用の開く操作は、セクションが書き込み用に開かれている場合は失敗します。</span><span class="sxs-lookup"><span data-stu-id="a01b9-139">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="a01b9-140">MAPI_MODIFY フラグと、 _lpuid_パラメーターに存在しない**MAPIUID**構造で**openprofile**を呼び出すことで、プロファイルセクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a01b9-140">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent **MAPIUID** structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="a01b9-141">必ず MAPI_MODIFY を指定してください。</span><span class="sxs-lookup"><span data-stu-id="a01b9-141">Be sure that you specify MAPI_MODIFY.</span></span> <span data-ttu-id="a01b9-142">存在しない**MAPIUID**をポイントするように_lpuid_を設定し、 **openプロファイル**が読み取り専用の既定のアクセスモードを使用するように設定されている場合、呼び出しは MAPI_E_NOT_FOUND で失敗します。</span><span class="sxs-lookup"><span data-stu-id="a01b9-142">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a01b9-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="a01b9-143">See also</span></span>



[<span data-ttu-id="a01b9-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a01b9-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="a01b9-145">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a01b9-145">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="a01b9-146">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a01b9-146">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="a01b9-147">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a01b9-147">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)

