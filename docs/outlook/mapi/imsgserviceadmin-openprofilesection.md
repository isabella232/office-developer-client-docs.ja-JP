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
ms.openlocfilehash: 32ebdea3a594b5adf5d46dc081098d3628ae145b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317399"
---
# <a name="imsgserviceadminopenprofilesection"></a><span data-ttu-id="9b909-103">IMsgServiceAdmin::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="9b909-103">IMsgServiceAdmin::OpenProfileSection</span></span>

  
  
<span data-ttu-id="9b909-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b909-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b909-105">現在のプロファイルのセクションを開き、さらにアクセスできるように[IProfSect](iprofsectimapiprop.md)ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="9b909-105">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span> 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a><span data-ttu-id="9b909-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9b909-106">Parameters</span></span>

 <span data-ttu-id="9b909-107">_lpuid_</span><span class="sxs-lookup"><span data-stu-id="9b909-107">_lpUID_</span></span>
  
> <span data-ttu-id="9b909-108">プロファイルセクションを識別する[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b909-108">A pointer to the [MAPIUID](mapiuid.md) structure that identifies the profile section.</span></span> 
    
 <span data-ttu-id="9b909-109">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="9b909-109">_lpInterface_</span></span>
  
> <span data-ttu-id="9b909-110">順番プロファイルセクションへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b909-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section.</span></span> <span data-ttu-id="9b909-111">_lppProfSect_パラメーターで返される標準インターフェイスへのポインターで NULL 値が渡されます。</span><span class="sxs-lookup"><span data-stu-id="9b909-111">Passing NULL results in a pointer to its standard interface being returned in the  _lppProfSect_ parameter.</span></span> <span data-ttu-id="9b909-112">プロファイルセクションの標準インターフェイスは**IProfSect**です。</span><span class="sxs-lookup"><span data-stu-id="9b909-112">The standard interface for a profile section is **IProfSect**.</span></span>
    
 <span data-ttu-id="9b909-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9b909-113">_ulFlags_</span></span>
  
> <span data-ttu-id="9b909-114">順番プロファイルセクションへのアクセスを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="9b909-114">[in] A bitmask of flags that controls access to the profile section.</span></span> <span data-ttu-id="9b909-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="9b909-115">The following flags can be set:</span></span>
    
<span data-ttu-id="9b909-116">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="9b909-116">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="9b909-117">呼び出し\*\*\*\* 元クライアントがプロファイルセクションを完全に利用できるようになるまで、openprofile の開始を正常に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="9b909-117">Allows **OpenProfileSection** to return successfully, possibly before the profile section is fully available to the calling client.</span></span> <span data-ttu-id="9b909-118">プロファイルセクションが使用できない場合は、その後の呼び出しでエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9b909-118">If the profile section is not available, making a subsequent call to it can raise an error.</span></span> 
    
<span data-ttu-id="9b909-119">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="9b909-119">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="9b909-120">読み取り/書き込みアクセス許可を要求します。</span><span class="sxs-lookup"><span data-stu-id="9b909-120">Requests read/write permission.</span></span> <span data-ttu-id="9b909-121">既定では、プロファイルセクションは読み取り専用のアクセス許可で開かれ、読み取り/書き込みアクセス許可が与えられているという前提でクライアントを動作させることはできません。</span><span class="sxs-lookup"><span data-stu-id="9b909-121">By default, profile sections are opened with read-only permission, and clients should not work on the assumption that read/write permission has been granted.</span></span> 
    
<span data-ttu-id="9b909-122">MAPI_FORCE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9b909-122">MAPI_FORCE_ACCESS</span></span>
  
> <span data-ttu-id="9b909-123">個々のサービスプロバイダによって所有されているものも含め、すべてのプロファイルセクションへのアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="9b909-123">Allows access to all profile sections, even those owned by individual service providers.</span></span>
    
 <span data-ttu-id="9b909-124">_lppProfSect_</span><span class="sxs-lookup"><span data-stu-id="9b909-124">_lppProfSect_</span></span>
  
> <span data-ttu-id="9b909-125">読み上げプロファイルセクションへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b909-125">[out] A pointer to a pointer to the profile section.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b909-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="9b909-126">Return value</span></span>

<span data-ttu-id="9b909-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b909-127">S_OK</span></span> 
  
> <span data-ttu-id="9b909-128">プロファイルセクションが正常に開かれました。</span><span class="sxs-lookup"><span data-stu-id="9b909-128">The profile section was successfully opened.</span></span>
    
<span data-ttu-id="9b909-129">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="9b909-129">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="9b909-130">発信者が十分なアクセス許可を持っていないプロファイルセクションにアクセスしようとしました。</span><span class="sxs-lookup"><span data-stu-id="9b909-130">An attempt was made to access a profile section for which the caller has insufficient permissions.</span></span>
    
<span data-ttu-id="9b909-131">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9b909-131">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="9b909-132">[要求されたプロファイル] セクションが存在しません。</span><span class="sxs-lookup"><span data-stu-id="9b909-132">The requested profile section does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b909-133">解説</span><span class="sxs-lookup"><span data-stu-id="9b909-133">Remarks</span></span>

<span data-ttu-id="9b909-134">**IMsgServiceAdmin:: openprofile**のメソッドは、プロファイルセクション、 [IProfSect](iprofsectimapiprop.md)インターフェイスをサポートするオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="9b909-134">The **IMsgServiceAdmin::OpenProfileSection** method opens a profile section, an object that supports the [IProfSect](iprofsectimapiprop.md) interface.</span></span> <span data-ttu-id="9b909-135">プロファイルセクションは、セッションプロファイルに関する情報の読み取りおよび書き込みに使用されます。</span><span class="sxs-lookup"><span data-stu-id="9b909-135">Profile sections are used for reading information from and writing information to the session profile.</span></span> 
  
 <span data-ttu-id="9b909-136">\*\*\*\* MAPI_FORCE_ACCESS が使用されていない場合、openprofile を使用して、個々のサービスプロバイダーが所有するプロファイルセクションを開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="9b909-136">**OpenProfileSection** cannot be used to open profile sections owned by individual service providers unless MAPI_FORCE_ACCESS is used.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9b909-137">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="9b909-137">Notes to callers</span></span>

<span data-ttu-id="9b909-138">複数のクライアントが読み取り専用アクセス許可でプロファイルセクションを開くことはできますが、読み取り/書き込みアクセス許可を持つプロファイルセクションを開くことができるクライアントは1つだけです。</span><span class="sxs-lookup"><span data-stu-id="9b909-138">Multiple clients can open a profile section with read-only permission, but only one client can open a profile section with read/write permission.</span></span> <span data-ttu-id="9b909-139">MAPI_MODIFY フラグセットを使用して openprofile を呼び出すことによっ\*\*\*\* て開こうとして、別のクライアントでプロファイルセクションが開いている場合、呼び出しは失敗し、MAPI_E_NO_ACCESS が返されます。</span><span class="sxs-lookup"><span data-stu-id="9b909-139">If another client has a profile section open that you attempt to open by calling **OpenProfileSection** with the MAPI_MODIFY flag set, the call will fail, returning MAPI_E_NO_ACCESS.</span></span> 
  
<span data-ttu-id="9b909-140">読み取り専用の開く操作は、セクションが書き込み用に開かれている場合は失敗します。</span><span class="sxs-lookup"><span data-stu-id="9b909-140">A read-only open operation fails if the section is open for writing.</span></span> 
  
<span data-ttu-id="9b909-141">MAPI_MODIFY フラグと、 _lpuid_パラメーターに存在しない[MAPIUID](mapiuid.md)構造で**openprofile**を呼び出すことで、プロファイルセクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9b909-141">You can create a profile section by calling **OpenProfileSection** with the MAPI_MODIFY flag and a nonexistent [MAPIUID](mapiuid.md) structure in the  _lpUID_ parameter.</span></span> <span data-ttu-id="9b909-142">必ず MAPI_MODIFY を指定してください。</span><span class="sxs-lookup"><span data-stu-id="9b909-142">Be sure you specify MAPI_MODIFY.</span></span> <span data-ttu-id="9b909-143">存在しない**MAPIUID**をポイントするように_lpuid_を設定し、 **openプロファイル**が読み取り専用の既定のアクセスモードを使用するように設定されている場合、呼び出しは MAPI_E_NOT_FOUND で失敗します。</span><span class="sxs-lookup"><span data-stu-id="9b909-143">If you set  _lpUID_ to point to a nonexistent **MAPIUID** and **OpenProfileSection** is set to use the default access mode of read-only, the call will fail with MAPI_E_NOT_FOUND.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9b909-144">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="9b909-144">MFCMAPI reference</span></span>

<span data-ttu-id="9b909-145">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b909-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9b909-146">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="9b909-146">**File**</span></span>|<span data-ttu-id="9b909-147">**関数**</span><span class="sxs-lookup"><span data-stu-id="9b909-147">**Function**</span></span>|<span data-ttu-id="9b909-148">**コメント**</span><span class="sxs-lookup"><span data-stu-id="9b909-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9b909-149">MAPIProfileFunctions</span><span class="sxs-lookup"><span data-stu-id="9b909-149">MAPIProfileFunctions.cpp</span></span>  <br/> |<span data-ttu-id="9b909-150">openプロファイル '</span><span class="sxs-lookup"><span data-stu-id="9b909-150">OpenProfileSection</span></span>  <br/> |<span data-ttu-id="9b909-151">mfcmapi は、 **IMsgServiceAdmin:: openprofile**の例を使用して、プロファイルセクションを開きます。</span><span class="sxs-lookup"><span data-stu-id="9b909-151">MFCMAPI uses the **IMsgServiceAdmin::OpenProfileSection** method to open a profile section.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b909-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b909-152">See also</span></span>



[<span data-ttu-id="9b909-153">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b909-153">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="9b909-154">IMAPISession::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="9b909-154">IMAPISession::OpenProfileSection</span></span>](imapisession-openprofilesection.md)
  
[<span data-ttu-id="9b909-155">IProfSect : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9b909-155">IProfSect : IMAPIProp</span></span>](iprofsectimapiprop.md)
  
[<span data-ttu-id="9b909-156">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="9b909-156">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="9b909-157">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b909-157">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


<span data-ttu-id="9b909-158">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="9b909-158">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

