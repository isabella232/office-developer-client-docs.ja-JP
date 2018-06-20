---
title: 配布リストの展開
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44231a95-dafc-44f7-bfa9-9f73ea8cb8b7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 47a37683ac54bef72ebd50aaaa11a36bdfd28659
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800025"
---
# <a name="expanding-distribution-lists"></a><span data-ttu-id="911ec-103">配布リストの展開</span><span class="sxs-lookup"><span data-stu-id="911ec-103">Expanding Distribution Lists</span></span>

  
  
<span data-ttu-id="911ec-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="911ec-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="911ec-105">**配布リストを展開するための MAPI メッセージを表示するのには**</span><span class="sxs-lookup"><span data-stu-id="911ec-105">**To prompt MAPI to expand a distribution list**</span></span>
  
- <span data-ttu-id="911ec-106">MAPIPDL に、 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="911ec-106">Set its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property to MAPIPDL.</span></span>
    
    <span data-ttu-id="911ec-107">MAPI は、トランスポート プロバイダーにメッセージを送信する前にこのタイプのアドレスを展開します。</span><span class="sxs-lookup"><span data-stu-id="911ec-107">MAPI expands addresses with this type before sending the message to the transport provider.</span></span>
    

