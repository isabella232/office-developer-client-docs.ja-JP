---
title: PidTagProfileServerFullVersion の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 284b4b451a31a9478caf31fe855d38bfeab2caf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803196"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a><span data-ttu-id="7d2b9-103">PidTagProfileServerFullVersion の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7d2b9-103">PidTagProfileServerFullVersion Canonical Property</span></span>

  
  
<span data-ttu-id="7d2b9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7d2b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7d2b9-105">プロファイル内のアカウントが接続されている Microsoft Exchange Server の完全なバージョンとビルドの情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-105">Specifies complete version and build information about the Microsoft Exchange Server to which accounts in a profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="7d2b9-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7d2b9-107">PR_PROFILE_SERVER_FULL_VERSION</span><span class="sxs-lookup"><span data-stu-id="7d2b9-107">PR_PROFILE_SERVER_FULL_VERSION</span></span>  <br/> |
|<span data-ttu-id="7d2b9-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="7d2b9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7d2b9-109">0x663B</span><span class="sxs-lookup"><span data-stu-id="7d2b9-109">0x663B</span></span>  <br/> |
|<span data-ttu-id="7d2b9-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="7d2b9-110">Property type:</span></span>  <br/> |<span data-ttu-id="7d2b9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7d2b9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7d2b9-112">領域:</span><span class="sxs-lookup"><span data-stu-id="7d2b9-112">Area:</span></span>  <br/> |<span data-ttu-id="7d2b9-113">MAPI プロファイルの構成</span><span class="sxs-lookup"><span data-stu-id="7d2b9-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d2b9-114">備考</span><span class="sxs-lookup"><span data-stu-id="7d2b9-114">Remarks</span></span>

<span data-ttu-id="7d2b9-115">プロファイルが Exchange Server に接続する 1 つまたは複数のアカウントを指定できますが、同一の Exchange Server に接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="7d2b9-116">Microsoft Office Outlook 2007 より前のバージョンの Outlook では、このプロパティをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 do not support this property.</span></span> <span data-ttu-id="7d2b9-117">これらのバージョンの Outlook プロファイルで**[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** の存在を確認してください。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-117">For those versions of Outlook, check for the existence of **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** in the profile.</span></span> 
  
<span data-ttu-id="7d2b9-118">一般に、アクティブなメールボックスが、Exchange Server に接続している場合は、Outlook 2007 は、アクティブなプロファイルの**PR_PROFILE_SERVER_FULL_VERSION**プロパティで完全な Exchange Server のバージョン情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-118">Generally, if the active mailbox is connected to an Exchange Server, Outlook 2007 stores complete Exchange Server version information in the **PR_PROFILE_SERVER_FULL_VERSION** property in the active profile.</span></span> <span data-ttu-id="7d2b9-119">Outlook では、メジャーおよびマイナー バージョン番号とメジャーとマイナーのビルド番号を含む**EXCHANGE_STORE_VERSION_NUM**構造体に情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-119">Outlook stores the information in an **EXCHANGE_STORE_VERSION_NUM** structure that contains the major and minor version numbers and the major and minor build numbers.</span></span> <span data-ttu-id="7d2b9-120">たとえば、 **8.0.685.24**を Exchange Server のバージョンの識別子を保存するには、メジャー バージョン番号は、8 とマイナー バージョン番号は、0、メジャー ビルド番号は、685 とマイナー ビルド番号は、24 です。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-120">For example, to store the Exchange Server version identifier of **8.0.685.24**, the major version number is 8 and minor version number is 0, and the major build number is 685 and minor build number is 24.</span></span>
  
<span data-ttu-id="7d2b9-121">**PR_PROFILE_SERVER_VERSION**または**PR_PROFILE_SERVER_FULL_VERSION**のいずれかのみでは、プロファイル内に存在する可能性がありますが、どちらか常に、プロファイル内に存在する保証はありません。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-121">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="7d2b9-122">Outlook は、Exchange Server に正常に接続されるまでに、これらのプロパティに書き込めません。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-122">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="7d2b9-123">Outlook オブジェクト モデルでは、アクティブなメールボックスがホストされている Exchange Server のバージョンを検索するのには、 **ExchangeMailboxServerVersion**オブジェクトのプロパティの**名前空間**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-123">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7d2b9-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="7d2b9-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7d2b9-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="7d2b9-125">Protocol specifications</span></span>

<span data-ttu-id="7d2b9-126">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7d2b9-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7d2b9-127">プロパティ セットの定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-127">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7d2b9-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="7d2b9-128">Header files</span></span>

<span data-ttu-id="7d2b9-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7d2b9-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="7d2b9-130">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="7d2b9-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7d2b9-131">Mapitags.h</span></span>
  
> <span data-ttu-id="7d2b9-132">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7d2b9-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="7d2b9-133">See also</span></span>



[<span data-ttu-id="7d2b9-134">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7d2b9-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7d2b9-135">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="7d2b9-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7d2b9-136">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="7d2b9-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7d2b9-137">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="7d2b9-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

