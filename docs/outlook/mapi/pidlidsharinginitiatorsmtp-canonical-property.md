---
title: PidLidSharingInitiatorSmtp の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 188424fc67534ea5df6ed5eb209909731e12c73c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802163"
---
# <a name="pidlidsharinginitiatorsmtp-canonical-property"></a><span data-ttu-id="b7132-103">PidLidSharingInitiatorSmtp の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="b7132-103">PidLidSharingInitiatorSmtp Canonical Property</span></span>

  
  
<span data-ttu-id="b7132-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7132-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7132-105">共有メッセージを開始したユーザーの SMTP アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="b7132-105">Specifies the SMTP address of the user who initiated the sharing message.</span></span> <span data-ttu-id="b7132-106">これは、共有メッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="b7132-106">This is a property of a sharing message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7132-107">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="b7132-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="b7132-108">dispidSharingInitiatorSmtp</span><span class="sxs-lookup"><span data-stu-id="b7132-108">dispidSharingInitiatorSmtp</span></span>  <br/> |
|<span data-ttu-id="b7132-109">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="b7132-109">Property set:</span></span>  <br/> |<span data-ttu-id="b7132-110">PSETID_Sharing</span><span class="sxs-lookup"><span data-stu-id="b7132-110">PSETID_Sharing</span></span>  <br/> |
|<span data-ttu-id="b7132-111">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="b7132-111">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b7132-112">0x00008A08</span><span class="sxs-lookup"><span data-stu-id="b7132-112">0x00008A08</span></span>  <br/> |
|<span data-ttu-id="b7132-113">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="b7132-113">Data type:</span></span>  <br/> |<span data-ttu-id="b7132-114">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b7132-114">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b7132-115">領域:</span><span class="sxs-lookup"><span data-stu-id="b7132-115">Area:</span></span>  <br/> |<span data-ttu-id="b7132-116">共有</span><span class="sxs-lookup"><span data-stu-id="b7132-116">Sharing</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7132-117">備考</span><span class="sxs-lookup"><span data-stu-id="b7132-117">Remarks</span></span>

<span data-ttu-id="b7132-118">このプロパティは、 **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) のプロパティで指定されたアドレス帳から**PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) プロパティの値を設定する必要があり。、必要があります。無視されます。</span><span class="sxs-lookup"><span data-stu-id="b7132-118">This property must be set to the value of the **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) property from the Address Book identified by the **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) property and should be ignored.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b7132-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b7132-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b7132-120">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="b7132-120">Protocol specifications</span></span>

<span data-ttu-id="b7132-121">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7132-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7132-122">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7132-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b7132-123">[[MS OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b7132-123">[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b7132-124">クライアント間でのメールボックスのフォルダーを共有します。</span><span class="sxs-lookup"><span data-stu-id="b7132-124">Shares mailbox folders between clients.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b7132-125">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="b7132-125">Header files</span></span>

<span data-ttu-id="b7132-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b7132-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b7132-127">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b7132-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b7132-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="b7132-128">See also</span></span>



[<span data-ttu-id="b7132-129">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7132-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b7132-130">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="b7132-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b7132-131">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="b7132-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b7132-132">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="b7132-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

