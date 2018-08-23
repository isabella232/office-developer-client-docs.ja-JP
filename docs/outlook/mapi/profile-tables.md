---
title: プロファイル テーブル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1046c8d92feec16428329636257ed9c1f0ec8719
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571480"
---
# <a name="profile-tables"></a><span data-ttu-id="affd7-103">プロファイル テーブル</span><span class="sxs-lookup"><span data-stu-id="affd7-103">Profile Tables</span></span>

  
  
<span data-ttu-id="affd7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="affd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="affd7-105">プロファイルの一覧には、特定のクライアント アプリケーションに関連付けられているすべてのプロファイルに関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="affd7-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="affd7-106">1 つのプロファイル テーブルのすべてのセッションでは、クライアントが使用する MAPI によって実装されています。</span><span class="sxs-lookup"><span data-stu-id="affd7-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="affd7-107">クライアントは、 [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)メソッドを呼び出して、プロファイル テーブルをアクセスします。</span><span class="sxs-lookup"><span data-stu-id="affd7-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="affd7-108">プロファイル テーブルは、静的なテーブルです。</span><span class="sxs-lookup"><span data-stu-id="affd7-108">The profile table is a static table.</span></span> <span data-ttu-id="affd7-109">削除対象としてマークされているプロファイルは、プロファイル テーブルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="affd7-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="affd7-110">としてテーブルのほとんどの実装で**GetProfileTable**が呼び出され、クライアントで利用できるプロファイルがない場合、テーブルが作成 0 個の行を持つ。</span><span class="sxs-lookup"><span data-stu-id="affd7-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="affd7-111">次のプロパティは、プロファイル テーブルに設定する必要な列を構成します。</span><span class="sxs-lookup"><span data-stu-id="affd7-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="affd7-112">**PR_DEFAULT_PROFILE**([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="affd7-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="affd7-113">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="affd7-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="affd7-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="affd7-114">See also</span></span>



[<span data-ttu-id="affd7-115">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="affd7-115">MAPI Tables</span></span>](mapi-tables.md)

