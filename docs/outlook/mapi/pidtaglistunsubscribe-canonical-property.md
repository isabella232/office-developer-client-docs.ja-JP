---
title: PidTagListUnsubscribe 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListUnsubscribe
api_type:
- HeaderDef
ms.assetid: 4e6bfbc7-7586-43cc-9380-daa0fe3d85a5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e057ab2ca0c75d5c0d749ebde8f1bdfb4f1ae66a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278880"
---
# <a name="pidtaglistunsubscribe-canonical-property"></a><span data-ttu-id="54249-103">PidTagListUnsubscribe 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="54249-103">PidTagListUnsubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="54249-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54249-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54249-105">マルチパーパスインターネットメール内線 (MIME) メッセージのリスト購読のヘッダーフィールドの値を格納します。</span><span class="sxs-lookup"><span data-stu-id="54249-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Unsubscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="54249-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="54249-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="54249-107">PR_LIST_UNSUBSCRIBE、PR_LIST_UNSUBSCRIBE_A、PR_LIST_UNSUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="54249-107">PR_LIST_UNSUBSCRIBE, PR_LIST_UNSUBSCRIBE_A, PR_LIST_UNSUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="54249-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="54249-108">Identifier:</span></span>  <br/> |<span data-ttu-id="54249-109">0x1045</span><span class="sxs-lookup"><span data-stu-id="54249-109">0x1045</span></span>  <br/> |
|<span data-ttu-id="54249-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="54249-110">Data type:</span></span>  <br/> |<span data-ttu-id="54249-111">PT_STRING8、PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="54249-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="54249-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="54249-112">Area:</span></span>  <br/> |<span data-ttu-id="54249-113">その他</span><span class="sxs-lookup"><span data-stu-id="54249-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54249-114">解説</span><span class="sxs-lookup"><span data-stu-id="54249-114">Remarks</span></span>

<span data-ttu-id="54249-115">リストの購読取り消しヘッダーフィールドを生成するには、クライアントはこれらのプロパティを目的の値に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54249-115">To generate a List-Unsubscribe header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="54249-116">MIME ライターは、これらのプロパティの値をリスト購読中止ヘッダーフィールドにコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="54249-116">MIME writers must copy the value of these properties to the List-Unsubscribe header field.</span></span>
  
<span data-ttu-id="54249-117">これらのリストサーバーに関連するプロパティの値を設定するには、次の表で指定されているように、MIME クライアントはヘッダーフィールドを記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54249-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="54249-118">**Property**</span><span class="sxs-lookup"><span data-stu-id="54249-118">**Property**</span></span>|<span data-ttu-id="54249-119">**優先ヘッダーフィールド名**</span><span class="sxs-lookup"><span data-stu-id="54249-119">**Preferred header field name**</span></span>|<span data-ttu-id="54249-120">**代替ヘッダーフィールド名**</span><span class="sxs-lookup"><span data-stu-id="54249-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="54249-121">**PR_LIST_UNSUBSCRIBE**</span><span class="sxs-lookup"><span data-stu-id="54249-121">**PR_LIST_UNSUBSCRIBE**</span></span> <br/> |<span data-ttu-id="54249-122">リスト-登録解除</span><span class="sxs-lookup"><span data-stu-id="54249-122">List-Unsubscribe</span></span>  <br/> |<span data-ttu-id="54249-123">X-リスト-登録解除</span><span class="sxs-lookup"><span data-stu-id="54249-123">X-List-Unsubscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="54249-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="54249-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="54249-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="54249-125">Protocol specifications</span></span>

<span data-ttu-id="54249-126">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54249-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54249-127">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="54249-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="54249-128">[[OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="54249-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="54249-129">インターネット標準の電子メールの規則からメッセージオブジェクトに変換します。</span><span class="sxs-lookup"><span data-stu-id="54249-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="54249-130">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="54249-130">Header files</span></span>

<span data-ttu-id="54249-131">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="54249-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="54249-132">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="54249-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="54249-133">Mapitags</span><span class="sxs-lookup"><span data-stu-id="54249-133">Mapitags.h</span></span>
  
> <span data-ttu-id="54249-134">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="54249-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="54249-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="54249-135">See also</span></span>



[<span data-ttu-id="54249-136">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="54249-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="54249-137">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="54249-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="54249-138">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="54249-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="54249-139">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="54249-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

