---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405661"
---
# <a name="iprovideradminopenprofilesection"></a><span data-ttu-id="c71d6-103">IProviderAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="c71d6-103">IProviderAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="c71d6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c71d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c71d6-105">現在のプロファイルからプロファイル セクションを開き、さらにアクセスする [IProfSect](iprofsectimapiprop.md) ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="c71d6-105">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="c71d6-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c71d6-106">Parameters</span></span>

 <span data-ttu-id="c71d6-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="c71d6-107">_lpUID_</span></span>
  
> <span data-ttu-id="c71d6-108">[in]開くプロファイル セクションの一意の識別子を含む [MAPIUID](mapiuid.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c71d6-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the profile section to be opened.</span></span> <span data-ttu-id="c71d6-109">クライアントは、lpUID パラメーターに  _NULL を渡す必要_ があります。</span><span class="sxs-lookup"><span data-stu-id="c71d6-109">Clients must not pass NULL for the  _lpUID_ parameter.</span></span> <span data-ttu-id="c71d6-110">サービス プロバイダーは、メッセージ サービスエントリ ポイント関数から呼び出す **際に、MAPIUID** を取得するために NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="c71d6-110">Service providers can pass NULL to retrieve the **MAPIUID** when they call from their message service entry point functions.</span></span> 
    
 <span data-ttu-id="c71d6-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c71d6-111">_lpInterface_</span></span>
  
> <span data-ttu-id="c71d6-112">[in]プロファイル セクションへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c71d6-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="c71d6-113">NULL を渡す場合、プロファイル セクションの標準インターフェイス (**IProfSect**) が返されます。</span><span class="sxs-lookup"><span data-stu-id="c71d6-113">Passing NULL results in the profile section's standard interface (**IProfSect**) being returned.</span></span> 
    
 <span data-ttu-id="c71d6-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c71d6-114">_ulFlags_</span></span>
  
> <span data-ttu-id="c71d6-115">[in]プロファイル セクションの開き方を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="c71d6-115">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="c71d6-116">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c71d6-116">The following flags can be set:</span></span>
    
<span data-ttu-id="c71d6-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c71d6-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c71d6-118">**OpenProfileSection を** 有効にし、プロファイル セクションが呼び出し元で完全に使用できる前に、正常に戻ります。</span><span class="sxs-lookup"><span data-stu-id="c71d6-118">Enables **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the caller.</span></span> <span data-ttu-id="c71d6-119">プロファイル セクションが使用できない場合は、後続の呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c71d6-119">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="c71d6-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="c71d6-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="c71d6-121">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="c71d6-121">Requests read/write permission.</span></span> <span data-ttu-id="c71d6-122">既定では、オブジェクトは読み取り専用のアクセス許可で開かれません。呼び出し元は、読み取り/書き込みアクセス許可が付与されているという前提では動作しません。</span><span class="sxs-lookup"><span data-stu-id="c71d6-122">By default, objects are opened with read-only permission, and callers should not work on the assumption that read/write permission has been granted.</span></span> <span data-ttu-id="c71d6-123">クライアントは、プロファイルのプロバイダー セクションに対する読み取り/書き込みアクセス許可を許可されません。</span><span class="sxs-lookup"><span data-stu-id="c71d6-123">Clients are not allowed read/write permission to provider sections of the profile.</span></span>
    
<span data-ttu-id="c71d6-124">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c71d6-124">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="c71d6-125">個々のサービス プロバイダーが所有するプロファイル セクションにもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c71d6-125">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="c71d6-126">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="c71d6-126">_lppProfSect_</span></span>
  
> <span data-ttu-id="c71d6-127">[out]プロファイル セクションへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="c71d6-127">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c71d6-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="c71d6-128">Return value</span></span>

<span data-ttu-id="c71d6-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="c71d6-129">S_OK</span></span> 
  
> <span data-ttu-id="c71d6-130">プロファイル セクションが正常に開かされました。</span><span class="sxs-lookup"><span data-stu-id="c71d6-130">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="c71d6-131">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="c71d6-131">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="c71d6-132">読み取り専用のプロファイル セクションを変更しようとしたり、ユーザーのアクセス許可が不十分なオブジェクトにアクセスしようとしたりしました。</span><span class="sxs-lookup"><span data-stu-id="c71d6-132">An attempt was made to modify a read-only profile section or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="c71d6-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c71d6-133">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c71d6-134">要求されたプロファイル セクションが存在しません。</span><span class="sxs-lookup"><span data-stu-id="c71d6-134">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c71d6-135">注釈</span><span class="sxs-lookup"><span data-stu-id="c71d6-135">Remarks</span></span>

<span data-ttu-id="c71d6-136">**IProviderAdmin::OpenProfileSection** メソッドは、プロファイル セクションを開き、呼び出し元がアクティブ なプロファイルから情報を読み取り、情報を書き込む可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c71d6-136">The **IProviderAdmin::OpenProfileSection** method opens a profile section, enabling the caller to read information from and possibly write information to the active profile.</span></span> 
  
<span data-ttu-id="c71d6-137">**クライアントは、OpenProfileSection** メソッドを使用してプロバイダーに属するプロファイル セクションを開くことができません。</span><span class="sxs-lookup"><span data-stu-id="c71d6-137">Clients cannot open profile sections that belong to providers by using the **OpenProfileSection** method.</span></span> 
  
<span data-ttu-id="c71d6-138">複数のクライアントまたはサービス プロバイダーは、読み取り専用アクセス許可を持つプロファイル セクションを同時に開くことができます。</span><span class="sxs-lookup"><span data-stu-id="c71d6-138">Multiple clients or service providers can simultaneously open a profile section with read-only permission.</span></span> <span data-ttu-id="c71d6-139">ただし、プロファイル セクションが読み取り/書き込みアクセス許可で開いている場合、アクセスの種類に関係なく、セクションを開く他の呼び出しを行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c71d6-139">However, when a profile section is open with read/write permission, no other calls can be made to open the section, regardless of the type of access.</span></span> <span data-ttu-id="c71d6-140">プロファイル セクションが読み取り専用アクセス許可で開いている場合、読み取り/書き込みアクセス許可を要求する後続の呼び出しは、MAPI_E_NO_ACCESS。</span><span class="sxs-lookup"><span data-stu-id="c71d6-140">If a profile section is open with read-only permission, a subsequent call to request read/write permission will fail with MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="c71d6-141">同様に、セクションが読み取り/書き込みアクセス許可で開いている場合、読み取り専用のアクセス許可を要求する後続の呼び出しも失敗します。</span><span class="sxs-lookup"><span data-stu-id="c71d6-141">Likewise, if a section is open with read/write permission, a subsequent call to request read-only permission will also fail.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c71d6-142">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="c71d6-142">Notes to callers</span></span>

<span data-ttu-id="c71d6-143">**OpenProfileSection** に _ulFlags_ で MAPI_MODIFY を渡し、lpUID で不明な **MAPIUID** を渡して存在しないプロファイル セクションを開くことを要求すると、プロファイル セクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="c71d6-143">If you request that **OpenProfileSection** open a nonexistent profile section by passing MAPI_MODIFY in  _ulFlags_ and an unknown **MAPIUID** in  _lpUID_, the profile section will be created.</span></span> 
  
<span data-ttu-id="c71d6-144">**OpenProfileSection が読み取** り専用のアクセス許可を持つ存在しないセクションを開くことを要求した場合は、そのセクションがMAPI_E_NOT_FOUND。</span><span class="sxs-lookup"><span data-stu-id="c71d6-144">If you request that **OpenProfileSection** open a nonexistent section with read-only permission, it returns MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c71d6-145">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="c71d6-145">MFCMAPI reference</span></span>

<span data-ttu-id="c71d6-146">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c71d6-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c71d6-147">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="c71d6-147">**File**</span></span>|<span data-ttu-id="c71d6-148">**関数**</span><span class="sxs-lookup"><span data-stu-id="c71d6-148">**Function**</span></span>|<span data-ttu-id="c71d6-149">**コメント**</span><span class="sxs-lookup"><span data-stu-id="c71d6-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c71d6-150">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="c71d6-150">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="c71d6-151">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="c71d6-151">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="c71d6-152">MFCMAPI は **、IProviderAdmin::OpenProfileSection** メソッドを使用して、現在のプロファイルからプロファイル セクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="c71d6-152">MFCMAPI uses the **IProviderAdmin::OpenProfileSection** method to open a profile section from the current profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c71d6-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="c71d6-153">See also</span></span>



[<span data-ttu-id="c71d6-154">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c71d6-154">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="c71d6-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c71d6-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="c71d6-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="c71d6-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="c71d6-157">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c71d6-157">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


<span data-ttu-id="c71d6-158">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="c71d6-158">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

