---
title: IContabAdminRemoveStore
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IContabAdmin.RemoveStore
api_type:
- COM
ms.assetid: 2a5fcf5c-8a5a-4774-b8c9-1ac1ff27947d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4865c1c867dd73514ab22ac4e8da628caf154ee7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435419"
---
# <a name="icontabadminremovestore"></a><span data-ttu-id="e2eaf-103">IContabAdmin::RemoveStore</span><span class="sxs-lookup"><span data-stu-id="e2eaf-103">IContabAdmin::RemoveStore</span></span>

  
  
<span data-ttu-id="e2eaf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2eaf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2eaf-105">指定したエントリ ID で指定された連絡先アドレス帳 (CAB) をアドレス帳階層から削除します。</span><span class="sxs-lookup"><span data-stu-id="e2eaf-105">Removes the Contact Address Book (CAB) specified by the given entry ID from the address book hierarchy.</span></span>
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="e2eaf-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e2eaf-106">Parameters</span></span>

 <span data-ttu-id="e2eaf-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="e2eaf-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="e2eaf-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="e2eaf-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="e2eaf-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="e2eaf-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="e2eaf-110">[in]開くオブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e2eaf-110">[in] A pointer to the entry identifier of the object to open.</span></span>
    

