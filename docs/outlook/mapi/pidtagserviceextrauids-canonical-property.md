---
title: PidTagServiceExtraUids の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 71f802014200d4b767c346c14df53f1193d44b0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803537"
---
# <a name="pidtagserviceextrauids-canonical-property"></a><span data-ttu-id="bbf30-103">PidTagServiceExtraUids の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="bbf30-103">PidTagServiceExtraUids Canonical Property</span></span>

  
  
<span data-ttu-id="bbf30-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bbf30-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bbf30-105">メッセージ サービスの追加のプロファイル セクションを識別する[MAPIUID](mapiuid.md)構造体の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bbf30-105">Contains a list of [MAPIUID](mapiuid.md) structures that identify additional profile sections for the message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bbf30-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="bbf30-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bbf30-107">PR_SERVICE_EXTRA_UIDS</span><span class="sxs-lookup"><span data-stu-id="bbf30-107">PR_SERVICE_EXTRA_UIDS</span></span>  <br/> |
|<span data-ttu-id="bbf30-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bbf30-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bbf30-109">0x3D0D</span><span class="sxs-lookup"><span data-stu-id="bbf30-109">0x3D0D</span></span>  <br/> |
|<span data-ttu-id="bbf30-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="bbf30-110">Data type:</span></span>  <br/> |<span data-ttu-id="bbf30-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbf30-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bbf30-112">領域:</span><span class="sxs-lookup"><span data-stu-id="bbf30-112">Area:</span></span>  <br/> |<span data-ttu-id="bbf30-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="bbf30-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbf30-114">備考</span><span class="sxs-lookup"><span data-stu-id="bbf30-114">Remarks</span></span>

<span data-ttu-id="bbf30-115">各メッセージ フィルターの新しいプロファイルのセクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="bbf30-115">New profile sections can be created for each message filter.</span></span> <span data-ttu-id="bbf30-116">メッセージ サービスについては、別のプロファイルにコピーするのには、それが同様のフィルターの追加のプロファイル セクションをコピーするのには重要です。</span><span class="sxs-lookup"><span data-stu-id="bbf30-116">When the information about the message service is to be copied to another profile, it is important to copy the additional profile sections for the filters as well.</span></span> <span data-ttu-id="bbf30-117">追加のプロファイル セクションを使用するサービス プロバイダーは、 **PR_SERVICE_EXTRA_UIDS**、その他のメッセージ サービスの情報をコピーするのには MAPI を使用するにこれらのプロファイル セクションの**MAPIUID**構造体を格納できます。</span><span class="sxs-lookup"><span data-stu-id="bbf30-117">A service provider that uses additional profile sections can store the **MAPIUID** structures of those profile sections in **PR_SERVICE_EXTRA_UIDS**, which allows MAPI to copy the additional message service information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bbf30-118">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bbf30-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bbf30-119">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bbf30-119">Header files</span></span>

<span data-ttu-id="bbf30-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bbf30-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="bbf30-121">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bbf30-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="bbf30-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bbf30-122">Mapitags.h</span></span>
  
> <span data-ttu-id="bbf30-123">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bbf30-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbf30-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="bbf30-124">See also</span></span>



[<span data-ttu-id="bbf30-125">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bbf30-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bbf30-126">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bbf30-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bbf30-127">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="bbf30-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bbf30-128">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="bbf30-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

