---
title: メッセージ サービスのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8388d14446a230b032e49ad0d614c85e79b8ece8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573720"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="614dc-103">メッセージ サービスのコピー</span><span class="sxs-lookup"><span data-stu-id="614dc-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="614dc-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="614dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="614dc-105">**メッセージ サービスをプロファイルにコピーするには**</span><span class="sxs-lookup"><span data-stu-id="614dc-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="614dc-106">[IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="614dc-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="614dc-107">メッセージ サービスをコピーすると、サービスの新しいインスタンスがオリジナルと全く同じように構成します。</span><span class="sxs-lookup"><span data-stu-id="614dc-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="614dc-108">場合があります**CopyMsgService**では、MAPI_E_ACCESS_DENIED エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="614dc-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="614dc-109">このエラーの戻り値の最も一般的な原因は、自身を複製するのには許可されていないメッセージ サービスです。</span><span class="sxs-lookup"><span data-stu-id="614dc-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

