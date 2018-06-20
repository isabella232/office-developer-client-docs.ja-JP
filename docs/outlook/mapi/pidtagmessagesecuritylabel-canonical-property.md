---
title: PidTagMessageSecurityLabel の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSecurityLabel
api_type:
- HeaderDef
ms.assetid: aae41f1b-19bb-40c7-8564-0c87a5a4e47c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 24cf7d8d7b025e5a013ce3a5c1bb03da5ae8a6a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802989"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="169bb-103">PidTagMessageSecurityLabel の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="169bb-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="169bb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="169bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="169bb-105">メッセージのセキュリティ ラベルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="169bb-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="169bb-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="169bb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="169bb-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="169bb-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="169bb-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="169bb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="169bb-109">0x001E</span><span class="sxs-lookup"><span data-stu-id="169bb-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="169bb-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="169bb-110">Data type:</span></span>  <br/> |<span data-ttu-id="169bb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="169bb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="169bb-112">領域:</span><span class="sxs-lookup"><span data-stu-id="169bb-112">Area:</span></span>  <br/> |<span data-ttu-id="169bb-113">Server</span><span class="sxs-lookup"><span data-stu-id="169bb-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="169bb-114">備考</span><span class="sxs-lookup"><span data-stu-id="169bb-114">Remarks</span></span>

<span data-ttu-id="169bb-115">このプロパティは、 **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) のプロパティがメッセージを保護する基盤を提供します。</span><span class="sxs-lookup"><span data-stu-id="169bb-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="169bb-116">トークンでは、メッセージの内容との関連が保証されます。</span><span class="sxs-lookup"><span data-stu-id="169bb-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="169bb-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="169bb-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="169bb-118">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="169bb-118">Header files</span></span>

<span data-ttu-id="169bb-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="169bb-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="169bb-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="169bb-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="169bb-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="169bb-121">Mapitags.h</span></span>
  
> <span data-ttu-id="169bb-122">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="169bb-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="169bb-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="169bb-123">See also</span></span>



[<span data-ttu-id="169bb-124">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="169bb-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="169bb-125">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="169bb-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="169bb-126">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="169bb-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="169bb-127">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="169bb-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

