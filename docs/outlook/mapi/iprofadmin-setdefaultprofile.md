---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: af695d55cdd5f8d7e24d7e60e6eebaf03868b03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587706"
---
# <a name="iprofadminsetdefaultprofile"></a><span data-ttu-id="9b6e4-103">IProfAdmin::SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b6e4-103">IProfAdmin::SetDefaultProfile</span></span>

  
  
<span data-ttu-id="9b6e4-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b6e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b6e4-105">設定またはクライアントの既定のプロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="9b6e4-105">Sets or clears a client's default profile.</span></span>
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9b6e4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9b6e4-106">Parameters</span></span>

 <span data-ttu-id="9b6e4-107">_lpszProfileName_</span><span class="sxs-lookup"><span data-stu-id="9b6e4-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="9b6e4-108">[in]プロファイルを既定値になりますが、または NULL の名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b6e4-108">[in] A pointer to the name of the profile that will become the default, or NULL.</span></span> <span data-ttu-id="9b6e4-109">_LpszProfileName_を NULL に設定すると、デフォルトがないクライアントをそのままで既存の既定のプロファイルを**SetDefaultProfile**が削除する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="9b6e4-109">Setting  _lpszProfileName_ to NULL indicates that **SetDefaultProfile** should remove the existing default profile, leaving the client without a default.</span></span> 
    
 <span data-ttu-id="9b6e4-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9b6e4-110">_ulFlags_</span></span>
  
> <span data-ttu-id="9b6e4-111">[in]_LpszProfileName_が指す文字列の種類を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="9b6e4-111">[in] A bitmask of flags that controls the type of the string pointed to by  _lpszProfileName_.</span></span> <span data-ttu-id="9b6e4-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="9b6e4-112">The following flag can be set:</span></span>
    
<span data-ttu-id="9b6e4-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9b6e4-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9b6e4-114">プロファイル名は、Unicode 形式では。</span><span class="sxs-lookup"><span data-stu-id="9b6e4-114">The profile name is in Unicode format.</span></span> <span data-ttu-id="9b6e4-115">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のプロファイル名です。</span><span class="sxs-lookup"><span data-stu-id="9b6e4-115">If the MAPI_UNICODE flag is not set, the profile name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b6e4-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="9b6e4-116">Return value</span></span>

<span data-ttu-id="9b6e4-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b6e4-117">S_OK</span></span> 
  
> <span data-ttu-id="9b6e4-118">既定のプロファイルを設定または削除に成功しました。</span><span class="sxs-lookup"><span data-stu-id="9b6e4-118">A default profile was successfully established or removed.</span></span>
    
<span data-ttu-id="9b6e4-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="9b6e4-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="9b6e4-120">指定されたプロファイルが存在しません。</span><span class="sxs-lookup"><span data-stu-id="9b6e4-120">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9b6e4-121">注釈</span><span class="sxs-lookup"><span data-stu-id="9b6e4-121">Remarks</span></span>

<span data-ttu-id="9b6e4-122">**IProfAdmin::SetDefaultProfile**メソッドは、クライアントの既定のプロファイルとして特定のプロファイルを確立するか、または現在の既定のプロファイルを削除します。</span><span class="sxs-lookup"><span data-stu-id="9b6e4-122">The **IProfAdmin::SetDefaultProfile** method either establishes a particular profile as the client's default profile or clears the current default profile.</span></span> <span data-ttu-id="9b6e4-123">既定のプロファイルは、クライアントは、MAPI セッションを開始するたびに自動的に使用されるプロファイルです。</span><span class="sxs-lookup"><span data-stu-id="9b6e4-123">The default profile is the profile that is automatically used whenever the client begins a MAPI session.</span></span> <span data-ttu-id="9b6e4-124">**SetDefaultProfile**は、新しい既定のプロファイルの**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) のプロパティを TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="9b6e4-124">**SetDefaultProfile** also sets the new default profile's **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property to TRUE.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="9b6e4-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="9b6e4-125">Notes to callers</span></span>

<span data-ttu-id="9b6e4-126">既定のプロファイル セッションを開始するには、 [MAPILogonEx](mapilogonex.md)関数に MAPI_USE_DEFAULT フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="9b6e4-126">To start a session with the default profile, pass the MAPI_USE_DEFAULT flag to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b6e4-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b6e4-127">See also</span></span>



[<span data-ttu-id="9b6e4-128">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="9b6e4-128">IProfAdmin::GetProfileTable</span></span>](iprofadmin-getprofiletable.md)
  
[<span data-ttu-id="9b6e4-129">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="9b6e4-129">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="9b6e4-130">PidTagDefaultProfile 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9b6e4-130">PidTagDefaultProfile Canonical Property</span></span>](pidtagdefaultprofile-canonical-property.md)
  
[<span data-ttu-id="9b6e4-131">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b6e4-131">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

