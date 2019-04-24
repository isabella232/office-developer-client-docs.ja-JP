---
title: PidNameExchangeJunkEmailMoveStamp 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameExchangeJunkEmailMoveStamp
api_type:
- COM
ms.assetid: 7a52f46c-371c-46d0-8d66-e154482e8269
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 07acfd8715dccad8833ee14ac8e573fb995539ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337948"
---
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a><span data-ttu-id="eebba-103">PidNameExchangeJunkEmailMoveStamp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eebba-103">PidNameExchangeJunkEmailMoveStamp Canonical Property</span></span>

  
  
<span data-ttu-id="eebba-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eebba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eebba-105">メッセージが既に処理されているか、または安全なので、メッセージがスパムフィルターによって処理されないことを示す永続的なメッセージ値が格納されています。</span><span class="sxs-lookup"><span data-stu-id="eebba-105">Contains the persisted message value that indicates that the message should not be processed by a spam filter because the message was either already processed or is safe.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eebba-106">フレンドリ名:</span><span class="sxs-lookup"><span data-stu-id="eebba-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="eebba-107">なし</span><span class="sxs-lookup"><span data-stu-id="eebba-107">None</span></span>  <br/> |
|<span data-ttu-id="eebba-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="eebba-108">Property set:</span></span>  <br/> |<span data-ttu-id="eebba-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="eebba-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="eebba-110">プロパティ名:</span><span class="sxs-lookup"><span data-stu-id="eebba-110">Property name:</span></span>  <br/> |https://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|<span data-ttu-id="eebba-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="eebba-111">Data type:</span></span>  <br/> |<span data-ttu-id="eebba-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="eebba-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="eebba-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="eebba-113">Area:</span></span>  <br/> |<span data-ttu-id="eebba-114">セキュリティで保護されたメッセージング</span><span class="sxs-lookup"><span data-stu-id="eebba-114">Secure messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eebba-115">解説</span><span class="sxs-lookup"><span data-stu-id="eebba-115">Remarks</span></span>

<span data-ttu-id="eebba-116">このプロパティは、迷惑メールルールによって移動されるすべてのメッセージ、または信頼できるコンテンツとしてスタンプされます。</span><span class="sxs-lookup"><span data-stu-id="eebba-116">This property is stamped on every message that is moved by the Junk E-Mail Rule or is otherwise trusted content.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="eebba-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="eebba-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eebba-118">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="eebba-118">Protocol specifications</span></span>

<span data-ttu-id="eebba-119">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eebba-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eebba-120">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="eebba-120">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eebba-121">[[OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eebba-121">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eebba-122">許可/ブロックリストの処理と、迷惑メールメッセージの決定を有効にします。</span><span class="sxs-lookup"><span data-stu-id="eebba-122">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="eebba-123">[[OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eebba-123">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eebba-124">RSS アイテムを表すプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="eebba-124">Specifies the properties and operations that represent RSS items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eebba-125">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="eebba-125">Header files</span></span>

<span data-ttu-id="eebba-126">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eebba-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="eebba-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="eebba-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eebba-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="eebba-128">See also</span></span>



[<span data-ttu-id="eebba-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="eebba-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eebba-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eebba-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eebba-131">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="eebba-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eebba-132">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="eebba-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

