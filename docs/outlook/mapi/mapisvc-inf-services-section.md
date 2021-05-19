---
title: MapiSvc.inf [Services] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e5bf5242ef673976ebda928d6ce4862e3e7dd072
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434782"
---
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="010a9-103">MapiSvc.inf [Services] セクション</span><span class="sxs-lookup"><span data-stu-id="010a9-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="010a9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="010a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="010a9-105">[ **サービス] セクションには** 、コンピューターにインストールされているメッセージ サービスが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="010a9-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="010a9-106">このセクションのエントリでは、次の形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="010a9-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="010a9-107">**[サービス]**</span><span class="sxs-lookup"><span data-stu-id="010a9-107">**[Services]**</span></span>
  
 <span data-ttu-id="010a9-108">_message-service セクション名_  =  _メッセージ サービス名_</span><span class="sxs-lookup"><span data-stu-id="010a9-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="010a9-109">message-service セクション名は、mapisvc.inf の他の場所にあるサービスの対応するセクションにこのエントリをリンクするメッセージ サービスによって定義される文字列です。</span><span class="sxs-lookup"><span data-stu-id="010a9-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="010a9-110">メッセージ サービス名は、インストールされているサービスの名前です。</span><span class="sxs-lookup"><span data-stu-id="010a9-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="010a9-111">次のセクションでは、既定のアドレス帳、自分のサービス、およびメッセージ ストア サービスの 3 つのメッセージ サービスを示します。</span><span class="sxs-lookup"><span data-stu-id="010a9-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="010a9-112">これらのサービスは架空の、説明のみを目的とします。</span><span class="sxs-lookup"><span data-stu-id="010a9-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="010a9-113">各メッセージ サービスの実装者は、このセクションのメッセージ サービスの適切なエントリを置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="010a9-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="010a9-114">このセクションの各エントリには、メッセージ サービスの情報が格納される独自の対応するセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="010a9-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="010a9-115">たとえば、既定のアドレス帳の対応するセクションは [AB] と呼ばれる。</span><span class="sxs-lookup"><span data-stu-id="010a9-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

