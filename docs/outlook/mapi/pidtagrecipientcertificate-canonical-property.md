---
title: PidTagRecipientCertificate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientCertificate
api_type:
- COM
ms.assetid: 7c5c749e-5463-4935-85b5-32219d06f782
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c659b77767fddc4c783732082c2eb65c68af8dbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356715"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="b9270-103">PidTagRecipientCertificate 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b9270-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="b9270-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9270-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9270-105">レポートで使用するためのメッセージ受信者の ASN. 1 証明書が保存されています。</span><span class="sxs-lookup"><span data-stu-id="b9270-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9270-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="b9270-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b9270-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="b9270-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="b9270-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="b9270-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b9270-109">0x0c13</span><span class="sxs-lookup"><span data-stu-id="b9270-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="b9270-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="b9270-110">Data type:</span></span>  <br/> |<span data-ttu-id="b9270-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b9270-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b9270-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="b9270-112">Area:</span></span>  <br/> |<span data-ttu-id="b9270-113">MAPI 受信者</span><span class="sxs-lookup"><span data-stu-id="b9270-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9270-114">解説</span><span class="sxs-lookup"><span data-stu-id="b9270-114">Remarks</span></span>

<span data-ttu-id="b9270-115">このプロパティは、レポートで使用する受信者の**PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) プロパティのコピーです。</span><span class="sxs-lookup"><span data-stu-id="b9270-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="b9270-116">このメソッドを使用すると、受信者が実際にメッセージを受信したことを証明することができます。これは、配信レポートが必ずしも示しているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="b9270-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b9270-117">関連リソース</span><span class="sxs-lookup"><span data-stu-id="b9270-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b9270-118">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="b9270-118">Header files</span></span>

<span data-ttu-id="b9270-119">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9270-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="b9270-120">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="b9270-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="b9270-121">Mapitags</span><span class="sxs-lookup"><span data-stu-id="b9270-121">Mapitags.h</span></span>
  
> <span data-ttu-id="b9270-122">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9270-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9270-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="b9270-123">See also</span></span>



[<span data-ttu-id="b9270-124">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="b9270-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b9270-125">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="b9270-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b9270-126">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b9270-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b9270-127">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="b9270-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

