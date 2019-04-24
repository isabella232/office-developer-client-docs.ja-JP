---
title: PidTagMessageSecurityLabel 標準プロパティ
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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b6900cbacc2bea6c5519efdc4281ca98629b23bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355679"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a><span data-ttu-id="9fea9-103">PidTagMessageSecurityLabel 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9fea9-103">PidTagMessageSecurityLabel Canonical Property</span></span>

  
  
<span data-ttu-id="9fea9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fea9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fea9-105">メッセージのセキュリティラベルが保存されています。</span><span class="sxs-lookup"><span data-stu-id="9fea9-105">Contains a security label for a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9fea9-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9fea9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9fea9-107">PR_MESSAGE_SECURITY_LABEL</span><span class="sxs-lookup"><span data-stu-id="9fea9-107">PR_MESSAGE_SECURITY_LABEL</span></span>  <br/> |
|<span data-ttu-id="9fea9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="9fea9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9fea9-109">0x001e</span><span class="sxs-lookup"><span data-stu-id="9fea9-109">0x001E</span></span>  <br/> |
|<span data-ttu-id="9fea9-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9fea9-110">Data type:</span></span>  <br/> |<span data-ttu-id="9fea9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9fea9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9fea9-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="9fea9-112">Area:</span></span>  <br/> |<span data-ttu-id="9fea9-113">サーバー</span><span class="sxs-lookup"><span data-stu-id="9fea9-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fea9-114">解説</span><span class="sxs-lookup"><span data-stu-id="9fea9-114">Remarks</span></span>

<span data-ttu-id="9fea9-115">このプロパティは、 **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) プロパティがメッセージを保護する基準を指定します。</span><span class="sxs-lookup"><span data-stu-id="9fea9-115">This property provides the basis on which the **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) property protects a message.</span></span> <span data-ttu-id="9fea9-116">メッセージコンテンツとの関連付けは、トークンによって保証されます。</span><span class="sxs-lookup"><span data-stu-id="9fea9-116">Its association with the message content is guaranteed by the token.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9fea9-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="9fea9-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9fea9-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="9fea9-118">Header files</span></span>

<span data-ttu-id="9fea9-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9fea9-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="9fea9-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="9fea9-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="9fea9-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="9fea9-121">Mapitags.h</span></span>
  
> <span data-ttu-id="9fea9-122">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9fea9-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9fea9-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="9fea9-123">See also</span></span>



[<span data-ttu-id="9fea9-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="9fea9-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9fea9-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9fea9-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9fea9-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9fea9-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9fea9-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="9fea9-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

