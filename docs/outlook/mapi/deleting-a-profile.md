---
title: プロファイルの削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 29e7806afce885968956d53005a66bd14639ad64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799892"
---
# <a name="deleting-a-profile"></a><span data-ttu-id="3a316-103">プロファイルの削除</span><span class="sxs-lookup"><span data-stu-id="3a316-103">Deleting a Profile</span></span>

  
  
<span data-ttu-id="3a316-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3a316-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="3a316-105">**プロファイルを削除するには**</span><span class="sxs-lookup"><span data-stu-id="3a316-105">**To delete a profile**</span></span>
  
- <span data-ttu-id="3a316-106">[IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3a316-106">Call [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).</span></span>
    
 <span data-ttu-id="3a316-107">**DeleteProfile**は、現在使用されている、それを削除することが無効になるまで待機する場合、プロファイルの削除をマークします。</span><span class="sxs-lookup"><span data-stu-id="3a316-107">**DeleteProfile** marks the profile for deletion if it is currently being used, waiting until it is no longer active to remove it.</span></span> <span data-ttu-id="3a316-108">プロファイル実際には消えませんがアクティブなセッションを持つすべてのクライアントが切断されるまで。</span><span class="sxs-lookup"><span data-stu-id="3a316-108">The profile does not actually disappear until every client with an active session has disconnected.</span></span> 
  
 <span data-ttu-id="3a316-109">**DeleteProfile** 、 _ulContext_パラメーターを MSG_SERVICE_DELETE を設定したプロファイルにすべてのメッセージ サービスのエントリ ポイント関数が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3a316-109">**DeleteProfile** calls the entry point function of every message service in the profile with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="3a316-110">エントリ ポイント関数への呼び出しは、サービスは、プロファイルから物理的に削除される前に発生します。</span><span class="sxs-lookup"><span data-stu-id="3a316-110">The calls to the entry point functions occur before the services are physically removed from the profile.</span></span> 
  

