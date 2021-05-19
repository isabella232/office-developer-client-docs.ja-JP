---
title: PidTagProfileServerFullVersion 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341602"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a><span data-ttu-id="3bff6-103">PidTagProfileServerFullVersion 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3bff6-103">PidTagProfileServerFullVersion Canonical Property</span></span>

  
  
<span data-ttu-id="3bff6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bff6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bff6-105">プロファイル内のアカウントが接続されているMicrosoft Exchange Server完全なバージョンとビルド情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="3bff6-105">Specifies complete version and build information about the Microsoft Exchange Server to which accounts in a profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="3bff6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="3bff6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3bff6-107">PR_PROFILE_SERVER_FULL_VERSION</span><span class="sxs-lookup"><span data-stu-id="3bff6-107">PR_PROFILE_SERVER_FULL_VERSION</span></span>  <br/> |
|<span data-ttu-id="3bff6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3bff6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3bff6-109">0x663B</span><span class="sxs-lookup"><span data-stu-id="3bff6-109">0x663B</span></span>  <br/> |
|<span data-ttu-id="3bff6-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="3bff6-110">Property type:</span></span>  <br/> |<span data-ttu-id="3bff6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3bff6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3bff6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="3bff6-112">Area:</span></span>  <br/> |<span data-ttu-id="3bff6-113">MAPI プロファイルの構成</span><span class="sxs-lookup"><span data-stu-id="3bff6-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bff6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="3bff6-114">Remarks</span></span>

<span data-ttu-id="3bff6-115">プロファイルは、1 つのアカウントに接続する 1 つ以上のアカウントをExchange Server、同じアカウントに接続する必要Exchange Server。</span><span class="sxs-lookup"><span data-stu-id="3bff6-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="3bff6-116">2007 Outlook以前Microsoft Office Outlookバージョンでは、このプロパティはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3bff6-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 do not support this property.</span></span> <span data-ttu-id="3bff6-117">これらのバージョンのプロファイルOutlookプロファイル **[内にPR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** を確認します。</span><span class="sxs-lookup"><span data-stu-id="3bff6-117">For those versions of Outlook, check for the existence of **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** in the profile.</span></span> 
  
<span data-ttu-id="3bff6-118">通常、アクティブなメールボックスが Exchange Server に接続されている場合、Outlook 2007 は、Exchange Server バージョン情報をアクティブ プロファイルの **PR_PROFILE_SERVER_FULL_VERSION** プロパティに保存します。</span><span class="sxs-lookup"><span data-stu-id="3bff6-118">Generally, if the active mailbox is connected to an Exchange Server, Outlook 2007 stores complete Exchange Server version information in the **PR_PROFILE_SERVER_FULL_VERSION** property in the active profile.</span></span> <span data-ttu-id="3bff6-119">Outlookは、メジャー バージョン番号とマイナー **バージョン番号EXCHANGE_STORE_VERSION_NUM** メジャービルド番号とマイナー ビルド番号を含むデータ構造に情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="3bff6-119">Outlook stores the information in an **EXCHANGE_STORE_VERSION_NUM** structure that contains the major and minor version numbers and the major and minor build numbers.</span></span> <span data-ttu-id="3bff6-120">たとえば、Exchange Server バージョン識別子 **8.0.685.24** を格納するには、メジャー バージョン番号は 8、マイナー バージョン番号は 0、メジャー ビルド番号は 685、マイナー ビルド番号は 24 です。</span><span class="sxs-lookup"><span data-stu-id="3bff6-120">For example, to store the Exchange Server version identifier of **8.0.685.24**, the major version number is 8 and minor version number is 0, and the major build number is 685 and minor build number is 24.</span></span>
  
<span data-ttu-id="3bff6-121">プロファイル **にPR_PROFILE_SERVER_VERSIONまたは** PR_PROFILE_SERVER_FULL_VERSIONの1 つだけが存在する可能性がありますが、プロファイルに常に存在する保証はありません。</span><span class="sxs-lookup"><span data-stu-id="3bff6-121">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="3bff6-122">Outlookに正常に接続するまで、どちらのプロパティにも書き込Exchange Server。</span><span class="sxs-lookup"><span data-stu-id="3bff6-122">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="3bff6-123">Outlook オブジェクト モデルでは **、NameSpace** オブジェクトの **ExchangeMailboxServerVersion** プロパティを使用して、アクティブなメールボックスがホストされている Exchange Server のバージョンを検索できます。</span><span class="sxs-lookup"><span data-stu-id="3bff6-123">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3bff6-124">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3bff6-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3bff6-125">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3bff6-125">Protocol specifications</span></span>

<span data-ttu-id="3bff6-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3bff6-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3bff6-127">プロパティ セットの定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3bff6-127">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3bff6-128">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3bff6-128">Header files</span></span>

<span data-ttu-id="3bff6-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3bff6-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="3bff6-130">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3bff6-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="3bff6-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3bff6-131">Mapitags.h</span></span>
  
> <span data-ttu-id="3bff6-132">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="3bff6-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3bff6-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="3bff6-133">See also</span></span>



[<span data-ttu-id="3bff6-134">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="3bff6-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3bff6-135">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="3bff6-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3bff6-136">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3bff6-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3bff6-137">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="3bff6-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

