---
title: PidLidFileUnderId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnderId
api_type:
- COM
ms.assetid: 917431a9-fd90-4b4d-b042-886e3dbf47c0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7af30866a5fd2846327223b7a58c6de91f5fef7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355707"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="494bd-103">PidLidFileUnderId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="494bd-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="494bd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="494bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="494bd-105">他の連絡先名のプロパティが変更された場合に **、dispidFileUnder** [(PidLidFileUnder)](pidlidfileunder-canonical-property.md)プロパティの値を生成および再計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="494bd-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="494bd-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="494bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="494bd-107">dispidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="494bd-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="494bd-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="494bd-108">Property set:</span></span>  <br/> |<span data-ttu-id="494bd-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="494bd-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="494bd-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="494bd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="494bd-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="494bd-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="494bd-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="494bd-112">Data type:</span></span>  <br/> |<span data-ttu-id="494bd-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="494bd-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="494bd-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="494bd-114">Area:</span></span>  <br/> |<span data-ttu-id="494bd-115">Contact</span><span class="sxs-lookup"><span data-stu-id="494bd-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="494bd-116">注釈</span><span class="sxs-lookup"><span data-stu-id="494bd-116">Remarks</span></span>

<span data-ttu-id="494bd-117">このプロパティが見つからないか、下の表または [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)の詳細ではない値に設定されている場合、アプリケーションは、他の連絡先名プロパティの変更に応じ、独自のロジックを選択して **dispidFileUnder** の値を再計算できます。</span><span class="sxs-lookup"><span data-stu-id="494bd-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="494bd-118">次の表では、表記を <PropertyName> 使用して "PropertyName の値" を指定します。</span><span class="sxs-lookup"><span data-stu-id="494bd-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="494bd-119">たとえば **、PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) プロパティの値が "Smith" で **、PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) プロパティの値が "Ben" の場合、" <PidTagGivenName> <PidTagSurname> " は "Ben Smith" という文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="494bd-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="494bd-120">表の "\r" は復帰文字を指定し、"\n" は改行文字を指定し、スペース文字 <space> を表します。</span><span class="sxs-lookup"><span data-stu-id="494bd-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="494bd-121">\*\*\*\*dispidFileUnderId\*\* プロパティの値\*\*</span><span class="sxs-lookup"><span data-stu-id="494bd-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="494bd-122">\*\*\*\*dispidFileUnder プロパティの\*\* 説明\*\*</span><span class="sxs-lookup"><span data-stu-id="494bd-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="494bd-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="494bd-123">0x00000000</span></span>  <br/> |<span data-ttu-id="494bd-124">空PT_UNICODE。</span><span class="sxs-lookup"><span data-stu-id="494bd-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="494bd-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="494bd-125">0x00003001</span></span>  <br/> |<span data-ttu-id="494bd-126">" \< PidTagDisplayName \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="494bd-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="494bd-128">" \< PidTagGivenName \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-129">0x00003A11</span><span class="sxs-lookup"><span data-stu-id="494bd-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="494bd-130">" \< PidTagSurname \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-131">0x00003A16</span><span class="sxs-lookup"><span data-stu-id="494bd-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="494bd-132">" \< PidTagCompanyName \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="494bd-133">0x00008017</span></span>  <br/> |<span data-ttu-id="494bd-134">" \< PidTagSurname \> , space \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="494bd-135">0x00008018</span></span>  <br/> |<span data-ttu-id="494bd-136">" \< PidTagCompanyName \>\r\n\< \> PidTagSurname 、 space \< \> \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="494bd-137">0x00008019</span></span>  <br/> |<span data-ttu-id="494bd-138">" \< PidTagSurname \> 、 space \< \> \< PidTagGivenName スペース \> \< \> \< PidTagMiddleName\r\n\> \< PidTagCompanyName \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="494bd-139">0x00008030</span></span>  <br/> |<span data-ttu-id="494bd-140">" \< PidTagSurname \> \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="494bd-141">0x00008031</span></span>  <br/> |<span data-ttu-id="494bd-142">" \< PidTagSurname \> \< スペース \> \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="494bd-143">0x00008032</span></span>  <br/> |<span data-ttu-id="494bd-144">" \< PidTagCompanyName \>\r\n\< PidTagSurname \> \< \> \< \> \< PidTagGivenName スペース PidTagMiddleName \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="494bd-145">0x00008033</span></span>  <br/> |<span data-ttu-id="494bd-146">" \< PidTagCompanyName \>\r\n\< \> \< PidTagSurname スペース \> \< \> \< \> \< PidTagGivenName スペース PidTagMiddleName \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="494bd-147">0x00008034</span></span>  <br/> |<span data-ttu-id="494bd-148">" \< PidTagSurname \> \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName\r\n\> \< PidTagCompanyName \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="494bd-149">0x00008035</span></span>  <br/> |<span data-ttu-id="494bd-150">" \< PidTagSurname \> \< スペース \> \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName\r\n\> \< PidTagCompanyName \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="494bd-151">0x00008036</span></span>  <br/> |<span data-ttu-id="494bd-152">" \< PidTagSurname \> \< スペース \> \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName スペース \> \< \> \< PidTagGeneration \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="494bd-153">0x00008037</span></span>  <br/> |<span data-ttu-id="494bd-154">" \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName \> \< スペース \> \< PidTagSurname スペース \> \< \> \< PidTagGeneration \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="494bd-155">0x00008038</span></span>  <br/> |<span data-ttu-id="494bd-156">" \< PidTagSurname \> \< PidTagGivenName \> \< スペース \> \< PidTagMiddleName \> \< スペース \> \< PidTagGeneration \> "</span><span class="sxs-lookup"><span data-stu-id="494bd-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="494bd-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="494bd-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="494bd-158">連絡先を表示するときに、アプリケーションが **dispidFileUnder** および他の連絡先プロパティの現在の値を使用して **、dispidFileUnderId** をこの表の前の値の 1 つに対して "最適な一致" を見つける必要があります。</span><span class="sxs-lookup"><span data-stu-id="494bd-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="494bd-159">0xfffffffe</span><span class="sxs-lookup"><span data-stu-id="494bd-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="494bd-160">連絡先を表示するときに、アプリケーションが **dispidFileUnderId** の適切な既定値 (言語ロケールに従って) を選択し、選択に一致する **dispidFileUnder** を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="494bd-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="494bd-161">0xffffffff</span><span class="sxs-lookup"><span data-stu-id="494bd-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="494bd-162">**dispidFileUnder** はユーザー提供のPT_UNICODEであり、別の連絡先名プロパティが変更された場合は変更できません。</span><span class="sxs-lookup"><span data-stu-id="494bd-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="494bd-163">関連リソース</span><span class="sxs-lookup"><span data-stu-id="494bd-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="494bd-164">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="494bd-164">Protocol specifications</span></span>

<span data-ttu-id="494bd-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="494bd-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="494bd-166">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="494bd-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="494bd-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="494bd-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="494bd-168">連絡先と個人用配布リストで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="494bd-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="494bd-169">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="494bd-169">Header files</span></span>

<span data-ttu-id="494bd-170">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="494bd-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="494bd-171">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="494bd-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="494bd-172">関連項目</span><span class="sxs-lookup"><span data-stu-id="494bd-172">See also</span></span>



[<span data-ttu-id="494bd-173">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="494bd-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="494bd-174">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="494bd-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="494bd-175">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="494bd-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="494bd-176">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="494bd-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

