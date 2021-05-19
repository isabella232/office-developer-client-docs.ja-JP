---
title: PidTagJunkPhishingEnableLinks 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkPhishingEnableLinks
api_type:
- HeaderDef
ms.assetid: 6b885c36-6e27-4f74-95c3-ce1cdc8a808a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7caeaa84602c9eb9a4384e9520edd866d72adbb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342758"
---
# <a name="pidtagjunkphishingenablelinks-canonical-property"></a><span data-ttu-id="eb489-103">PidTagJunkPhishingEnableLinks 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eb489-103">PidTagJunkPhishingEnableLinks Canonical Property</span></span>

  
  
<span data-ttu-id="eb489-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb489-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb489-105">TRUE の場合は、メッセージのフィッシング スタンプを無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb489-105">Signifies, if TRUE, that the phishing stamp on the message should be ignored.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb489-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="eb489-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="eb489-107">PR_JUNK_PHISHING_ENABLE_LINKS</span><span class="sxs-lookup"><span data-stu-id="eb489-107">PR_JUNK_PHISHING_ENABLE_LINKS</span></span>  <br/> |
|<span data-ttu-id="eb489-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="eb489-108">Identifier:</span></span>  <br/> |<span data-ttu-id="eb489-109">0x6107</span><span class="sxs-lookup"><span data-stu-id="eb489-109">0x6107</span></span>  <br/> |
|<span data-ttu-id="eb489-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="eb489-110">Data type:</span></span>  <br/> |<span data-ttu-id="eb489-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="eb489-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="eb489-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="eb489-112">Area:</span></span>  <br/> |<span data-ttu-id="eb489-113">スパム</span><span class="sxs-lookup"><span data-stu-id="eb489-113">Spam</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="eb489-114">関連リソース</span><span class="sxs-lookup"><span data-stu-id="eb489-114">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="eb489-115">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="eb489-115">Protocol specifications</span></span>

<span data-ttu-id="eb489-116">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb489-116">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb489-117">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="eb489-117">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="eb489-118">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb489-118">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb489-119">許可/ブロック リストの処理と迷惑メール メッセージの決定を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="eb489-119">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="eb489-120">[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="eb489-120">[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="eb489-121">受信者を騙して機密情報 (パスワードや他の個人情報など) を信頼できないソースに開示するように設計された電子メール メッセージを識別およびマークします。</span><span class="sxs-lookup"><span data-stu-id="eb489-121">Identifies and marks email messages that are designed to trick recipients into divulging sensitive information (such as passwords and other personal information) to a non-trustworthy source.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="eb489-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="eb489-122">Header files</span></span>

<span data-ttu-id="eb489-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eb489-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="eb489-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="eb489-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="eb489-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="eb489-125">Mapitags.h</span></span>
  
> <span data-ttu-id="eb489-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="eb489-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb489-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb489-127">See also</span></span>



[<span data-ttu-id="eb489-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="eb489-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="eb489-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eb489-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="eb489-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="eb489-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="eb489-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="eb489-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

