---
title: PidLidSharingInitiatorSmtp 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorSmtp
api_type:
- COM
ms.assetid: 4fb7d91d-4c51-41c1-9cb6-7b837dd12f11
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: eb699b2312064f8ed330238962dd86992c046139
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337122"
---
# <a name="pidlidsharinginitiatorsmtp-canonical-property"></a><span data-ttu-id="a89f2-103">PidLidSharingInitiatorSmtp 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a89f2-103">PidLidSharingInitiatorSmtp Canonical Property</span></span>

  
  
<span data-ttu-id="a89f2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a89f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a89f2-105">共有メッセージを開始したユーザーの SMTP アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="a89f2-105">Specifies the SMTP address of the user who initiated the sharing message.</span></span> <span data-ttu-id="a89f2-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="a89f2-106">This is a property of a sharing message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a89f2-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="a89f2-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="a89f2-108">dispidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="a89f2-108">dispidSharingInitiatorSmtp</span></span>  <br/> |
|<span data-ttu-id="a89f2-109">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="a89f2-109">Property set:</span></span>  <br/> |<span data-ttu-id="a89f2-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="a89f2-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="a89f2-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="a89f2-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a89f2-112">0x00008A08</span><span class="sxs-lookup"><span data-stu-id="a89f2-112">0x00008A08</span></span>  <br/> |
|<span data-ttu-id="a89f2-113">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="a89f2-113">Data type:</span></span>  <br/> |<span data-ttu-id="a89f2-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a89f2-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a89f2-115">エリア:</span><span class="sxs-lookup"><span data-stu-id="a89f2-115">Area:</span></span>  <br/> |<span data-ttu-id="a89f2-116">共有</span><span class="sxs-lookup"><span data-stu-id="a89f2-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a89f2-117">注釈</span><span class="sxs-lookup"><span data-stu-id="a89f2-117">Remarks</span></span>

<span data-ttu-id="a89f2-118">このプロパティは **、dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) プロパティで識別されるアドレス帳の **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) プロパティの値に設定する必要があります。無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a89f2-118">This property must be set to the value of the **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) property from the Address Book identified by the **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a89f2-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a89f2-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a89f2-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a89f2-120">Protocol specifications</span></span>

<span data-ttu-id="a89f2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a89f2-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a89f2-122">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="a89f2-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a89f2-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a89f2-123">[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a89f2-124">クライアント間でメールボックス フォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="a89f2-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a89f2-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a89f2-125">Header files</span></span>

<span data-ttu-id="a89f2-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a89f2-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a89f2-127">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a89f2-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a89f2-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="a89f2-128">See also</span></span>



[<span data-ttu-id="a89f2-129">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="a89f2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a89f2-130">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a89f2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a89f2-131">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a89f2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a89f2-132">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="a89f2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

