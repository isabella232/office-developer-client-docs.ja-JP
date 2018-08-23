---
title: PidTagExceptionStartTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExceptionStartTime
api_type:
- HeaderDef
ms.assetid: 3aa4f9d7-8105-435d-af68-424a079e1a84
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fbbd261558cf75458e69371e7fb53857e0692e74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802740"
---
# <a name="pidtagexceptionstarttime-canonical-property"></a><span data-ttu-id="7cf49-103">PidTagExceptionStartTime 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="7cf49-103">PidTagExceptionStartTime Canonical Property</span></span>

  
  
<span data-ttu-id="7cf49-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7cf49-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7cf49-105">例外が作成されると、開始の日付と時刻、コンピューターのローカル タイム ゾーンの例外を示します。</span><span class="sxs-lookup"><span data-stu-id="7cf49-105">Indicates the start date and time of the exception in the local time zone of the machine when the exception is created.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7cf49-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="7cf49-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7cf49-107">PR_EXCEPTION_STARTTIME</span><span class="sxs-lookup"><span data-stu-id="7cf49-107">PR_EXCEPTION_STARTTIME</span></span>  <br/> |
|<span data-ttu-id="7cf49-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7cf49-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7cf49-109">0x7FFB</span><span class="sxs-lookup"><span data-stu-id="7cf49-109">0x7FFB</span></span>  <br/> |
|<span data-ttu-id="7cf49-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="7cf49-110">Data type:</span></span>  <br/> |<span data-ttu-id="7cf49-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7cf49-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7cf49-112">領域:</span><span class="sxs-lookup"><span data-stu-id="7cf49-112">Area:</span></span>  <br/> |<span data-ttu-id="7cf49-113">クラスによって定義されたメッセージの転送を可能な</span><span class="sxs-lookup"><span data-stu-id="7cf49-113">Message class-defined non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7cf49-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7cf49-114">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="7cf49-115">このプロパティは、情報提供する必要がありますがサポートされていない重要な情報にします。</span><span class="sxs-lookup"><span data-stu-id="7cf49-115">This property is informational and must not be relied on for critical information.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7cf49-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7cf49-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7cf49-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7cf49-117">Protocol specifications</span></span>

<span data-ttu-id="7cf49-118">[[MS OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7cf49-118">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7cf49-119">プロパティや予定、会議出席依頼および応答メッセージの動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="7cf49-119">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7cf49-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7cf49-120">Header files</span></span>

<span data-ttu-id="7cf49-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7cf49-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="7cf49-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7cf49-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="7cf49-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7cf49-123">Mapitags.h</span></span>
  
> <span data-ttu-id="7cf49-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7cf49-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7cf49-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="7cf49-125">See also</span></span>



[<span data-ttu-id="7cf49-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7cf49-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7cf49-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7cf49-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7cf49-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7cf49-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7cf49-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="7cf49-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

