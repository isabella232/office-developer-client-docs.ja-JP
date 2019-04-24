---
title: mapisvc.inf [Services] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e5bf5242ef673976ebda928d6ce4862e3e7dd072
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270022"
---
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="5f328-103">mapisvc.inf [Services] セクション</span><span class="sxs-lookup"><span data-stu-id="5f328-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="5f328-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f328-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f328-105">**[Services]** セクションには、コンピューターにインストールされているメッセージサービスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5f328-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="5f328-106">このセクションのエントリは、次の形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="5f328-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="5f328-107">**サービス**</span><span class="sxs-lookup"><span data-stu-id="5f328-107">**[Services]**</span></span>
  
 <span data-ttu-id="5f328-108">_メッセージ-サービスセクション名_ =  _メッセージサービス名_</span><span class="sxs-lookup"><span data-stu-id="5f328-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="5f328-109">メッセージサービスセクション名は、このエントリを mapisvc.inf 内の他の場所にあるサービスの対応するセクションにリンクするメッセージサービスによって定義された文字列です。</span><span class="sxs-lookup"><span data-stu-id="5f328-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="5f328-110">メッセージサービス名は、インストールされているサービスの名前です。</span><span class="sxs-lookup"><span data-stu-id="5f328-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="5f328-111">次のセクションでは、既定のアドレス帳、独自のサービス、およびメッセージストアサービスという3つのメッセージサービスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5f328-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="5f328-112">これらのサービスは架空のものであり、説明のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="5f328-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="5f328-113">各メッセージサービスの実装者は、このセクションでメッセージサービスの適切なエントリを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5f328-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="5f328-114">このセクションの各エントリには、メッセージサービスの情報が格納されている場所に対応するセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="5f328-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="5f328-115">たとえば、既定のアドレス帳の対応するセクションは [AB] と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="5f328-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

