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
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="07a00-103">PidTagDefCreateMailuser 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="07a00-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="07a00-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07a00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07a00-105">既定のメッセージングユーザーオブジェクトのテンプレートエントリ識別子を含みます。</span><span class="sxs-lookup"><span data-stu-id="07a00-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07a00-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="07a00-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="07a00-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="07a00-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="07a00-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="07a00-108">Identifier:</span></span>  <br/> |<span data-ttu-id="07a00-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="07a00-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="07a00-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="07a00-110">Data type:</span></span>  <br/> |<span data-ttu-id="07a00-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="07a00-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="07a00-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="07a00-112">Area:</span></span>  <br/> |<span data-ttu-id="07a00-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="07a00-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07a00-114">注釈</span><span class="sxs-lookup"><span data-stu-id="07a00-114">Remarks</span></span>

<span data-ttu-id="07a00-115">クライアントアプリケーションは、このプロパティを使用して、コンテナー内にメッセージングユーザーオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="07a00-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="07a00-116">エントリ作成のサポートは、アドレス帳コンテナーでは省略可能です。これをサポートしていないものは、このプロパティを公開する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="07a00-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="07a00-117">このプロパティは、メッセージングユーザーの**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) プロパティに表示できるエントリを指定します。</span><span class="sxs-lookup"><span data-stu-id="07a00-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="07a00-118">識別子を取得した後、クライアントは[IABContainer:: createentry](iabcontainer-createentry.md)メソッドへの呼び出しでその識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="07a00-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="07a00-119">このエントリは、既定のメッセージングユーザーのテンプレートを表します。</span><span class="sxs-lookup"><span data-stu-id="07a00-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="07a00-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="07a00-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="07a00-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="07a00-121">Header files</span></span>

<span data-ttu-id="07a00-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="07a00-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="07a00-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="07a00-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="07a00-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="07a00-124">Mapitags.h</span></span>
  
> <span data-ttu-id="07a00-125">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="07a00-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07a00-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="07a00-126">See also</span></span>



[<span data-ttu-id="07a00-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="07a00-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="07a00-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="07a00-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="07a00-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="07a00-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="07a00-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="07a00-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

