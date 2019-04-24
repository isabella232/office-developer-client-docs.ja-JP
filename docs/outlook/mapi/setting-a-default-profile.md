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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339313"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="29c46-103">既定のプロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="29c46-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="29c46-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29c46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29c46-105">既定のプロファイルは、 [MAPILogonEx](mapilogonex.md)への呼び出しで明示的に指定されていない場合に使用されるプロファイルです。 MAPI_USE_DEFAULT フラグの代わりに設定します。</span><span class="sxs-lookup"><span data-stu-id="29c46-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="29c46-106">**既定のプロファイルを設定するには**</span><span class="sxs-lookup"><span data-stu-id="29c46-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="29c46-107">[MAPIAdminProfiles](mapiadminprofiles.md)関数を呼び出して、 **IProfAdmin**インターフェイスポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="29c46-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="29c46-108">Call [IProfAdmin:: setdefaultprofile](iprofadmin-setdefaultprofile.md)。</span><span class="sxs-lookup"><span data-stu-id="29c46-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="29c46-109">**setdefaultprofile**は、新しい既定のプロファイルに対して**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) プロパティを設定し、以前の既定のプロファイルの設定を削除します。</span><span class="sxs-lookup"><span data-stu-id="29c46-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

