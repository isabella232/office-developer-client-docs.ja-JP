---
title: コンテナーの一時テーブルを実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 83351e18750ccbffbe60c4e19f9b04a9c94a42e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800909"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="4dc88-103">コンテナーの一時テーブルを実装します。</span><span class="sxs-lookup"><span data-stu-id="4dc88-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="4dc88-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4dc88-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4dc88-105">コンテナーの 1 つに属している一時テーブルにアクセスするには、MAPI は**IMAPITable**と**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティを開くには、コンテナーの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="4dc88-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="4dc88-106">コンテナーがクライアント アプリケーションでコンテナーに受信者を追加しようとするときに、一時テーブルを取得しようとしています。</span><span class="sxs-lookup"><span data-stu-id="4dc88-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="4dc88-107">コンテナーは、いずれかの受信者を許可している場合、プロバイダー独自のテーブルの実装を返すか、MAPI 実装を取得する[IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4dc88-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="4dc88-108">コンテナーの一時テーブル内のテンプレートのセットは、特定のコンテナーが保持できる受信者の種類を反映します。</span><span class="sxs-lookup"><span data-stu-id="4dc88-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="4dc88-109">通常、1 つまたは 2 つのテンプレート、個々 のメッセージングのユーザーまたは配布リストを作成するためのテンプレートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4dc88-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="4dc88-110">**PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) と**PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) のプロパティ] では、これらのテンプレートのエントリ id が保持されます。</span><span class="sxs-lookup"><span data-stu-id="4dc88-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="4dc88-111">ただし、コンテナーでは、これらの種類のエントリに限定されるわけではありませんです。</span><span class="sxs-lookup"><span data-stu-id="4dc88-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="4dc88-112">受信者または受信者以外のエントリは、ディレクトリなどの他の種類が格納できます。</span><span class="sxs-lookup"><span data-stu-id="4dc88-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

