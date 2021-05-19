---
title: プロファイルの削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410204"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="05fce-103">プロファイルの削除</span><span class="sxs-lookup"><span data-stu-id="05fce-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="05fce-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05fce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="05fce-105">**プロファイルを削除するには**</span><span class="sxs-lookup"><span data-stu-id="05fce-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="05fce-106">[IProfAdmin::D Profile を呼び出します](iprofadmin-deleteprofile.md)。</span><span class="sxs-lookup"><span data-stu-id="05fce-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="05fce-107">**DeleteProfile は** 、プロファイルが現在使用されている場合は削除のマークを付け、プロファイルの削除がアクティブでなくなるまで待機します。</span><span class="sxs-lookup"><span data-stu-id="05fce-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="05fce-108">アクティブなセッションを持つすべてのクライアントが切断されるまで、プロファイルは実際には消えません。</span><span class="sxs-lookup"><span data-stu-id="05fce-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="05fce-109">**DeleteProfile は** 、プロファイル内のすべてのメッセージ サービスのエントリ ポイント関数を呼び出し  _、ulContext_ パラメーターを MSG_SERVICE_DELETE。</span><span class="sxs-lookup"><span data-stu-id="05fce-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="05fce-110">エントリ ポイント関数の呼び出しは、サービスがプロファイルから物理的に削除される前に行われます。</span><span class="sxs-lookup"><span data-stu-id="05fce-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

