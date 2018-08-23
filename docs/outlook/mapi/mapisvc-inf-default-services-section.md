---
title: MapiSvc.inf [Default Services] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5d860135d846df8ef1ea0784d7430c71ad0fe64e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801526"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="72eed-103">MapiSvc.inf [Default Services] セクション</span><span class="sxs-lookup"><span data-stu-id="72eed-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="72eed-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72eed-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72eed-105">**[既定のサービス]** セクションには、すべてのメッセージ サービスの既定値として選択されているメッセージ サービスが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="72eed-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="72eed-106">これらの既定メッセージ サービスは、 **[サービス]** セクションに記載されているメッセージ サービスのサブセットです。</span><span class="sxs-lookup"><span data-stu-id="72eed-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="72eed-107">プロファイルの構成プログラムは、既定のプロファイルを作成する場合、このセクションのメッセージ サービスは、自動的に含まれています。</span><span class="sxs-lookup"><span data-stu-id="72eed-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="72eed-108">エントリに示すように次のよう、 **[サービス]** セクションのエントリとして同じ形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="72eed-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="72eed-109">**[既定のサービス]**</span><span class="sxs-lookup"><span data-stu-id="72eed-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="72eed-110">_メッセージ サービス セクション名_ =  _メッセージ サービス名_</span><span class="sxs-lookup"><span data-stu-id="72eed-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="72eed-111">次のエントリは、mapisvc.inf の前の図に示すように **[サービスの既定値]** セクションに含まれます。</span><span class="sxs-lookup"><span data-stu-id="72eed-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


