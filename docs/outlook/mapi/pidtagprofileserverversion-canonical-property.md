---
title: PidTagProfileServerVersion 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 79b6461ca4a796b292b86f0f3bdbd8a39ad65863
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575680"
---
# <a name="pidtagprofileserverversion-canonical-property"></a><span data-ttu-id="bbfbe-103">PidTagProfileServerVersion 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="bbfbe-103">PidTagProfileServerVersion Canonical Property</span></span>

  
  
<span data-ttu-id="bbfbe-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bbfbe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bbfbe-105">Microsoft Outlook プロファイル内のアカウントが接続されている、Microsoft Exchange Server のバージョンに関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-105">Specifies information about the version of Microsoft Exchange Server to which accounts in a Microsoft Outlook profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="bbfbe-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="bbfbe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bbfbe-107">PR_PROFILE_SERVER_VERSION</span><span class="sxs-lookup"><span data-stu-id="bbfbe-107">PR_PROFILE_SERVER_VERSION</span></span>  <br/> |
|<span data-ttu-id="bbfbe-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="bbfbe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bbfbe-109">0x661B</span><span class="sxs-lookup"><span data-stu-id="bbfbe-109">0x661B</span></span>  <br/> |
|<span data-ttu-id="bbfbe-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="bbfbe-110">Property type:</span></span>  <br/> |<span data-ttu-id="bbfbe-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bbfbe-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bbfbe-112">領域:</span><span class="sxs-lookup"><span data-stu-id="bbfbe-112">Area:</span></span>  <br/> |<span data-ttu-id="bbfbe-113">MAPI プロファイルの構成</span><span class="sxs-lookup"><span data-stu-id="bbfbe-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bbfbe-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bbfbe-114">Remarks</span></span>

<span data-ttu-id="bbfbe-115">プロファイルが Exchange Server に接続する 1 つまたは複数のアカウントを指定できますが、同一の Exchange Server に接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="bbfbe-116">Microsoft Office Outlook 2007 より前のバージョンの Outlook は、アクティブなプロファイルが接続されている Exchange Server のバージョンに関する情報を格納するには、このプロパティを作成できます。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 can write to this property to store information about the version of Exchange Server to which the active profile is connected.</span></span> <span data-ttu-id="bbfbe-117">ただし、バージョン情報の形式は、Exchange Server のバージョンごとに異なります。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-117">However, the format of the version information varies for different versions of Exchange Server.</span></span> <span data-ttu-id="bbfbe-118">たとえば、 **PR_PROFILE_SERVER_VERSION** 10 進値 6944 メジャーのみを表すために Outlook ストアは、Microsoft Exchange Server 2003 の**6.5.6944.3**のバージョン id の番号を構築します。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-118">For example, Outlook stores in **PR_PROFILE_SERVER_VERSION** the decimal value 6944 to represent only the major build number in the version identifier of **6.5.6944.3** for Microsoft Exchange Server 2003.</span></span> <span data-ttu-id="bbfbe-119">Exchange 2007 接続の場合は、メジャー バージョン番号を格納する Outlook とメジャー ビルド番号のプロパティでこれらの数値の場合は、連結された 16 進数表現。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-119">For an Exchange 2007 connection, Outlook stores the major version number and the major build number in a concatenated hexadecimal representation of these numbers in the property.</span></span> <span data-ttu-id="bbfbe-120">**8.0.685.24**の Exchange 2007 のバージョン識別子は、10 進数でメジャー バージョン番号 8 とメジャー ビルド番号 685 を持ちます。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-120">An Exchange 2007 version identifier of **8.0.685.24** has a major version number 8 and a major build number 685 in decimal.</span></span> <span data-ttu-id="bbfbe-121">0x8 と 0x2AD を取得する両方の数値を 16 進数に変換します。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-121">Converting both numbers to hexadecimal, you get 0x8 and 0x2AD.</span></span> <span data-ttu-id="bbfbe-122">これら 2 つの数値を連結するには、Outlook 格納値 0x82AD **PR_PROFILE_SERVER_VERSION**で 16 進数表現でします。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-122">Concatenating these two numbers, Outlook stores the value 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadecimal representation.</span></span> 
  
<span data-ttu-id="bbfbe-123">Outlook 2007 の読み取りまたはこのプロパティへの書き込みはないです。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-123">Outlook 2007 does not read or write to this property.</span></span> <span data-ttu-id="bbfbe-124">**[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** をサポートします。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-124">It supports **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span></span> 
  
<span data-ttu-id="bbfbe-125">**PR_PROFILE_SERVER_VERSION**または**PR_PROFILE_SERVER_FULL_VERSION**のいずれかのみでは、プロファイル内に存在する可能性がありますが、どちらか常に、プロファイル内に存在する保証はありません。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-125">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="bbfbe-126">Outlook は、Exchange Server に正常に接続されるまでに、これらのプロパティに書き込めません。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-126">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="bbfbe-127">Outlook オブジェクト モデルでは、アクティブなメールボックスがホストされている Exchange Server のバージョンを検索するのには、 **ExchangeMailboxServerVersion**オブジェクトのプロパティの**名前空間**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-127">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bbfbe-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="bbfbe-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bbfbe-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="bbfbe-129">Protocol specifications</span></span>

<span data-ttu-id="bbfbe-130">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bbfbe-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bbfbe-131">プロパティ セットの定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-131">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bbfbe-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="bbfbe-132">Header files</span></span>

<span data-ttu-id="bbfbe-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bbfbe-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="bbfbe-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="bbfbe-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bbfbe-135">Mapitags.h</span></span>
  
> <span data-ttu-id="bbfbe-136">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bbfbe-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bbfbe-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="bbfbe-137">See also</span></span>



[<span data-ttu-id="bbfbe-138">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bbfbe-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bbfbe-139">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="bbfbe-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bbfbe-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bbfbe-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bbfbe-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="bbfbe-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

