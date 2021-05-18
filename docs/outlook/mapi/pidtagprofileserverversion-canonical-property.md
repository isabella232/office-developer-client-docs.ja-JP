---
title: PidTagProfileServerVersion 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286567"
---
# <a name="pidtagprofileserverversion-canonical-property"></a><span data-ttu-id="1f567-103">PidTagProfileServerVersion 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1f567-103">PidTagProfileServerVersion Canonical Property</span></span>

  
  
<span data-ttu-id="1f567-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f567-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f567-105">Microsoft プロファイルのアカウントが接続されているMicrosoft Exchange Serverのバージョンに関する情報Outlook指定します。</span><span class="sxs-lookup"><span data-stu-id="1f567-105">Specifies information about the version of Microsoft Exchange Server to which accounts in a Microsoft Outlook profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="1f567-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1f567-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f567-107">PR_PROFILE_SERVER_VERSION</span><span class="sxs-lookup"><span data-stu-id="1f567-107">PR_PROFILE_SERVER_VERSION</span></span>  <br/> |
|<span data-ttu-id="1f567-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1f567-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f567-109">0x661B</span><span class="sxs-lookup"><span data-stu-id="1f567-109">0x661B</span></span>  <br/> |
|<span data-ttu-id="1f567-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="1f567-110">Property type:</span></span>  <br/> |<span data-ttu-id="1f567-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1f567-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1f567-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="1f567-112">Area:</span></span>  <br/> |<span data-ttu-id="1f567-113">MAPI プロファイルの構成</span><span class="sxs-lookup"><span data-stu-id="1f567-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f567-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1f567-114">Remarks</span></span>

<span data-ttu-id="1f567-115">プロファイルは、1 つのアカウントに接続する 1 つ以上のアカウントをExchange Server、同じアカウントに接続する必要Exchange Server。</span><span class="sxs-lookup"><span data-stu-id="1f567-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="1f567-116">Outlook 2007 Microsoft Office Outlook より前のバージョンでは、このプロパティに書き込み、アクティブ なプロファイルが接続されている Exchange Server のバージョンに関する情報を格納できます。</span><span class="sxs-lookup"><span data-stu-id="1f567-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 can write to this property to store information about the version of Exchange Server to which the active profile is connected.</span></span> <span data-ttu-id="1f567-117">ただし、バージョン情報の形式は、バージョンごとに異Exchange Server。</span><span class="sxs-lookup"><span data-stu-id="1f567-117">However, the format of the version information varies for different versions of Exchange Server.</span></span> <span data-ttu-id="1f567-118">たとえば、Outlook は 2003 年のバージョン識別子 **6.5.6944.3** のメジャー ビルド番号のみを表す 10 進数の値 6944 を PR_PROFILE_SERVER_VERSION に格納Microsoft Exchange Serverします。 </span><span class="sxs-lookup"><span data-stu-id="1f567-118">For example, Outlook stores in **PR_PROFILE_SERVER_VERSION** the decimal value 6944 to represent only the major build number in the version identifier of **6.5.6944.3** for Microsoft Exchange Server 2003.</span></span> <span data-ttu-id="1f567-119">2007 Exchange 2007 接続の場合、Outlook はメジャー バージョン番号とメジャー ビルド番号を、これらの番号の連結された 16 進表記でプロパティに格納します。</span><span class="sxs-lookup"><span data-stu-id="1f567-119">For an Exchange 2007 connection, Outlook stores the major version number and the major build number in a concatenated hexadecimal representation of these numbers in the property.</span></span> <span data-ttu-id="1f567-120">2007 Exchange **8.0.685.24** のバージョン識別子には、メジャー バージョン番号 8 と 10 進数のメジャー ビルド番号 685 があります。</span><span class="sxs-lookup"><span data-stu-id="1f567-120">An Exchange 2007 version identifier of **8.0.685.24** has a major version number 8 and a major build number 685 in decimal.</span></span> <span data-ttu-id="1f567-121">両方の数値を 16 進数に変換すると、0x8と0x2AD。</span><span class="sxs-lookup"><span data-stu-id="1f567-121">Converting both numbers to hexadecimal, you get 0x8 and 0x2AD.</span></span> <span data-ttu-id="1f567-122">これら 2 つの数値を連結するとOutlook値が 16 進表記 **0x82ADにPR_PROFILE_SERVER_VERSION** 格納されます。</span><span class="sxs-lookup"><span data-stu-id="1f567-122">Concatenating these two numbers, Outlook stores the value 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadecimal representation.</span></span> 
  
<span data-ttu-id="1f567-123">Outlook 2007 は、このプロパティの読み取りまたは書き込みを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f567-123">Outlook 2007 does not read or write to this property.</span></span> <span data-ttu-id="1f567-124">これは、PR_PROFILE_SERVER_FULL_VERSION **[をサポートしています](pidtagprofileserverfullversion-canonical-property.md)**。</span><span class="sxs-lookup"><span data-stu-id="1f567-124">It supports **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span></span> 
  
<span data-ttu-id="1f567-125">プロファイル **にPR_PROFILE_SERVER_VERSIONまたは** PR_PROFILE_SERVER_FULL_VERSIONの1 つだけが存在する可能性がありますが、プロファイルに常に存在する保証はありません。</span><span class="sxs-lookup"><span data-stu-id="1f567-125">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="1f567-126">Outlookに正常に接続するまで、どちらのプロパティにも書き込Exchange Server。</span><span class="sxs-lookup"><span data-stu-id="1f567-126">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="1f567-127">Outlook オブジェクト モデルでは **、NameSpace** オブジェクトの **ExchangeMailboxServerVersion** プロパティを使用して、アクティブなメールボックスがホストされている Exchange Server のバージョンを検索できます。</span><span class="sxs-lookup"><span data-stu-id="1f567-127">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1f567-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1f567-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f567-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1f567-129">Protocol specifications</span></span>

<span data-ttu-id="1f567-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f567-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f567-131">プロパティ セットの定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1f567-131">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f567-132">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1f567-132">Header files</span></span>

<span data-ttu-id="1f567-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f567-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f567-134">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1f567-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f567-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f567-135">Mapitags.h</span></span>
  
> <span data-ttu-id="1f567-136">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="1f567-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f567-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="1f567-137">See also</span></span>



[<span data-ttu-id="1f567-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1f567-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f567-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1f567-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f567-140">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="1f567-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f567-141">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="1f567-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

