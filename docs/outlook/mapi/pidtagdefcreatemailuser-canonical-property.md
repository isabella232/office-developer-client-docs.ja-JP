---
title: PidTagDefCreateMailuser の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 33c62b81982aaac3659ad4d41ea2cf5298b42287
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802667"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a><span data-ttu-id="31112-103">PidTagDefCreateMailuser の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="31112-103">PidTagDefCreateMailuser Canonical Property</span></span>

  
  
<span data-ttu-id="31112-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="31112-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="31112-105">ユーザー オブジェクトのメッセージングの既定のテンプレートのエントリ id が含まれています。</span><span class="sxs-lookup"><span data-stu-id="31112-105">Contains the template entry identifier for a default messaging user object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31112-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="31112-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="31112-107">PR_DEF_CREATE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="31112-107">PR_DEF_CREATE_MAILUSER</span></span>  <br/> |
|<span data-ttu-id="31112-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="31112-108">Identifier:</span></span>  <br/> |<span data-ttu-id="31112-109">0x3612</span><span class="sxs-lookup"><span data-stu-id="31112-109">0x3612</span></span>  <br/> |
|<span data-ttu-id="31112-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="31112-110">Data type:</span></span>  <br/> |<span data-ttu-id="31112-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="31112-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="31112-112">領域:</span><span class="sxs-lookup"><span data-stu-id="31112-112">Area:</span></span>  <br/> |<span data-ttu-id="31112-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="31112-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31112-114">備考</span><span class="sxs-lookup"><span data-stu-id="31112-114">Remarks</span></span>

<span data-ttu-id="31112-115">クライアント アプリケーションでは、このプロパティを使用して、コンテナー内のメッセージングのユーザー オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="31112-115">Client applications use this property to create a messaging user object within a container.</span></span> <span data-ttu-id="31112-116">エントリの作成のサポートはオプションのアドレス帳コンテナーです。サポートしていないものは、このプロパティを公開する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="31112-116">Support of entry creation is optional for address book containers; those that do not support it are not required to expose this property.</span></span> 
  
<span data-ttu-id="31112-117">このプロパティでは、メッセージング ユーザーの**PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) のプロパティで表示可能なエントリを指定します。</span><span class="sxs-lookup"><span data-stu-id="31112-117">This property specifies an entry that can appear in the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property for messaging users.</span></span> <span data-ttu-id="31112-118">Id を入手すると、クライアントは、それを[IABContainer::CreateEntry](iabcontainer-createentry.md)メソッドの呼び出しで使用します。</span><span class="sxs-lookup"><span data-stu-id="31112-118">After obtaining the identifier, the client uses it in a call to the [IABContainer::CreateEntry](iabcontainer-createentry.md) method.</span></span> <span data-ttu-id="31112-119">エントリは、既定のメッセージング ユーザーのテンプレートを表します。</span><span class="sxs-lookup"><span data-stu-id="31112-119">The entry represents the template for the default messaging user.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="31112-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="31112-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="31112-121">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="31112-121">Header files</span></span>

<span data-ttu-id="31112-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="31112-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="31112-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="31112-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="31112-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="31112-124">Mapitags.h</span></span>
  
> <span data-ttu-id="31112-125">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="31112-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31112-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="31112-126">See also</span></span>



[<span data-ttu-id="31112-127">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="31112-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="31112-128">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="31112-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="31112-129">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="31112-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="31112-130">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="31112-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

