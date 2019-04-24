---
title: PidTagControlId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b27f59e0bfdcac8eca1751af2f07139f12e2b3a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334742"
---
# <a name="pidtagcontrolid-canonical-property"></a><span data-ttu-id="379fd-103">PidTagControlId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="379fd-103">PidTagControlId Canonical Property</span></span>

  
  
<span data-ttu-id="379fd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="379fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="379fd-105">ダイアログボックスで使用されるコントロールの一意識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="379fd-105">Contains a unique identifier for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="379fd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="379fd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="379fd-107">PR_CONTROL_ID</span><span class="sxs-lookup"><span data-stu-id="379fd-107">PR_CONTROL_ID</span></span>  <br/> |
|<span data-ttu-id="379fd-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="379fd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="379fd-109">0x3f07</span><span class="sxs-lookup"><span data-stu-id="379fd-109">0x3F07</span></span>  <br/> |
|<span data-ttu-id="379fd-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="379fd-110">Data type:</span></span>  <br/> |<span data-ttu-id="379fd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="379fd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="379fd-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="379fd-112">Area:</span></span>  <br/> |<span data-ttu-id="379fd-113">MAPI 表示テーブル</span><span class="sxs-lookup"><span data-stu-id="379fd-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="379fd-114">解説</span><span class="sxs-lookup"><span data-stu-id="379fd-114">Remarks</span></span>

<span data-ttu-id="379fd-115">このプロパティには、コントロールの一意の識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="379fd-115">This property contains a unique identifier for the control.</span></span> <span data-ttu-id="379fd-116">この識別子には、 [GUID](guid.md)構造と、 **LONG**型のバイナリ値を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="379fd-116">This identifier should contain a [GUID](guid.md) structure and a binary value of type **LONG**.</span></span> <span data-ttu-id="379fd-117">ダイアログボックス内のすべてのコントロールは、同じ**GUID**を使用してサービスプロバイダーを識別する必要があり、各コントロールは固有の**LONG**値を使用して、コントロールが競合しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="379fd-117">All controls in the dialog box should use the same **GUID** to identify the service provider, and each control should use a unique **LONG** value to ensure that the controls do not collide.</span></span> 
  
<span data-ttu-id="379fd-118">このプロパティは通知で使用されます。</span><span class="sxs-lookup"><span data-stu-id="379fd-118">This property is used in notifications.</span></span> <span data-ttu-id="379fd-119">たとえば、表示テーブルで送信された通知では、更新するコントロールを一意に識別するために、このプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="379fd-119">For example, notifications sent on the display table must set this property to uniquely identify the control to update.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="379fd-120">関連リソース</span><span class="sxs-lookup"><span data-stu-id="379fd-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="379fd-121">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="379fd-121">Header files</span></span>

<span data-ttu-id="379fd-122">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="379fd-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="379fd-123">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="379fd-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="379fd-124">Mapitags</span><span class="sxs-lookup"><span data-stu-id="379fd-124">Mapitags.h</span></span>
  
> <span data-ttu-id="379fd-125">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="379fd-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="379fd-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="379fd-126">See also</span></span>



[<span data-ttu-id="379fd-127">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="379fd-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="379fd-128">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="379fd-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="379fd-129">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="379fd-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="379fd-130">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="379fd-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

