---
title: mapisvc.inf [Default Services] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435321"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="f257d-103">mapisvc.inf [Default Services] セクション</span><span class="sxs-lookup"><span data-stu-id="f257d-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="f257d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f257d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f257d-105">**[default Services]** セクションには、既定のメッセージサービスとして選択されているすべてのメッセージサービスが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="f257d-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="f257d-106">これらの既定のメッセージサービスは、 **[services]** セクションにリストされているメッセージサービスのサブセットです。</span><span class="sxs-lookup"><span data-stu-id="f257d-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="f257d-107">プロファイル構成プログラムが既定のプロファイルを作成すると、このセクションのメッセージサービスが自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="f257d-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="f257d-108">これらのエントリは、次に示すように **[Services]** セクションのエントリと同じ形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="f257d-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="f257d-109">**[既定のサービス]**</span><span class="sxs-lookup"><span data-stu-id="f257d-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="f257d-110">_メッセージ-サービスセクション名_ =  _メッセージサービス名_</span><span class="sxs-lookup"><span data-stu-id="f257d-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="f257d-111">前の図に示したように、mapisvc.inf の **[Default Services]** セクションには次のエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f257d-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


