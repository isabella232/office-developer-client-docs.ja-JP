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
ms.openlocfilehash: 7d1296ba74bbafcd26a8878dfb1eb2f359ab3e03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799808"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="e799f-103">メッセージ サービスのコピー</span><span class="sxs-lookup"><span data-stu-id="e799f-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="e799f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e799f-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="e799f-105">**メッセージ サービスをプロファイルにコピーするには**</span><span class="sxs-lookup"><span data-stu-id="e799f-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="e799f-106">[IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e799f-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="e799f-107">メッセージ サービスをコピーすると、サービスの新しいインスタンスがオリジナルと全く同じように構成します。</span><span class="sxs-lookup"><span data-stu-id="e799f-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="e799f-108">場合があります**CopyMsgService**では、MAPI_E_ACCESS_DENIED エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="e799f-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="e799f-109">このエラーの戻り値の最も一般的な原因は、自身を複製するのには許可されていないメッセージ サービスです。</span><span class="sxs-lookup"><span data-stu-id="e799f-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

