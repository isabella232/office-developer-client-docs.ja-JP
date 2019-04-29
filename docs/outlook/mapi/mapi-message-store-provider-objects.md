---
title: MAPI メッセージストアプロバイダーオブジェクト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 87a452e6-dedf-414d-b7cf-07c8b02dd94a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 55220927206692822593fefb1502a3101b777ccc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413298"
---
# <a name="mapi-message-store-provider-objects"></a><span data-ttu-id="8237a-103">MAPI メッセージストアプロバイダーオブジェクト</span><span class="sxs-lookup"><span data-stu-id="8237a-103">MAPI message store provider objects</span></span>
  
<span data-ttu-id="8237a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8237a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8237a-105">メッセージストアプロバイダーは、すべてのサービスプロバイダーと同様に、プロバイダーおよびログオンオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="8237a-105">Message store providers implement provider and logon objects, as do all service providers.</span></span> <span data-ttu-id="8237a-106">また、メッセージストアオブジェクト、フォルダー、メッセージ、添付ファイル、およびテーブルも実装します。</span><span class="sxs-lookup"><span data-stu-id="8237a-106">They also implement a message store object, folders, messages, attachments, and tables.</span></span> <span data-ttu-id="8237a-107">オプションとして、一部のメッセージストアプロバイダーは status オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="8237a-107">As an option, some message store providers implement status objects.</span></span>
  
<span data-ttu-id="8237a-108">次の図は、各メッセージストアオブジェクトとそれに対応するインターフェイス、およびそれを使用する MAPI コンポーネントを示しています。</span><span class="sxs-lookup"><span data-stu-id="8237a-108">The following illustration shows each message store object with its corresponding interface and the MAPI component that uses it.</span></span>
  
<span data-ttu-id="8237a-109">![メッセージストアプロバイダーが実装するオブジェクト](media/amapi_63.gif "メッセージストアプロバイダーが実装するオブジェクト")</span><span class="sxs-lookup"><span data-stu-id="8237a-109">![Objects that message store providers implement](media/amapi_63.gif "Objects that message store providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8237a-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="8237a-110">See also</span></span>

- [<span data-ttu-id="8237a-111">MAPI サービスプロバイダオブジェクト</span><span class="sxs-lookup"><span data-stu-id="8237a-111">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

