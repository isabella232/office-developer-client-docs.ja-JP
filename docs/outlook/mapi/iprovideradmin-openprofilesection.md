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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301548"
---
# <a name="iprovideradminopenprofilesection"></a><span data-ttu-id="ec42b-103">IProviderAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="ec42b-103">IProviderAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="ec42b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec42b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec42b-105">現在のプロファイルからプロファイルセクションを開き、さらにアクセスできるように[IProfSect](iprofsectimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="ec42b-105">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="ec42b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ec42b-106">Parameters</span></span>

 <span data-ttu-id="ec42b-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="ec42b-107">_lpUID_</span></span>
  
> <span data-ttu-id="ec42b-108">順番開くプロファイルセクションの一意識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ec42b-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the profile section to be opened.</span></span> <span data-ttu-id="ec42b-109">クライアントは_lpuid_パラメーターに NULL を渡すことはできません。</span><span class="sxs-lookup"><span data-stu-id="ec42b-109">Clients must not pass NULL for the  _lpUID_ parameter.</span></span> <span data-ttu-id="ec42b-110">サービスプロバイダーは、メッセージサービスのエントリポイント関数から呼び出したときに、 **MAPIUID**を取得するために NULL を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="ec42b-110">Service providers can pass NULL to retrieve the **MAPIUID** when they call from their message service entry point functions.</span></span> 
    
 <span data-ttu-id="ec42b-111">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="ec42b-111">_lpInterface_</span></span>
  
> <span data-ttu-id="ec42b-112">順番プロファイルセクションへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ec42b-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="ec42b-113">NULL 結果をプロファイルセクションの標準インターフェイス (**IProfSect**) に渡すと、返されます。</span><span class="sxs-lookup"><span data-stu-id="ec42b-113">Passing NULL results in the profile section's standard interface (**IProfSect**) being returned.</span></span> 
    
 <span data-ttu-id="ec42b-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ec42b-114">_ulFlags_</span></span>
  
> <span data-ttu-id="ec42b-115">順番プロファイルセクションが開かれる方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ec42b-115">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="ec42b-116">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ec42b-116">The following flags can be set:</span></span>
    
<span data-ttu-id="ec42b-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ec42b-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ec42b-118">呼び出し元がプロファイルセクションを完全に利用できるようになる前に、 **openプロファイル**を正常に返すことができるようにします。</span><span class="sxs-lookup"><span data-stu-id="ec42b-118">Enables **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the caller.</span></span> <span data-ttu-id="ec42b-119">プロファイルセクションが使用できない場合は、その後の呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec42b-119">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="ec42b-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="ec42b-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="ec42b-121">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="ec42b-121">Requests read/write permission.</span></span> <span data-ttu-id="ec42b-122">既定では、オブジェクトは読み取り専用アクセス許可で開かれ、読み取り/書き込みアクセス許可が付与されているという前提で呼び出し元は機能しません。</span><span class="sxs-lookup"><span data-stu-id="ec42b-122">By default, objects are opened with read-only permission, and callers should not work on the assumption that read/write permission has been granted.</span></span> <span data-ttu-id="ec42b-123">クライアントは、プロファイルのプロバイダーセクションに対する読み取り/書き込みアクセス許可を許可しません。</span><span class="sxs-lookup"><span data-stu-id="ec42b-123">Clients are not allowed read/write permission to provider sections of the profile.</span></span>
    
<span data-ttu-id="ec42b-124">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ec42b-124">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="ec42b-125">個々のサービスプロバイダによって所有されているものも含め、すべてのプロファイルセクションへのアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="ec42b-125">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="ec42b-126">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="ec42b-126">_lppProfSect_</span></span>
  
> <span data-ttu-id="ec42b-127">読み上げプロファイルセクションへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ec42b-127">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ec42b-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="ec42b-128">Return value</span></span>

<span data-ttu-id="ec42b-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec42b-129">S_OK</span></span> 
  
> <span data-ttu-id="ec42b-130">プロファイルセクションが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="ec42b-130">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="ec42b-131">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="ec42b-131">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="ec42b-132">読み取り専用プロファイルセクションを変更しようとしたか、またはユーザーが十分な権限を持っていないオブジェクトにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="ec42b-132">An attempt was made to modify a read-only profile section or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="ec42b-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ec42b-133">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ec42b-134">[要求されたプロファイル] セクションが存在しません。</span><span class="sxs-lookup"><span data-stu-id="ec42b-134">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec42b-135">解説</span><span class="sxs-lookup"><span data-stu-id="ec42b-135">Remarks</span></span>

<span data-ttu-id="ec42b-136">**IProviderAdmin:: openprofile**のメソッドは、プロファイルセクションを開き、発信者が情報を読み取り、アクティブなプロファイルに情報を書き込むことができるようにします。</span><span class="sxs-lookup"><span data-stu-id="ec42b-136">The **IProviderAdmin::OpenProfileSection** method opens a profile section, enabling the caller to read information from and possibly write information to the active profile.</span></span> 
  
<span data-ttu-id="ec42b-137">クライアントは、openプロファイルの使い方を使用して、 \*\*\*\* プロバイダーに属するプロファイルセクションを開くことができません。</span><span class="sxs-lookup"><span data-stu-id="ec42b-137">Clients cannot open profile sections that belong to providers by using the **OpenProfileSection** method.</span></span> 
  
<span data-ttu-id="ec42b-138">複数のクライアントまたはサービスプロバイダーは、読み取り専用のアクセス許可を持つプロファイルセクションを同時に開くことができます。</span><span class="sxs-lookup"><span data-stu-id="ec42b-138">Multiple clients or service providers can simultaneously open a profile section with read-only permission.</span></span> <span data-ttu-id="ec42b-139">ただし、プロファイルセクションが読み取り/書き込みアクセス許可で開かれている場合、アクセスの種類に関係なく、セクションを開く他の呼び出しを行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="ec42b-139">However, when a profile section is open with read/write permission, no other calls can be made to open the section, regardless of the type of access.</span></span> <span data-ttu-id="ec42b-140">読み取り専用アクセス許可でプロファイルセクションが開かれている場合、読み取り/書き込みアクセス許可を要求する後続の呼び出しは、MAPI_E_NO_ACCESS で失敗します。</span><span class="sxs-lookup"><span data-stu-id="ec42b-140">If a profile section is open with read-only permission, a subsequent call to request read/write permission will fail with MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="ec42b-141">同様に、セクションが読み取り/書き込みアクセス許可で開かれている場合は、読み取り専用アクセス許可を要求する次の呼び出しも失敗します。</span><span class="sxs-lookup"><span data-stu-id="ec42b-141">Likewise, if a section is open with read/write permission, a subsequent call to request read-only permission will also fail.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ec42b-142">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ec42b-142">Notes to callers</span></span>

<span data-ttu-id="ec42b-143">**MAPIUID**で MAPI_MODIFY を渡すことによって、存在しないプロファイルセクションを__ 開くように**openprofile**を要求__ した場合は、[プロファイル] セクションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ec42b-143">If you request that **OpenProfileSection** open a nonexistent profile section by passing MAPI_MODIFY in  _ulFlags_ and an unknown **MAPIUID** in  _lpUID_, the profile section will be created.</span></span> 
  
<span data-ttu-id="ec42b-144">読み取り専用アクセス許可で、存在しないセクションを開くように**openプロファイル**を要求すると、MAPI_E_NOT_FOUND が返されます。</span><span class="sxs-lookup"><span data-stu-id="ec42b-144">If you request that **OpenProfileSection** open a nonexistent section with read-only permission, it returns MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ec42b-145">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="ec42b-145">MFCMAPI reference</span></span>

<span data-ttu-id="ec42b-146">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec42b-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ec42b-147">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="ec42b-147">**File**</span></span>|<span data-ttu-id="ec42b-148">**関数**</span><span class="sxs-lookup"><span data-stu-id="ec42b-148">**Function**</span></span>|<span data-ttu-id="ec42b-149">**コメント**</span><span class="sxs-lookup"><span data-stu-id="ec42b-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec42b-150">MAPIProfileFunctions</span><span class="sxs-lookup"><span data-stu-id="ec42b-150">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ec42b-151">openプロファイル '</span><span class="sxs-lookup"><span data-stu-id="ec42b-151">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="ec42b-152">mfcmapi は、 **IProviderAdmin:: openprofile**の例を使用して、現在のプロファイルからプロファイルセクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="ec42b-152">MFCMAPI uses the **IProviderAdmin::OpenProfileSection** method to open a profile section from the current profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec42b-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec42b-153">See also</span></span>



[<span data-ttu-id="ec42b-154">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec42b-154">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="ec42b-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ec42b-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="ec42b-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ec42b-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ec42b-157">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec42b-157">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


<span data-ttu-id="ec42b-158">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ec42b-158">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

