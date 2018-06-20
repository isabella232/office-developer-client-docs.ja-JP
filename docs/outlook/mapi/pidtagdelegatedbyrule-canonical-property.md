---
title: PidTagDelegatedByRule の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegatedByRule
api_type:
- HeaderDef
ms.assetid: 284b5001-5de6-4c4e-8e5c-0593ae1b301f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d851f5cfa2697ea2a81f80c90e8051c59172d549
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802660"
---
# <a name="pidtagdelegatedbyrule-canonical-property"></a><span data-ttu-id="c2d2d-103">PidTagDelegatedByRule の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="c2d2d-103">PidTagDelegatedByRule Canonical Property</span></span>

  
  
<span data-ttu-id="c2d2d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c2d2d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c2d2d-105">フォルダーのメッセージがルールによって委任されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="c2d2d-105">Indicates whether a folder's message is delegated by a rule.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c2d2d-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="c2d2d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c2d2d-107">PR_DELEGATED_BY_RULE</span><span class="sxs-lookup"><span data-stu-id="c2d2d-107">PR_DELEGATED_BY_RULE</span></span>  <br/> |
|<span data-ttu-id="c2d2d-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="c2d2d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c2d2d-109">0x3FE3</span><span class="sxs-lookup"><span data-stu-id="c2d2d-109">0x3FE3</span></span>  <br/> |
|<span data-ttu-id="c2d2d-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="c2d2d-110">Data type:</span></span>  <br/> |<span data-ttu-id="c2d2d-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c2d2d-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c2d2d-112">領域:</span><span class="sxs-lookup"><span data-stu-id="c2d2d-112">Area:</span></span>  <br/> |<span data-ttu-id="c2d2d-113">MAPI のステータス</span><span class="sxs-lookup"><span data-stu-id="c2d2d-113">MAPI status</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c2d2d-114">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c2d2d-114">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c2d2d-115">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c2d2d-115">Protocol specifications</span></span>

<span data-ttu-id="c2d2d-116">[[MS OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2d2d-116">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2d2d-117">接続し、別のユーザーに代わって動作する場合は、デリゲート、およびメッセージと予定表のオブジェクトとの対話としてメールボックスを構成するためのメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="c2d2d-117">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="c2d2d-118">[[MS OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c2d2d-118">[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c2d2d-119">サーバー上の受信電子メール メッセージを操作します。</span><span class="sxs-lookup"><span data-stu-id="c2d2d-119">Manipulates incoming email messages on a server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c2d2d-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c2d2d-120">Header files</span></span>

<span data-ttu-id="c2d2d-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c2d2d-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="c2d2d-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c2d2d-122">Provides data type definitions</span></span>
    
<span data-ttu-id="c2d2d-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c2d2d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="c2d2d-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c2d2d-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c2d2d-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="c2d2d-125">See also</span></span>



[<span data-ttu-id="c2d2d-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c2d2d-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c2d2d-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c2d2d-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c2d2d-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="c2d2d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c2d2d-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="c2d2d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

