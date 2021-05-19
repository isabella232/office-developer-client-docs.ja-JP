---
title: メッセージ サービスの構成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4c3d30c7111e7b26886cbfb069ec2822d2ee0234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434509"
---
# <a name="configuring-a-message-service"></a><span data-ttu-id="5f2fe-103">メッセージ サービスの構成</span><span class="sxs-lookup"><span data-stu-id="5f2fe-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="5f2fe-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f2fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="5f2fe-105">**メッセージ サービス内のすべてのサービス プロバイダーを構成するには**</span><span class="sxs-lookup"><span data-stu-id="5f2fe-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="5f2fe-106">[IMsgServiceAdmin::ConfigureMsgService を呼び出します](imsgserviceadmin-configuremsgservice.md)。</span><span class="sxs-lookup"><span data-stu-id="5f2fe-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="5f2fe-107">構成に必要なすべてのデータをプログラムで使用できる場合は、ユーザー インターフェイスを表示するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="5f2fe-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="5f2fe-108">ただし、1 つ以上のプロバイダーの情報の一部が使用できない場合は、SERVICE_UI_ALLOWEDまたはSERVICE_UI_ALWAYSしてください。</span><span class="sxs-lookup"><span data-stu-id="5f2fe-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="5f2fe-109">必要な構成データが使用できない場合にユーザー インターフェイスを抑制すると、構成されていないメッセージ サービスが発生します。</span><span class="sxs-lookup"><span data-stu-id="5f2fe-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="5f2fe-110">**メッセージ サービスで 1 つのサービス プロバイダーを構成するには**</span><span class="sxs-lookup"><span data-stu-id="5f2fe-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="5f2fe-111">[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出して、サービス プロバイダーの状態オブジェクトにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="5f2fe-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="5f2fe-112">[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)を呼び出して、サービス プロバイダーのプロパティ シートを表示します。</span><span class="sxs-lookup"><span data-stu-id="5f2fe-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="5f2fe-113">状態オブジェクトの使用の詳細については、「Status [Table and Status Objects」を参照してください](status-table-and-status-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="5f2fe-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

