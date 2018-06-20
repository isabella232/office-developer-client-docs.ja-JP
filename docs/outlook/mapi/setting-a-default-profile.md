---
title: 既定のプロファイルを設定します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ea21e735dba8690a392629b92b636b834d7d57d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803880"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="aa62a-103">既定のプロファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="aa62a-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="aa62a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa62a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa62a-105">既定のプロファイルは、明示的に指定しない[MAPILogonEx](mapilogonex.md)、MAPI_USE_DEFAULT フラグを設定する代わりに呼び出しのいずれかの場合に使用されるプロファイルです。</span><span class="sxs-lookup"><span data-stu-id="aa62a-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="aa62a-106">**既定のプロファイルを確立するために**</span><span class="sxs-lookup"><span data-stu-id="aa62a-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="aa62a-107">**IProfAdmin**インターフェイス ポインターを取得するために[MAPIAdminProfiles](mapiadminprofiles.md)関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="aa62a-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="aa62a-108">[IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="aa62a-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="aa62a-109">**SetDefaultProfile**は、新しい既定のプロファイルで、 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) のプロパティを設定し、以前の既定のプロファイルの設定を削除します。</span><span class="sxs-lookup"><span data-stu-id="aa62a-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

