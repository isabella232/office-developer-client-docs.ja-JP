---
title: メッセージサービスの構成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4c3d30c7111e7b26886cbfb069ec2822d2ee0234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335113"
---
# <a name="configuring-a-message-service"></a><span data-ttu-id="30be1-103">メッセージサービスの構成</span><span class="sxs-lookup"><span data-stu-id="30be1-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="30be1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30be1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="30be1-105">**メッセージサービスのすべてのサービスプロバイダーを構成するには**</span><span class="sxs-lookup"><span data-stu-id="30be1-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="30be1-106">[IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="30be1-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="30be1-107">構成に必要なすべてのデータがプログラムで利用できる場合は、ユーザーインターフェイスを表示するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="30be1-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="30be1-108">ただし、1つまたは複数のプロバイダーの情報の一部を使用できない場合は、SERVICE_UI_ALLOWED または SERVICE_UI_ALWAYS フラグを設定してください。</span><span class="sxs-lookup"><span data-stu-id="30be1-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="30be1-109">必要な構成データが利用できない場合にユーザーインターフェイスを非表示にすると、メッセージサービスは未構成の状態になります。</span><span class="sxs-lookup"><span data-stu-id="30be1-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="30be1-110">**メッセージサービスで1つのサービスプロバイダーを構成するには**</span><span class="sxs-lookup"><span data-stu-id="30be1-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="30be1-111">呼び出し[imapisession:: getstatustable](imapisession-getstatustable.md)は、サービスプロバイダーの status オブジェクトにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="30be1-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="30be1-112">呼び出し[imapistatus:: settingsdialog](imapistatus-settingsdialog.md)を呼び出して、サービスプロバイダーのプロパティシートを表示します。</span><span class="sxs-lookup"><span data-stu-id="30be1-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="30be1-113">状態オブジェクトの使用の詳細については、「 [status Table and status objects](status-table-and-status-objects.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="30be1-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

