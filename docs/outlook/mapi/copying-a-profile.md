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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424729"
---
# <a name="copying-a-profile"></a><span data-ttu-id="30848-103">プロファイルのコピー</span><span class="sxs-lookup"><span data-stu-id="30848-103">Copying a Profile</span></span>

  
  
<span data-ttu-id="30848-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30848-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30848-105">プロファイルを作成する 1 つの方法は、既存のプロファイルからコピーし、必要なメッセージ サービスとサービス プロバイダーを変更する方法です。</span><span class="sxs-lookup"><span data-stu-id="30848-105">One way to create a profile is to copy from an existing profile and alter the necessary message services and service providers.</span></span> <span data-ttu-id="30848-106">プロファイルのコピーには [、MAPIAdminProfiles](mapiadminprofiles.md) 関数を介して MAPI によって提供されるプロファイル管理オブジェクトを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30848-106">Copying a profile involves using a profile administration object, provided by MAPI through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> 
  
 <span data-ttu-id="30848-107">**プロファイルをコピーするには**</span><span class="sxs-lookup"><span data-stu-id="30848-107">**To copy a profile**</span></span>
  
1. <span data-ttu-id="30848-108">**MAPIAdminProfiles を呼び出** して **、IProfAdmin インターフェイス ポインターを** 取得します。</span><span class="sxs-lookup"><span data-stu-id="30848-108">Call **MAPIAdminProfiles** to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="30848-109">[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)を呼び出して、プロファイル テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="30848-109">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="30848-110">[SPropertyRestriction](spropertyrestriction.md)構造体を使用してプロパティ制限を作成し **、PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) とコピーするプロファイルの名前を一致します。</span><span class="sxs-lookup"><span data-stu-id="30848-110">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the profile to be copied.</span></span> 
    
4. <span data-ttu-id="30848-111">[IMAPITable::FindRow を呼び出](imapitable-findrow.md)して、プロファイル テーブル内の適切な行を探します。</span><span class="sxs-lookup"><span data-stu-id="30848-111">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the appropriate row in the profile table.</span></span> 
    
5. <span data-ttu-id="30848-112">[IProfAdmin::CopyProfile](iprofadmin-copyprofile.md)を呼び出し、PR_DISPLAY_NAMEの値を _lpszOldProfileName パラメーターとして渡_ します。 </span><span class="sxs-lookup"><span data-stu-id="30848-112">Call [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passing the value of the **PR_DISPLAY_NAME** column as the  _lpszOldProfileName_ parameter.</span></span> 
    

