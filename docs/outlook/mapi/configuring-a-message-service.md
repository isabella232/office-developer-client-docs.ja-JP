---
title: メッセージ サービスの構成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2b170037bc51a7848154c12acbfe700a0142ef8f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564109"
---
# <a name="configuring-a-message-service"></a><span data-ttu-id="1e369-103">メッセージ サービスの構成</span><span class="sxs-lookup"><span data-stu-id="1e369-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="1e369-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e369-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="1e369-105">**メッセージ サービスですべてのサービス プロバイダーを構成するのには**</span><span class="sxs-lookup"><span data-stu-id="1e369-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="1e369-106">[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1e369-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="1e369-107">すべての構成に必要なデータがある場合プログラムでは、ユーザー インターフェイスを表示するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="1e369-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="1e369-108">ただし、1 つまたは複数のプロバイダーの情報の一部が利用できない場合を確認、SERVICE_UI_ALLOWED または SERVICE_UI_ALWAYS フラグを設定することです。</span><span class="sxs-lookup"><span data-stu-id="1e369-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="1e369-109">必要な構成データは、メッセージが構成されていないサービスの結果を使用できない場合は、ユーザー インターフェイスを抑制します。</span><span class="sxs-lookup"><span data-stu-id="1e369-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="1e369-110">**メッセージ サービスで 1 つのサービス プロバイダーを構成するのには**</span><span class="sxs-lookup"><span data-stu-id="1e369-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="1e369-111">サービス プロバイダーの状態のオブジェクトにアクセスするのには[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1e369-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="1e369-112">サービス プロバイダーのプロパティ シートを表示するのには[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1e369-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="1e369-113">ステータス オブジェクトの使い方の詳細については、[状態テーブルおよび状態オブジェクト](status-table-and-status-objects.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e369-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

