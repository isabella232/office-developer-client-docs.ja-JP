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
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286567"
---
# <a name="pidtagprofileserverversion-canonical-property"></a><span data-ttu-id="4710c-103">PidTagProfileServerVersion 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4710c-103">PidTagProfileServerVersion Canonical Property</span></span>

  
  
<span data-ttu-id="4710c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4710c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4710c-105">microsoft Outlook プロファイルのアカウントが接続されている microsoft Exchange Server のバージョンに関する情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="4710c-105">Specifies information about the version of Microsoft Exchange Server to which accounts in a Microsoft Outlook profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="4710c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4710c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4710c-107">PR_PROFILE_SERVER_VERSION</span><span class="sxs-lookup"><span data-stu-id="4710c-107">PR_PROFILE_SERVER_VERSION</span></span>  <br/> |
|<span data-ttu-id="4710c-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4710c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4710c-109">0x661b</span><span class="sxs-lookup"><span data-stu-id="4710c-109">0x661B</span></span>  <br/> |
|<span data-ttu-id="4710c-110">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="4710c-110">Property type:</span></span>  <br/> |<span data-ttu-id="4710c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4710c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4710c-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="4710c-112">Area:</span></span>  <br/> |<span data-ttu-id="4710c-113">MAPI プロファイルの構成</span><span class="sxs-lookup"><span data-stu-id="4710c-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4710c-114">解説</span><span class="sxs-lookup"><span data-stu-id="4710c-114">Remarks</span></span>

<span data-ttu-id="4710c-115">プロファイルは、exchange サーバーに接続する1つ以上のアカウントを指定できますが、それらは同じ exchange サーバーに接続されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4710c-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="4710c-116">Microsoft Office outlook 2007 より前のバージョンの outlook では、このプロパティを書き込み、アクティブなプロファイルが接続されている Exchange サーバーのバージョンに関する情報を格納できます。</span><span class="sxs-lookup"><span data-stu-id="4710c-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 can write to this property to store information about the version of Exchange Server to which the active profile is connected.</span></span> <span data-ttu-id="4710c-117">ただし、バージョン情報の形式は、Exchange Server のバージョンによって異なります。</span><span class="sxs-lookup"><span data-stu-id="4710c-117">However, the format of the version information varies for different versions of Exchange Server.</span></span> <span data-ttu-id="4710c-118">たとえば、Outlook は**PR_PROFILE_SERVER_VERSION**に格納されている10進値6944で、Microsoft Exchange SERVER 2003 の**6.5.6944.3**のバージョン識別子のメジャービルド番号のみを表します。</span><span class="sxs-lookup"><span data-stu-id="4710c-118">For example, Outlook stores in **PR_PROFILE_SERVER_VERSION** the decimal value 6944 to represent only the major build number in the version identifier of **6.5.6944.3** for Microsoft Exchange Server 2003.</span></span> <span data-ttu-id="4710c-119">Exchange 2007 接続の場合、Outlook は、メジャーバージョン番号とメジャービルド番号を、プロパティにこれらの数値を連結した16進形式で格納します。</span><span class="sxs-lookup"><span data-stu-id="4710c-119">For an Exchange 2007 connection, Outlook stores the major version number and the major build number in a concatenated hexadecimal representation of these numbers in the property.</span></span> <span data-ttu-id="4710c-120">**8.0.685.24**の Exchange 2007 バージョン id には、メジャーバージョン番号8とメジャービルド番号685が10進数で含まれています。</span><span class="sxs-lookup"><span data-stu-id="4710c-120">An Exchange 2007 version identifier of **8.0.685.24** has a major version number 8 and a major build number 685 in decimal.</span></span> <span data-ttu-id="4710c-121">両方の数値を16進数に変換すると、0x8 と0x2ad が得られます。</span><span class="sxs-lookup"><span data-stu-id="4710c-121">Converting both numbers to hexadecimal, you get 0x8 and 0x2AD.</span></span> <span data-ttu-id="4710c-122">これらの2つの数値を連結すると、Outlook では**PR_PROFILE_SERVER_VERSION**の値0x82ad が16進表現で格納されます。</span><span class="sxs-lookup"><span data-stu-id="4710c-122">Concatenating these two numbers, Outlook stores the value 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadecimal representation.</span></span> 
  
<span data-ttu-id="4710c-123">Outlook 2007 では、このプロパティの読み取りまたは書き込みは行われません。</span><span class="sxs-lookup"><span data-stu-id="4710c-123">Outlook 2007 does not read or write to this property.</span></span> <span data-ttu-id="4710c-124">**[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="4710c-124">It supports **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span></span> 
  
<span data-ttu-id="4710c-125">**PR_PROFILE_SERVER_VERSION**または**PR_PROFILE_SERVER_FULL_VERSION**のいずれか1つだけがプロファイルに存在する可能性がありますが、プロファイルに常に存在する保証はありません。</span><span class="sxs-lookup"><span data-stu-id="4710c-125">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="4710c-126">Outlook は、Exchange サーバーに正常に接続されるまでは、どちらのプロパティにも書き込みを行いません。</span><span class="sxs-lookup"><span data-stu-id="4710c-126">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="4710c-127">Outlook オブジェクトモデルでは、 **NameSpace**オブジェクトの**ExchangeMailboxServerVersion**プロパティを使用して、アクティブなメールボックスがホストされている Exchange サーバーのバージョンを検索できます。</span><span class="sxs-lookup"><span data-stu-id="4710c-127">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4710c-128">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4710c-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4710c-129">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4710c-129">Protocol specifications</span></span>

<span data-ttu-id="4710c-130">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4710c-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4710c-131">プロパティセットの定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4710c-131">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4710c-132">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="4710c-132">Header files</span></span>

<span data-ttu-id="4710c-133">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4710c-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="4710c-134">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4710c-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="4710c-135">Mapitags</span><span class="sxs-lookup"><span data-stu-id="4710c-135">Mapitags.h</span></span>
  
> <span data-ttu-id="4710c-136">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4710c-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4710c-137">関連項目</span><span class="sxs-lookup"><span data-stu-id="4710c-137">See also</span></span>



[<span data-ttu-id="4710c-138">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="4710c-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4710c-139">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4710c-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4710c-140">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4710c-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4710c-141">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4710c-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

