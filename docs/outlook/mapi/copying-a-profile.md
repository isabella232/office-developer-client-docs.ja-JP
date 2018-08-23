---
title: プロファイルのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 53b7099ae74828a97eb703b865ba30ab385e9a5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564935"
---
# <a name="copying-a-profile"></a><span data-ttu-id="7a804-103">プロファイルのコピー</span><span class="sxs-lookup"><span data-stu-id="7a804-103">Copying a Profile</span></span>

  
  
<span data-ttu-id="7a804-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a804-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a804-105">プロファイルを作成する方法の 1 つでは、既存のプロファイルからコピーし、必要なメッセージ サービスおよびサービス ・ プロバイダーを変更します。</span><span class="sxs-lookup"><span data-stu-id="7a804-105">One way to create a profile is to copy from an existing profile and alter the necessary message services and service providers.</span></span> <span data-ttu-id="7a804-106">プロファイルをコピーするには、 [MAPIAdminProfiles](mapiadminprofiles.md)関数によって、MAPI によって提供されるプロファイルの管理オブジェクトを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a804-106">Copying a profile involves using a profile administration object, provided by MAPI through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> 
  
 <span data-ttu-id="7a804-107">**プロファイルをコピーするには**</span><span class="sxs-lookup"><span data-stu-id="7a804-107">**To copy a profile**</span></span>
  
1. <span data-ttu-id="7a804-108">**IProfAdmin**インターフェイス ポインターを取得するために**MAPIAdminProfiles**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7a804-108">Call **MAPIAdminProfiles** to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="7a804-109">プロファイル テーブルにアクセスするのには[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7a804-109">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="7a804-110">コピーするプロファイルの名前の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) に一致する[SPropertyRestriction](spropertyrestriction.md)構造を持つプロパティの制限を作成します。</span><span class="sxs-lookup"><span data-stu-id="7a804-110">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the profile to be copied.</span></span> 
    
4. <span data-ttu-id="7a804-111">プロファイル テーブルに適切な行を検索するのには[IMAPITable::FindRow](imapitable-findrow.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7a804-111">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the appropriate row in the profile table.</span></span> 
    
5. <span data-ttu-id="7a804-112">[IProfAdmin::CopyProfile](iprofadmin-copyprofile.md)、 _lpszOldProfileName_パラメーターとして**PR_DISPLAY_NAME**列の値を渡すことを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7a804-112">Call [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passing the value of the **PR_DISPLAY_NAME** column as the  _lpszOldProfileName_ parameter.</span></span> 
    

