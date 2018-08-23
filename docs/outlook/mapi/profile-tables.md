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
ms.openlocfilehash: 84c2d02da840dfcad077462954cb10894ba153d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803686"
---
# <a name="profile-tables"></a><span data-ttu-id="13834-103">プロファイル テーブル</span><span class="sxs-lookup"><span data-stu-id="13834-103">Profile Tables</span></span>

  
  
<span data-ttu-id="13834-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13834-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13834-105">プロファイルの一覧には、特定のクライアント アプリケーションに関連付けられているすべてのプロファイルに関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="13834-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="13834-106">1 つのプロファイル テーブルのすべてのセッションでは、クライアントが使用する MAPI によって実装されています。</span><span class="sxs-lookup"><span data-stu-id="13834-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="13834-107">クライアントは、 [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)メソッドを呼び出して、プロファイル テーブルをアクセスします。</span><span class="sxs-lookup"><span data-stu-id="13834-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="13834-108">プロファイル テーブルは、静的なテーブルです。</span><span class="sxs-lookup"><span data-stu-id="13834-108">The profile table is a static table.</span></span> <span data-ttu-id="13834-109">削除対象としてマークされているプロファイルは、プロファイル テーブルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="13834-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="13834-110">としてテーブルのほとんどの実装で**GetProfileTable**が呼び出され、クライアントで利用できるプロファイルがない場合、テーブルが作成 0 個の行を持つ。</span><span class="sxs-lookup"><span data-stu-id="13834-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="13834-111">次のプロパティは、プロファイル テーブルに設定する必要な列を構成します。</span><span class="sxs-lookup"><span data-stu-id="13834-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="13834-112">**PR_DEFAULT_PROFILE**([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13834-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="13834-113">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="13834-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="13834-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="13834-114">See also</span></span>



[<span data-ttu-id="13834-115">MAPI テーブル</span><span class="sxs-lookup"><span data-stu-id="13834-115">MAPI Tables</span></span>](mapi-tables.md)

