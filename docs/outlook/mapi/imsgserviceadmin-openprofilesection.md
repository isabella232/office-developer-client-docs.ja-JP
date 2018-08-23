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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8dfa777480af48819e5357fad9b1e7524148a8b7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568813"
---
# <a name="imsgserviceadminopenprofilesection"></a><span data-ttu-id="1ee0d-103">IMsgServiceAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="1ee0d-103">IMsgServiceAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="1ee0d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ee0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ee0d-105">現在のプロファイルのセクションを開き、さらにアクセスするための[IProfSect](iprofsectimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="1ee0d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1ee0d-106">Parameters</span></span>

 <span data-ttu-id="1ee0d-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="1ee0d-107">_lpUID_</span></span>
  
> <span data-ttu-id="1ee0d-108">プロファイル セクションを識別する[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-108">A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="1ee0d-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="1ee0d-109">_lpInterface_</span></span>
  
> <span data-ttu-id="1ee0d-110">[in]プロファイル セクションにアクセスするためのインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="1ee0d-111">_LppProfSect_パラメーターで返される、標準のインターフェイスへのポインターに NULL を渡すことが発生します。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-111">Passing NULL results in a pointer to its standard interface being returned in the  _lppProfSect_ parameter.</span></span> <span data-ttu-id="1ee0d-112">プロファイル セクションのための標準インターフェイスは、 **IProfSect**です。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-112">The standard interface for a profile section is **IProfSect**.</span></span>
    
 <span data-ttu-id="1ee0d-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1ee0d-113">_ulFlags_</span></span>
  
> <span data-ttu-id="1ee0d-114">[in]プロファイル セクションへのアクセスを制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-114">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="1ee0d-115">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-115">The following flags can be set:</span></span>
    
<span data-ttu-id="1ee0d-116">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="1ee0d-116">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="1ee0d-117">正常に完了するのには**OpenProfileSection**では、可能性のあるプロファイルする前にセクションは、呼び出し側のクライアントに完全に使用可能。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-117">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="1ee0d-118">プロファイル セクションが利用できない場合は、それ以降の呼び出しを行うとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-118">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="1ee0d-119">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="1ee0d-119">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="1ee0d-120">要求の読み取り/書き込みのアクセス許可</span><span class="sxs-lookup"><span data-stu-id="1ee0d-120">Requests read/write permission.</span></span> <span data-ttu-id="1ee0d-121">既定では、読み取り専用のアクセス許可を持つプロファイルのセクションを開くし、クライアントが読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-121">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="1ee0d-122">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="1ee0d-122">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="1ee0d-123">個々 のサービス ・ プロバイダーが所有するものであっても、すべてのプロファイル セクションへのアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-123">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="1ee0d-124">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="1ee0d-124">_lppProfSect_</span></span>
  
> <span data-ttu-id="1ee0d-125">[out]プロファイル セクションへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-125">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1ee0d-126">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1ee0d-126">Return value</span></span>

<span data-ttu-id="1ee0d-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ee0d-127">S_OK</span></span> 
  
> <span data-ttu-id="1ee0d-128">プロファイル セクションが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-128">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="1ee0d-129">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="1ee0d-129">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="1ee0d-130">呼び出し元が十分なアクセス許可を持っているプロファイル セクションにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-130">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="1ee0d-131">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1ee0d-131">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1ee0d-132">要求したプロファイル セクションが存在しません。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-132">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ee0d-133">注釈</span><span class="sxs-lookup"><span data-stu-id="1ee0d-133">Remarks</span></span>

<span data-ttu-id="1ee0d-134">**IMsgServiceAdmin::OpenProfileSection**メソッドは、プロファイルのセクションでは、 [IProfSect](iprofsectimapiprop.md)インターフェイスをサポートするオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-134">The **IMsgServiceAdmin::OpenProfileSection** method opens a profile section, an object that supports the [IProfSect](iprofsectimapiprop.md) interface.</span></span> <span data-ttu-id="1ee0d-135">プロファイルのセクションでは、情報の読み込みおよびセッション ・ プロファイル情報を書き込むのために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-135">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
 <span data-ttu-id="1ee0d-136">**OpenProfileSection**は、MAPI_FORCE_ACCESS を使用しない場合は、個々 のサービス ・ プロバイダーが所有するプロファイルのセクションを開くには使用できません。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-136">**OpenProfileSection** cannot be used to open profile sections owned by individual service providers unless MAPI_FORCE_ACCESS is used.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1ee0d-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="1ee0d-137">Notes to callers</span></span>

<span data-ttu-id="1ee0d-138">複数のクライアントが読み取り専用のアクセス許可を持つプロファイル セクションを開くことができますが、1 つのクライアントは、読み取り/書き込みアクセス許可を持つプロファイル セクションを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-138">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="1ee0d-139">プロファイルのセクションを開くには、MAPI_MODIFY フラグを設定して**OpenProfileSection**を呼び出すことで開こうとすると、別のクライアントの場合は、MAPI_E_NO_ACCESS を返す呼び出しが失敗します。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-139">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="1ee0d-140">セクションが書き込み用に開いている場合、読み取り専用ファイルを開く操作が失敗します。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-140">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="1ee0d-141">MAPI_MODIFY フラグと、 _lpUID_パラメーターに存在しない[MAPIUID](mapiuid.md)構造体の**OpenProfileSection**を呼び出すことによって、プロファイルのセクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-141">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent [MAPIUID](mapiuid.md) structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="1ee0d-142">MAPI_MODIFY を指定することを確認します。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-142">Be sure you specify MAPI_MODIFY.</span></span> <span data-ttu-id="1ee0d-143">存在しない**MAPIUID**を指すように_lpUID_を設定すると、 **OpenProfileSection**は読み取り専用の既定のアクセス モードを使用する設定は、MAPI_E_NOT_FOUND の呼び出しは失敗します。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-143">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1ee0d-144">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="1ee0d-144">MFCMAPI reference</span></span>

<span data-ttu-id="1ee0d-145">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="1ee0d-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1ee0d-146">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="1ee0d-146">**File**</span></span>|<span data-ttu-id="1ee0d-147">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="1ee0d-147">**Function**</span></span>|<span data-ttu-id="1ee0d-148">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="1ee0d-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ee0d-149">MAPIProfileFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="1ee0d-149">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1ee0d-150">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="1ee0d-150">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="1ee0d-151">MFCMAPI では、 **IMsgServiceAdmin::OpenProfileSection**メソッドを使用して、プロファイルのセクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="1ee0d-151">MFCMAPI uses the **IMsgServiceAdmin::OpenProfileSection** method to open a profile section.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ee0d-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="1ee0d-152">See also</span></span>



[<span data-ttu-id="1ee0d-153">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1ee0d-153">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="1ee0d-154">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="1ee0d-154">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="1ee0d-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1ee0d-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="1ee0d-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="1ee0d-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="1ee0d-157">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1ee0d-157">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="1ee0d-158">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1ee0d-158">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

