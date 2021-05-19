---
title: コンテナー テーブルのOne-Offする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417421"
---
# <a name="implementing-a-container-one-off-table"></a><span data-ttu-id="c1dd3-103">コンテナー テーブルのOne-Offする</span><span class="sxs-lookup"><span data-stu-id="c1dd3-103">Implementing a Container One-Off Table</span></span>

  
  
<span data-ttu-id="c1dd3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1dd3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1dd3-105">コンテナーの 1 つに属する 1 回のテーブルにアクセスするには、MAPI はコンテナーの [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して **、IMAPITable** インターフェイスを使用して **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="c1dd3-105">To access the one-off table belonging to one of your containers, MAPI calls the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property with the **IMAPITable** interface.</span></span> <span data-ttu-id="c1dd3-106">クライアント アプリケーションがコンテナーに受信者を追加しようとしている場合、コンテナーは 1 回きりテーブルを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1dd3-106">Your container is asked to return its one-off table when a client application is trying to add a recipient to the container.</span></span> <span data-ttu-id="c1dd3-107">コンテナーで受信者が許可されている場合、プロバイダーは独自のテーブル実装を返すか [、IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) を呼び出して MAPI 実装を返します。</span><span class="sxs-lookup"><span data-stu-id="c1dd3-107">If the container allows any recipients, your provider can either return its own table implementation or call [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) to return the MAPI implementation.</span></span> 
  
<span data-ttu-id="c1dd3-108">コンテナーの一時テーブル内のテンプレートのセットは、特定のコンテナーが保持できる受信者の種類を反映する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1dd3-108">The set of templates in the container one-off table should reflect the type of recipients that the particular container can hold.</span></span> <span data-ttu-id="c1dd3-109">通常、これには 1 つまたは 2 つのテンプレート、個々のメッセージング ユーザーまたは配布リストを作成するためのテンプレートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c1dd3-109">Typically, this includes one or two templates, templates for creating an individual messaging user or a distribution list.</span></span> <span data-ttu-id="c1dd3-110">これらのテンプレートのエントリ識別子は **、PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) および PR_DEF_CREATE_DL **(** [PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) プロパティに保持されます。</span><span class="sxs-lookup"><span data-stu-id="c1dd3-110">The entry identifiers for these templates are held in the **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) and **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) properties.</span></span> <span data-ttu-id="c1dd3-111">ただし、コンテナーは、これらの種類のエントリに限定されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="c1dd3-111">However, containers are by no means limited to these types of entries.</span></span> <span data-ttu-id="c1dd3-112">他の種類の受信者や、ディレクトリなどの受信者以外のエントリを保持できます。</span><span class="sxs-lookup"><span data-stu-id="c1dd3-112">They can hold other types of recipients or non-recipient entries such as directories.</span></span> 
  

