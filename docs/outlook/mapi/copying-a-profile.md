---
title: プロファイルのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285231"
---
# <a name="copying-a-profile"></a><span data-ttu-id="05972-103">プロファイルのコピー</span><span class="sxs-lookup"><span data-stu-id="05972-103">Copying a Profile</span></span>

  
  
<span data-ttu-id="05972-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05972-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05972-105">プロファイルを作成する方法の1つは、既存のプロファイルからコピーして、必要なメッセージサービスおよびサービスプロバイダーを変更することです。</span><span class="sxs-lookup"><span data-stu-id="05972-105">One way to create a profile is to copy from an existing profile and alter the necessary message services and service providers.</span></span> <span data-ttu-id="05972-106">プロファイルのコピーには、 [MAPIAdminProfiles](mapiadminprofiles.md)関数を使用して MAPI で提供されるプロファイル管理オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="05972-106">Copying a profile involves using a profile administration object, provided by MAPI through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> 
  
 <span data-ttu-id="05972-107">**プロファイルをコピーするには**</span><span class="sxs-lookup"><span data-stu-id="05972-107">**To copy a profile**</span></span>
  
1. <span data-ttu-id="05972-108">**MAPIAdminProfiles**を呼び出して、 **IProfAdmin**インターフェイスポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="05972-108">Call **MAPIAdminProfiles** to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="05972-109">プロファイルテーブルにアクセスするには、 [IProfAdmin:: getprofiletable](iprofadmin-getprofiletable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="05972-109">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="05972-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) をコピーするプロファイルの名前と一致させるために、 [spropertyrestriction](spropertyrestriction.md)構造のプロパティ制限を構築します。</span><span class="sxs-lookup"><span data-stu-id="05972-110">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the profile to be copied.</span></span> 
    
4. <span data-ttu-id="05972-111">[IMAPITable:: FindRow](imapitable-findrow.md)を呼び出して、プロファイルテーブルで該当する行を見つけます。</span><span class="sxs-lookup"><span data-stu-id="05972-111">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the appropriate row in the profile table.</span></span> 
    
5. <span data-ttu-id="05972-112">[IProfAdmin:: copyprofile](iprofadmin-copyprofile.md)を呼び出し、 **PR_DISPLAY_NAME**列の値を_lpszoldprofilename_パラメーターとして渡します。</span><span class="sxs-lookup"><span data-stu-id="05972-112">Call [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passing the value of the **PR_DISPLAY_NAME** column as the  _lpszOldProfileName_ parameter.</span></span> 
    

