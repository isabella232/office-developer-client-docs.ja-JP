---
title: 既定のプロファイルの設定
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f6bf8f88fa3e87ae619fa32d759fc182290998ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439815"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="475c6-103">既定のプロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="475c6-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="475c6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="475c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="475c6-105">既定のプロファイルは [、MAPILogonEx](mapilogonex.md)の呼び出しで明示的に指定しない場合に使用されるプロファイルで、代わりに MAPI_USE_DEFAULT フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="475c6-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="475c6-106">**既定のプロファイルを確立するには**</span><span class="sxs-lookup"><span data-stu-id="475c6-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="475c6-107">[MAPIAdminProfiles 関数を呼び出](mapiadminprofiles.md)して **、IProfAdmin** インターフェイス ポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="475c6-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="475c6-108">[IProfAdmin::SetDefaultProfile を呼び出します](iprofadmin-setdefaultprofile.md)。</span><span class="sxs-lookup"><span data-stu-id="475c6-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="475c6-109">**SetDefaultProfile** は **PR_DEFAULT_PROFILE既定の** プロファイルの PR_DEFAULT_PROFILE ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) プロパティを設定し、以前の既定のプロファイルの設定を削除します。</span><span class="sxs-lookup"><span data-stu-id="475c6-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

