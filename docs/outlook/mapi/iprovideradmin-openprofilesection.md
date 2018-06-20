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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 276a2bd84156e9b396df71f51130e6704ad7c7fb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801161"
---
# <a name="iprovideradminopenprofilesection"></a><span data-ttu-id="cbb98-103">IProviderAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="cbb98-103">IProviderAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="cbb98-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cbb98-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cbb98-105">現在のプロファイルからプロファイルのセクションを開き、さらにアクセスするための[IProfSect](iprofsectimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="cbb98-105">Opens a profile section from the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="cbb98-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="cbb98-106">Parameters</span></span>

 <span data-ttu-id="cbb98-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="cbb98-107">_lpUID_</span></span>
  
> <span data-ttu-id="cbb98-108">[in]プロファイルのセクションを開くことの一意の識別子を含む[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cbb98-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the profile section to be opened.</span></span> <span data-ttu-id="cbb98-109">クライアントは、 _lpUID_パラメーターに NULL を渡す必要がありますされません。</span><span class="sxs-lookup"><span data-stu-id="cbb98-109">Clients must not pass NULL for the  _lpUID_ parameter.</span></span> <span data-ttu-id="cbb98-110">サービス プロバイダーは、メッセージ サービスのエントリ ポイント関数を呼び出すときに、 **MAPIUID**を取得するために NULL を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="cbb98-110">Service providers can pass NULL to retrieve the **MAPIUID** when they call from their message service entry point functions.</span></span> 
    
 <span data-ttu-id="cbb98-111">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="cbb98-111">_lpInterface_</span></span>
  
> <span data-ttu-id="cbb98-112">[in]プロファイル セクションにアクセスするためのインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cbb98-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="cbb98-113">プロファイル セクションの標準的なインタ フェースで (**IProfSect**) が返される NULL を渡すことが発生します。</span><span class="sxs-lookup"><span data-stu-id="cbb98-113">Passing NULL results in the profile section's standard interface (**IProfSect**) being returned.</span></span> 
    
 <span data-ttu-id="cbb98-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cbb98-114">_ulFlags_</span></span>
  
> <span data-ttu-id="cbb98-115">[in]プロファイル セクションを開く方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="cbb98-115">[in] A bitmask of flags that controls how the profile section is opened.</span></span> <span data-ttu-id="cbb98-116">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="cbb98-116">The following flags can be set:</span></span>
    
<span data-ttu-id="cbb98-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="cbb98-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="cbb98-118">正常に完了が、[プロファイル] セクションは、呼び出し元に完全に利用可能な前に**OpenProfileSection**を有効にします。</span><span class="sxs-lookup"><span data-stu-id="cbb98-118">Enables **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the caller.</span></span> <span data-ttu-id="cbb98-119">プロファイル セクションが利用できない場合は、それ以降の呼び出しを行うとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="cbb98-119">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="cbb98-120">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="cbb98-120">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="cbb98-121">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="cbb98-121">Requests read/write permission.</span></span> <span data-ttu-id="cbb98-122">既定では、読み取り専用の権限を持つオブジェクトが開いているし、呼び出し元は読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="cbb98-122">By default, objects are opened with read-only permission, and callers should not work on the assumption that read/write permission has been granted.</span></span> <span data-ttu-id="cbb98-123">クライアントは、プロファイルのプロバイダー セクションへの読み取り/書き込み権限を許可されていません。</span><span class="sxs-lookup"><span data-stu-id="cbb98-123">Clients are not allowed read/write permission to provider sections of the profile.</span></span>
    
<span data-ttu-id="cbb98-124">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="cbb98-124">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="cbb98-125">個々 のサービス ・ プロバイダーが所有するものであっても、すべてのプロファイル セクションへのアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="cbb98-125">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="cbb98-126">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="cbb98-126">_lppProfSect_</span></span>
  
> <span data-ttu-id="cbb98-127">[out]プロファイル セクションへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cbb98-127">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cbb98-128">�߂�l</span><span class="sxs-lookup"><span data-stu-id="cbb98-128">Return value</span></span>

<span data-ttu-id="cbb98-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="cbb98-129">S_OK</span></span> 
  
> <span data-ttu-id="cbb98-130">プロファイル セクションが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="cbb98-130">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="cbb98-131">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="cbb98-131">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="cbb98-132">しようとは、読み取り専用のプロファイル セクションを変更するか、ユーザーが十分なアクセス許可を持っているオブジェクトへのアクセスにしました。</span><span class="sxs-lookup"><span data-stu-id="cbb98-132">An attempt was made to modify a read-only profile section or to access an object for which the user has insufficient permissions.</span></span>
    
<span data-ttu-id="cbb98-133">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="cbb98-133">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="cbb98-134">要求したプロファイル セクションが存在しません。</span><span class="sxs-lookup"><span data-stu-id="cbb98-134">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cbb98-135">備考</span><span class="sxs-lookup"><span data-stu-id="cbb98-135">Remarks</span></span>

<span data-ttu-id="cbb98-136">**IProviderAdmin::OpenProfileSection**メソッドは、呼び出し元から情報を読み取るし、可能性のあるアクティブなプロファイルに情報を記述するを有効にすると、プロファイルのセクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="cbb98-136">The **IProviderAdmin::OpenProfileSection** method opens a profile section, enabling the caller to read information from and possibly write information to the active profile.</span></span> 
  
<span data-ttu-id="cbb98-137">クライアントは、 **OpenProfileSection**メソッドを使用してプロバイダーに属するプロファイル セクションを開くことができません。</span><span class="sxs-lookup"><span data-stu-id="cbb98-137">Clients cannot open profile sections that belong to providers by using the **OpenProfileSection** method.</span></span> 
  
<span data-ttu-id="cbb98-138">複数のクライアントまたはサービス プロバイダーでは、読み取り専用のアクセス許可を持つプロファイル セクションを開くことができます同時にします。</span><span class="sxs-lookup"><span data-stu-id="cbb98-138">Multiple clients or service providers can simultaneously open a profile section with read-only permission.</span></span> <span data-ttu-id="cbb98-139">ただし、プロファイル セクションが読み取り/書き込み権限で開かれている場合は、他の呼び出しされるアクセスの種類に関係なく、」セクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="cbb98-139">However, when a profile section is open with read/write permission, no other calls can be made to open the section, regardless of the type of access.</span></span> <span data-ttu-id="cbb98-140">プロファイル セクションが読み取り専用のアクセス許可で開く場合は、読み取り/書き込みアクセス許可を要求する後続の呼び出しが MAPI_E_NO_ACCESS で失敗します。</span><span class="sxs-lookup"><span data-stu-id="cbb98-140">If a profile section is open with read-only permission, a subsequent call to request read/write permission will fail with MAPI_E_NO_ACCESS.</span></span> <span data-ttu-id="cbb98-141">同様に、セクションが読み取り/書き込み権限で開かれている場合は、読み取り専用のアクセス許可を要求する後続の呼び出しも失敗します。</span><span class="sxs-lookup"><span data-stu-id="cbb98-141">Likewise, if a section is open with read/write permission, a subsequent call to request read-only permission will also fail.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cbb98-142">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="cbb98-142">Notes to callers</span></span>

<span data-ttu-id="cbb98-143">要求する場合**OpenProfileSection**は、 _ulFlags_で MAPI_MODIFY を渡すことによってプロファイルが存在しないセクションを開くし、 _lpUID_プロファイルのセクションでは、不明な**MAPIUID**が作成されます。</span><span class="sxs-lookup"><span data-stu-id="cbb98-143">If you request that **OpenProfileSection** open a nonexistent profile section by passing MAPI_MODIFY in  _ulFlags_ and an unknown **MAPIUID** in  _lpUID_, the profile section will be created.</span></span> 
  
<span data-ttu-id="cbb98-144">読み取り専用アクセス権を持つ**OpenProfileSection**が存在しないセクションを開くことを要求した場合は MAPI_E_NOT_FOUND を返します。</span><span class="sxs-lookup"><span data-stu-id="cbb98-144">If you request that **OpenProfileSection** open a nonexistent section with read-only permission, it returns MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cbb98-145">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="cbb98-145">MFCMAPI reference</span></span>

<span data-ttu-id="cbb98-146">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="cbb98-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cbb98-147">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="cbb98-147">**File**</span></span>|<span data-ttu-id="cbb98-148">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="cbb98-148">**Function**</span></span>|<span data-ttu-id="cbb98-149">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="cbb98-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cbb98-150">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="cbb98-150">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="cbb98-151">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="cbb98-151">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="cbb98-152">MFCMAPI では、 **IProviderAdmin::OpenProfileSection**メソッドを使用して、現在のプロファイルからプロファイルのセクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="cbb98-152">MFCMAPI uses the **IProviderAdmin::OpenProfileSection** method to open a profile section from the current profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cbb98-153">関連項目</span><span class="sxs-lookup"><span data-stu-id="cbb98-153">See also</span></span>



[<span data-ttu-id="cbb98-154">IMAPIProp: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbb98-154">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="cbb98-155">IProfSect: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cbb98-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="cbb98-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="cbb98-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="cbb98-157">IProviderAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbb98-157">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


<span data-ttu-id="cbb98-158">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="cbb98-158">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

