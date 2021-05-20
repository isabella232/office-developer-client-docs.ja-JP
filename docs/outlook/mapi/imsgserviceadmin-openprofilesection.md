---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 32ebdea3a594b5adf5d46dc081098d3628ae145b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437113"
---
# <a name="imsgserviceadminopenprofilesection"></a><span data-ttu-id="8468b-103">IMsgServiceAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="8468b-103">IMsgServiceAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="8468b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8468b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8468b-105">現在のプロファイルのセクションを開き、さらにアクセスする [IProfSect](iprofsectimapiprop.md) ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="8468b-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="8468b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8468b-106">Parameters</span></span>

 <span data-ttu-id="8468b-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="8468b-107">_lpUID_</span></span>
  
> <span data-ttu-id="8468b-108">プロファイル セクションを識別 [する MAPIUID](mapiuid.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8468b-108">A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="8468b-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="8468b-109">_lpInterface_</span></span>
  
> <span data-ttu-id="8468b-110">[in]プロファイル セクションへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8468b-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="8468b-111">NULL を渡す場合、標準インターフェイスへのポインターが  _lppProfSect パラメーターで返_ されます。</span><span class="sxs-lookup"><span data-stu-id="8468b-111">Passing NULL results in a pointer to its standard interface being returned in the  _lppProfSect_ parameter.</span></span> <span data-ttu-id="8468b-112">プロファイル セクションの標準インターフェイスは **IProfSect です**。</span><span class="sxs-lookup"><span data-stu-id="8468b-112">The standard interface for a profile section is **IProfSect**.</span></span>
    
 <span data-ttu-id="8468b-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8468b-113">_ulFlags_</span></span>
  
> <span data-ttu-id="8468b-114">[in]プロファイル セクションへのアクセスを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="8468b-114">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="8468b-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8468b-115">The following flags can be set:</span></span>
    
<span data-ttu-id="8468b-116">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="8468b-116">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="8468b-117">プロファイル セクションが呼び出し元のクライアントで完全に使用できる前に **、OpenProfileSection** が正常に返されるのを許可します。</span><span class="sxs-lookup"><span data-stu-id="8468b-117">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="8468b-118">プロファイル セクションが使用できない場合は、後続の呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8468b-118">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="8468b-119">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="8468b-119">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="8468b-120">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="8468b-120">Requests read/write permission.</span></span> <span data-ttu-id="8468b-121">既定では、プロファイル セクションは読み取り専用のアクセス許可で開かれません。クライアントは、読み取り/書き込みアクセス許可が付与されているという前提で動作しません。</span><span class="sxs-lookup"><span data-stu-id="8468b-121">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="8468b-122">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8468b-122">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="8468b-123">個々のサービス プロバイダーが所有するプロファイル セクションにもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8468b-123">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="8468b-124">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="8468b-124">_lppProfSect_</span></span>
  
> <span data-ttu-id="8468b-125">[out]プロファイル セクションへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="8468b-125">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8468b-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="8468b-126">Return value</span></span>

<span data-ttu-id="8468b-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="8468b-127">S_OK</span></span> 
  
> <span data-ttu-id="8468b-128">プロファイル セクションが正常に開かされました。</span><span class="sxs-lookup"><span data-stu-id="8468b-128">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="8468b-129">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="8468b-129">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="8468b-130">呼び出し元のアクセス許可が不十分なプロファイル セクションへのアクセスが試行されました。</span><span class="sxs-lookup"><span data-stu-id="8468b-130">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="8468b-131">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8468b-131">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="8468b-132">要求されたプロファイル セクションが存在しません。</span><span class="sxs-lookup"><span data-stu-id="8468b-132">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8468b-133">注釈</span><span class="sxs-lookup"><span data-stu-id="8468b-133">Remarks</span></span>

<span data-ttu-id="8468b-134">**IMsgServiceAdmin::OpenProfileSection** メソッドは [、IProfSect](iprofsectimapiprop.md)インターフェイスをサポートするオブジェクトであるプロファイル セクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="8468b-134">The **IMsgServiceAdmin::OpenProfileSection** method opens a profile section, an object that supports the [IProfSect](iprofsectimapiprop.md) interface.</span></span> <span data-ttu-id="8468b-135">プロファイル セクションは、セッション プロファイルからの情報の読み取りおよびセッション プロファイルへの書き込みに使用されます。</span><span class="sxs-lookup"><span data-stu-id="8468b-135">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
 <span data-ttu-id="8468b-136">**OpenProfileSection** を使用して、個々のサービス プロバイダーが所有するプロファイル セクションを開MAPI_FORCE_ACCESS使用できません。</span><span class="sxs-lookup"><span data-stu-id="8468b-136">**OpenProfileSection** cannot be used to open profile sections owned by individual service providers unless MAPI_FORCE_ACCESS is used.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8468b-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="8468b-137">Notes to callers</span></span>

<span data-ttu-id="8468b-138">複数のクライアントが読み取り専用アクセス許可を持つプロファイル セクションを開くことができますが、読み取り/書き込みアクセス許可を持つプロファイル セクションを開くことができるのは 1 つのクライアントのみです。</span><span class="sxs-lookup"><span data-stu-id="8468b-138">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="8468b-139">MAPI_MODIFY フラグを設定して **OpenProfileSection** を呼び出して開くプロファイル セクションが別のクライアントにある場合、呼び出しは失敗し、MAPI_E_NO_ACCESS。</span><span class="sxs-lookup"><span data-stu-id="8468b-139">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="8468b-140">セクションが書き込み用に開いている場合、読み取り専用の開く操作は失敗します。</span><span class="sxs-lookup"><span data-stu-id="8468b-140">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="8468b-141">プロファイル セクションを作成するには **、openProfileSection** を呼び出して、MAPI_MODIFY フラグと _lpUID_ パラメーターに存在しない [MAPIUID](mapiuid.md)構造を指定します。</span><span class="sxs-lookup"><span data-stu-id="8468b-141">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent [MAPIUID](mapiuid.md) structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="8468b-142">必ず指定する必要MAPI_MODIFY。</span><span class="sxs-lookup"><span data-stu-id="8468b-142">Be sure you specify MAPI_MODIFY.</span></span> <span data-ttu-id="8468b-143">存在しない _MAPIUID_ をポイントする lpUIDを設定し **、OpenProfileSection** が読み取り専用の既定のアクセス モードを使用するために設定されている場合、呼び出しは MAPI_E_NOT_FOUND で失敗します。</span><span class="sxs-lookup"><span data-stu-id="8468b-143">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8468b-144">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="8468b-144">MFCMAPI reference</span></span>

<span data-ttu-id="8468b-145">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8468b-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8468b-146">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="8468b-146">**File**</span></span>|<span data-ttu-id="8468b-147">**関数**</span><span class="sxs-lookup"><span data-stu-id="8468b-147">**Function**</span></span>|<span data-ttu-id="8468b-148">**コメント**</span><span class="sxs-lookup"><span data-stu-id="8468b-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8468b-149">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="8468b-149">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="8468b-150">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="8468b-150">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="8468b-151">MFCMAPI は **、IMsgServiceAdmin::OpenProfileSection** メソッドを使用してプロファイル セクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="8468b-151">MFCMAPI uses the **IMsgServiceAdmin::OpenProfileSection** method to open a profile section.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8468b-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="8468b-152">See also</span></span>



[<span data-ttu-id="8468b-153">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8468b-153">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="8468b-154">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="8468b-154">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="8468b-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8468b-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="8468b-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="8468b-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="8468b-157">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8468b-157">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="8468b-158">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="8468b-158">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

