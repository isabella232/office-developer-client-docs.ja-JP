---
title: PidTagDefCreateMailuser 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cd09c85e4f44bbea29807d72a273ccf6980ca6df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407481"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="f95a9-103">PidTagDefCreateMailuser 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f95a9-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="f95a9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f95a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f95a9-105">既定のメッセージング ユーザー オブジェクトのテンプレート エントリ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="f95a9-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f95a9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="f95a9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f95a9-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="f95a9-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="f95a9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="f95a9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f95a9-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="f95a9-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="f95a9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="f95a9-110">Data type:</span></span>  <br/> |<span data-ttu-id="f95a9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f95a9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f95a9-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="f95a9-112">Area:</span></span>  <br/> |<span data-ttu-id="f95a9-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="f95a9-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f95a9-114">注釈</span><span class="sxs-lookup"><span data-stu-id="f95a9-114">Remarks</span></span>

<span data-ttu-id="f95a9-115">クライアント アプリケーションは、このプロパティを使用して、コンテナー内にメッセージング ユーザー オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="f95a9-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="f95a9-116">エントリの作成のサポートは、アドレス帳コンテナーではオプションです。このプロパティをサポートしていないユーザーは、このプロパティを公開する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f95a9-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="f95a9-117">このプロパティは、メッセージング ユーザーの PR_CREATE_TEMPLATES **(** [PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティに表示されるエントリを指定します。</span><span class="sxs-lookup"><span data-stu-id="f95a9-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="f95a9-118">識別子を取得した後、クライアントは [IABContainer::CreateEntry](iabcontainer-createentry.md) メソッドの呼び出しで識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="f95a9-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="f95a9-119">このエントリは、既定のメッセージング ユーザーのテンプレートを表します。</span><span class="sxs-lookup"><span data-stu-id="f95a9-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f95a9-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="f95a9-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f95a9-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="f95a9-121">Header files</span></span>

<span data-ttu-id="f95a9-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f95a9-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="f95a9-123">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="f95a9-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="f95a9-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f95a9-124">Mapitags.h</span></span>
  
> <span data-ttu-id="f95a9-125">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="f95a9-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f95a9-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="f95a9-126">See also</span></span>



[<span data-ttu-id="f95a9-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="f95a9-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f95a9-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f95a9-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f95a9-129">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f95a9-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f95a9-130">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="f95a9-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

