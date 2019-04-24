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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 44be43864d943257520f27297e5754a4978c568d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270169"
---
# <a name="iprofadminsetdefaultprofile"></a><span data-ttu-id="a43b9-103">IProfAdmin::SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a43b9-103">IProfAdmin::SetDefaultProfile</span></span>

  
  
<span data-ttu-id="a43b9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a43b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a43b9-105">クライアントの既定のプロファイルを設定またはクリアします。</span><span class="sxs-lookup"><span data-stu-id="a43b9-105">Sets or clears a client's default profile.</span></span>
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a43b9-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a43b9-106">Parameters</span></span>

 <span data-ttu-id="a43b9-107">_lpszprofilename_</span><span class="sxs-lookup"><span data-stu-id="a43b9-107">_lpszProfileName_</span></span>
  
> <span data-ttu-id="a43b9-108">順番既定値になるプロファイルの名前、または NULL のポインター。</span><span class="sxs-lookup"><span data-stu-id="a43b9-108">[in] A pointer to the name of the profile that will become the default, or NULL.</span></span> <span data-ttu-id="a43b9-109">_lpszprofilename_を NULL に設定すると、 **setdefaultprofile**が既存の既定のプロファイルを削除して、クライアントを既定にしないようにする必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="a43b9-109">Setting  _lpszProfileName_ to NULL indicates that **SetDefaultProfile** should remove the existing default profile, leaving the client without a default.</span></span> 
    
 <span data-ttu-id="a43b9-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a43b9-110">_ulFlags_</span></span>
  
> <span data-ttu-id="a43b9-111">順番_lpszprofilename_が指す文字列の種類を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a43b9-111">[in] A bitmask of flags that controls the type of the string pointed to by  _lpszProfileName_.</span></span> <span data-ttu-id="a43b9-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a43b9-112">The following flag can be set:</span></span>
    
<span data-ttu-id="a43b9-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a43b9-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a43b9-114">プロファイル名が Unicode 形式である。</span><span class="sxs-lookup"><span data-stu-id="a43b9-114">The profile name is in Unicode format.</span></span> <span data-ttu-id="a43b9-115">MAPI_UNICODE フラグが設定されていない場合、プロファイル名は ANSI 形式になります。</span><span class="sxs-lookup"><span data-stu-id="a43b9-115">If the MAPI_UNICODE flag is not set, the profile name is in ANSI format.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a43b9-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="a43b9-116">Return value</span></span>

<span data-ttu-id="a43b9-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="a43b9-117">S_OK</span></span> 
  
> <span data-ttu-id="a43b9-118">既定のプロファイルが正常に確立または削除されました。</span><span class="sxs-lookup"><span data-stu-id="a43b9-118">A default profile was successfully established or removed.</span></span>
    
<span data-ttu-id="a43b9-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a43b9-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a43b9-120">指定されたプロファイルが存在しません。</span><span class="sxs-lookup"><span data-stu-id="a43b9-120">The specified profile does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a43b9-121">解説</span><span class="sxs-lookup"><span data-stu-id="a43b9-121">Remarks</span></span>

<span data-ttu-id="a43b9-122">**IProfAdmin:: setdefaultprofile**メソッドは、特定のプロファイルをクライアントの既定のプロファイルとして確立するか、現在の既定のプロファイルをクリアします。</span><span class="sxs-lookup"><span data-stu-id="a43b9-122">The **IProfAdmin::SetDefaultProfile** method either establishes a particular profile as the client's default profile or clears the current default profile.</span></span> <span data-ttu-id="a43b9-123">既定のプロファイルは、クライアントが MAPI セッションを開始するときに自動的に使用されるプロファイルです。</span><span class="sxs-lookup"><span data-stu-id="a43b9-123">The default profile is the profile that is automatically used whenever the client begins a MAPI session.</span></span> <span data-ttu-id="a43b9-124">**setdefaultprofile**は、新しい既定のプロファイルの**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) プロパティも TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="a43b9-124">**SetDefaultProfile** also sets the new default profile's **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property to TRUE.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a43b9-125">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a43b9-125">Notes to callers</span></span>

<span data-ttu-id="a43b9-126">既定のプロファイルを使用してセッションを開始するには、MAPI_USE_DEFAULT フラグを[MAPILogonEx](mapilogonex.md)関数に渡します。</span><span class="sxs-lookup"><span data-stu-id="a43b9-126">To start a session with the default profile, pass the MAPI_USE_DEFAULT flag to the [MAPILogonEx](mapilogonex.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a43b9-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="a43b9-127">See also</span></span>



[<span data-ttu-id="a43b9-128">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="a43b9-128">IProfAdmin::GetProfileTable</span></span>](iprofadmin-getprofiletable.md)
  
[<span data-ttu-id="a43b9-129">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="a43b9-129">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="a43b9-130">PidTagDefaultProfile 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a43b9-130">PidTagDefaultProfile Canonical Property</span></span>](pidtagdefaultprofile-canonical-property.md)
  
[<span data-ttu-id="a43b9-131">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a43b9-131">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)

