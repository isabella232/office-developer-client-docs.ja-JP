---
title: メッセージ サービスのコピー
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01e8ad76-973a-42fa-96aa-f41aabc12b4f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a4db4ed1c3098226891edca054621fe145daaa1f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425394"
---
# <a name="copying-a-message-service"></a><span data-ttu-id="048d9-103">メッセージ サービスのコピー</span><span class="sxs-lookup"><span data-stu-id="048d9-103">Copying a Message Service</span></span>

  
  
<span data-ttu-id="048d9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="048d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="048d9-105">**メッセージ サービスをプロファイルにコピーするには**</span><span class="sxs-lookup"><span data-stu-id="048d9-105">**To copy a message service to a profile**</span></span>
  
- <span data-ttu-id="048d9-106">[IMsgServiceAdmin::CopyMsgService を呼び出します](imsgserviceadmin-copymsgservice.md)。</span><span class="sxs-lookup"><span data-stu-id="048d9-106">Call [IMsgServiceAdmin::CopyMsgService](imsgserviceadmin-copymsgservice.md).</span></span>
    
<span data-ttu-id="048d9-107">メッセージ サービスをコピーすると、サービスの新しいインスタンスは元のインスタンスとまったく同じ方法で構成されます。</span><span class="sxs-lookup"><span data-stu-id="048d9-107">When a message service is copied, the new instance of the service is configured in exactly the same way as the original.</span></span> <span data-ttu-id="048d9-108">**CopyMsgService がエラー** メッセージを返MAPI_E_ACCESS_DENIED。</span><span class="sxs-lookup"><span data-stu-id="048d9-108">Sometimes **CopyMsgService** returns the error MAPI_E_ACCESS_DENIED.</span></span> <span data-ttu-id="048d9-109">このエラーの戻り値の最も一般的な原因は、それ自体を複製できないメッセージ サービスです。</span><span class="sxs-lookup"><span data-stu-id="048d9-109">The most common cause of this error return is a message service that does not allow itself to be duplicated.</span></span> 
  

