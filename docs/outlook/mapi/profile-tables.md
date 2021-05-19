---
title: プロファイル テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 15c07c05af82389bce697c300cd9b1d504e98736
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424351"
---
# <a name="profile-tables"></a><span data-ttu-id="01924-103">プロファイル テーブル</span><span class="sxs-lookup"><span data-stu-id="01924-103">Profile Tables</span></span>

  
  
<span data-ttu-id="01924-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01924-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01924-105">プロファイル テーブルには、特定のクライアント アプリケーションに関連付けられているすべてのプロファイルに関する情報が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="01924-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="01924-106">クライアントで使用するために MAPI によって実装される、すべてのセッションに 1 つのプロファイル テーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="01924-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="01924-107">クライアントは [、IProfAdmin::GetProfileTable メソッド](iprofadmin-getprofiletable.md) を呼び出してプロファイル テーブルにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="01924-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="01924-108">プロファイル テーブルは静的テーブルです。</span><span class="sxs-lookup"><span data-stu-id="01924-108">The profile table is a static table.</span></span> <span data-ttu-id="01924-109">削除のマークが付いているプロファイルは、プロファイル テーブルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="01924-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="01924-110">ほとんどのテーブル実装と同様に **、GetProfileTable** が呼び出され、クライアントで使用できるプロファイルがない場合、テーブルはゼロ行で作成されます。</span><span class="sxs-lookup"><span data-stu-id="01924-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="01924-111">次のプロパティは、プロファイル テーブルで必要な列セットを構成します。</span><span class="sxs-lookup"><span data-stu-id="01924-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="01924-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="01924-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="01924-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="01924-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="01924-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="01924-114">See also</span></span>



[<span data-ttu-id="01924-115">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="01924-115">MAPI Tables</span></span>](mapi-tables.md)

