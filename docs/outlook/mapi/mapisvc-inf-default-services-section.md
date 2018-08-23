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
ms.openlocfilehash: a7270bce12f6d91dbb5632f739f4644df866924d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573146"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="8423c-103">MapiSvc.inf [Default Services] セクション</span><span class="sxs-lookup"><span data-stu-id="8423c-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="8423c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8423c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8423c-105">**[既定のサービス]** セクションには、すべてのメッセージ サービスの既定値として選択されているメッセージ サービスが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="8423c-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="8423c-106">これらの既定メッセージ サービスは、 **[サービス]** セクションに記載されているメッセージ サービスのサブセットです。</span><span class="sxs-lookup"><span data-stu-id="8423c-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="8423c-107">プロファイルの構成プログラムは、既定のプロファイルを作成する場合、このセクションのメッセージ サービスは、自動的に含まれています。</span><span class="sxs-lookup"><span data-stu-id="8423c-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="8423c-108">エントリに示すように次のよう、 **[サービス]** セクションのエントリとして同じ形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="8423c-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="8423c-109">**[既定のサービス]**</span><span class="sxs-lookup"><span data-stu-id="8423c-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="8423c-110">_メッセージ サービス セクション名_ =  _メッセージ サービス名_</span><span class="sxs-lookup"><span data-stu-id="8423c-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="8423c-111">次のエントリは、mapisvc.inf の前の図に示すように **[サービスの既定値]** セクションに含まれます。</span><span class="sxs-lookup"><span data-stu-id="8423c-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


