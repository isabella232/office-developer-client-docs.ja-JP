---
title: 配布リストの展開
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44231a95-dafc-44f7-bfa9-9f73ea8cb8b7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5731a35b5d570669d8606be6dd6ca1a23fb87e88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414138"
---
# <a name="expanding-distribution-lists"></a><span data-ttu-id="b62d2-103">配布リストの展開</span><span class="sxs-lookup"><span data-stu-id="b62d2-103">Expanding Distribution Lists</span></span>

  
  
<span data-ttu-id="b62d2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b62d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b62d2-105">**MAPI に配布リストを展開するかどうかを確認するには**</span><span class="sxs-lookup"><span data-stu-id="b62d2-105">**To prompt MAPI to expand a distribution list**</span></span>
  
- <span data-ttu-id="b62d2-106">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) プロパティを mapipdl に設定します。</span><span class="sxs-lookup"><span data-stu-id="b62d2-106">Set its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property to MAPIPDL.</span></span>
    
    <span data-ttu-id="b62d2-107">MAPI は、メッセージをトランスポートプロバイダーに送信する前に、この種類のアドレスを展開します。</span><span class="sxs-lookup"><span data-stu-id="b62d2-107">MAPI expands addresses with this type before sending the message to the transport provider.</span></span>
    

