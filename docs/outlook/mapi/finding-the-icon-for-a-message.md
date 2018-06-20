---
title: メッセージのアイコンを検索します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b73545585d3279bc290524c7ccb26c14c2977fe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800049"
---
# <a name="finding-the-icon-for-a-message"></a><span data-ttu-id="d5d95-103">メッセージのアイコンを検索します。</span><span class="sxs-lookup"><span data-stu-id="d5d95-103">Finding the Icon for a Message</span></span>

  
  
<span data-ttu-id="d5d95-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d5d95-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="d5d95-105">**メッセージに関連付けられているアイコンを検索するには**</span><span class="sxs-lookup"><span data-stu-id="d5d95-105">**To find the icon associated with a message**</span></span>
  
1. <span data-ttu-id="d5d95-106">その**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) のプロパティを取得するために、メッセージの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d5d95-106">Call the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="d5d95-107">**IMAPIFormMgr**インターフェイス ポインターを取得するために[MAPIOpenFormMgr](mapiopenformmgr.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d5d95-107">Call [MAPIOpenFormMgr](mapiopenformmgr.md) to retrieve an **IMAPIFormMgr** interface pointer.</span></span> <span data-ttu-id="d5d95-108">_PSession_パラメーターで、 **IMAPISession**ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="d5d95-108">Pass your **IMAPISession** pointer in the  _pSession_ parameter.</span></span> 
    
3. <span data-ttu-id="d5d95-109">**IMAPIFormInfo**インターフェイス ポインターを取得するために[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d5d95-109">Call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) to retrieve an **IMAPIFormInfo** interface pointer.</span></span> 
    
4. <span data-ttu-id="d5d95-110">**IMAPIFormInfo**ポインターを使用して、 [IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出すし、 **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) や**PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="d5d95-110">Use the **IMAPIFormInfo** pointer to call [IMAPIProp::GetProps](imapiprop-getprops.md) and retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and/or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties.</span></span> 
    

