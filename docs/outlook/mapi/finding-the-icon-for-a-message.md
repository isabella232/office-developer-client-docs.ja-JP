---
title: メッセージのアイコンの検索
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80a97c3d-4bca-4819-9da4-ca0fbf3a686f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b351cc68e3c3d9f9c01acb4b3d0e52158e302d7a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409154"
---
# <a name="finding-the-icon-for-a-message"></a><span data-ttu-id="e0173-103">メッセージのアイコンの検索</span><span class="sxs-lookup"><span data-stu-id="e0173-103">Finding the Icon for a Message</span></span>

  
  
<span data-ttu-id="e0173-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0173-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e0173-105">**メッセージに関連付けられているアイコンを見つけるには**</span><span class="sxs-lookup"><span data-stu-id="e0173-105">**To find the icon associated with a message**</span></span>
  
1. <span data-ttu-id="e0173-106">メッセージの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_MESSAGE_CLASS **(** [PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="e0173-106">Call the message's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="e0173-107">[MAPIOpenFormMgr を呼び](mapiopenformmgr.md)出して **IMAPIFormMgr インターフェイス ポインターを** 取得します。</span><span class="sxs-lookup"><span data-stu-id="e0173-107">Call [MAPIOpenFormMgr](mapiopenformmgr.md) to retrieve an **IMAPIFormMgr** interface pointer.</span></span> <span data-ttu-id="e0173-108">pSession パラメーター **で IMAPISession** ポインター  _を渡_ します。</span><span class="sxs-lookup"><span data-stu-id="e0173-108">Pass your **IMAPISession** pointer in the  _pSession_ parameter.</span></span> 
    
3. <span data-ttu-id="e0173-109">[IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md)を呼び出して **、IMAPIFormInfo** インターフェイス ポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="e0173-109">Call [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) to retrieve an **IMAPIFormInfo** interface pointer.</span></span> 
    
4. <span data-ttu-id="e0173-110">**IMAPIFormInfo** ポインターを使用して [IMAPIProp::GetProps](imapiprop-getprops.md)を呼び出し **、PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) プロパティまたは PR_MINI_ICON ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティ **を** 取得します。</span><span class="sxs-lookup"><span data-stu-id="e0173-110">Use the **IMAPIFormInfo** pointer to call [IMAPIProp::GetProps](imapiprop-getprops.md) and retrieve the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and/or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties.</span></span> 
    

