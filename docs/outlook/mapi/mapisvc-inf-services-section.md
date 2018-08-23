---
title: MapiSvc.inf [Services] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 520478061e192f9fec97c6b13edde7833a13a3d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571396"
---
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="de417-103">MapiSvc.inf [Services] セクション</span><span class="sxs-lookup"><span data-stu-id="de417-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="de417-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de417-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de417-105">**[サービス]** セクションには、コンピューターにインストールされているメッセージ サービスが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="de417-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="de417-106">このセクションのエントリは、次の形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="de417-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="de417-107">**[サービス]**</span><span class="sxs-lookup"><span data-stu-id="de417-107">**[Services]**</span></span>
  
 <span data-ttu-id="de417-108">_メッセージ サービス セクション名_ =  _メッセージ サービス名_</span><span class="sxs-lookup"><span data-stu-id="de417-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="de417-109">メッセージ サービスのセクション名は文字列定義メッセージ サービスでリンクしているこのエントリ mapisvc.inf の他の場所でサービスの対応するセクションです。</span><span class="sxs-lookup"><span data-stu-id="de417-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="de417-110">メッセージ サービス名は、インストールされているサービスの名前です。</span><span class="sxs-lookup"><span data-stu-id="de417-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="de417-111">次のセクションでは、3 つのメッセージ サービスを示しています: 既定のアドレス帳、自分独自のサービス、およびメッセージ ストアのサービスです。</span><span class="sxs-lookup"><span data-stu-id="de417-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="de417-112">これらのサービスは、例示目的でのみ、架空されています。</span><span class="sxs-lookup"><span data-stu-id="de417-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="de417-113">各メッセージ サービスの実装側は、ここで自分のメッセージ サービスの適切なエントリではなきます。</span><span class="sxs-lookup"><span data-stu-id="de417-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="de417-114">このセクションでは、各エントリには、メッセージ サービスの情報を格納する、独自の対応するセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="de417-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="de417-115">たとえば、既定のアドレス帳の対応するセクションは、[AB] と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="de417-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

