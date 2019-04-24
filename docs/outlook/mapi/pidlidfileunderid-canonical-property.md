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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7af30866a5fd2846327223b7a58c6de91f5fef7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355707"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="1b551-103">PidLidFileUnderId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1b551-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="1b551-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b551-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b551-105">他の連絡先の名前のプロパティが変更されたときに、([PidLidFileUnder](pidlidfileunder-canonical-property.md)) プロパティの**dispidfileunder**値を生成して再計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="1b551-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b551-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1b551-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b551-107">dispidfile過小 id</span><span class="sxs-lookup"><span data-stu-id="1b551-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="1b551-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="1b551-108">Property set:</span></span>  <br/> |<span data-ttu-id="1b551-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="1b551-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="1b551-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="1b551-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1b551-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="1b551-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="1b551-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1b551-112">Data type:</span></span>  <br/> |<span data-ttu-id="1b551-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1b551-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1b551-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="1b551-114">Area:</span></span>  <br/> |<span data-ttu-id="1b551-115">連絡先</span><span class="sxs-lookup"><span data-stu-id="1b551-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b551-116">解説</span><span class="sxs-lookup"><span data-stu-id="1b551-116">Remarks</span></span>

<span data-ttu-id="1b551-117">このプロパティが指定されていない場合、または次の表に記載されていない値または[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)に設定されている場合は、アプリケーションは独自のロジックを選択して、[その他の連絡先名のプロパティが変更されたときに、 **dispidfileunder**値を再計算できます。</span><span class="sxs-lookup"><span data-stu-id="1b551-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="1b551-118">次の表では、表記<PropertyName>を使用して "PropertyName の値" を指定しています。</span><span class="sxs-lookup"><span data-stu-id="1b551-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="1b551-119">たとえば、 **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) プロパティの値が "Smith" で、 **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) プロパティの値が "ben" の場合は、"ben Smith" と<PidTagGivenName> <PidTagSurname>いう文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="1b551-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="1b551-120">表で、"\r" はキャリッジリターン文字を指定します。 "\n" は改行文字を指定し<space> 、スペース文字を表します。</span><span class="sxs-lookup"><span data-stu-id="1b551-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="1b551-121">\*\*\*\*dispidfile過小 id**プロパティの値**</span><span class="sxs-lookup"><span data-stu-id="1b551-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="1b551-122">**プロパティの**下の dispidfileunder**説明**</span><span class="sxs-lookup"><span data-stu-id="1b551-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1b551-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1b551-123">0x00000000</span></span>  <br/> |<span data-ttu-id="1b551-124">空の PT_UNICODE。</span><span class="sxs-lookup"><span data-stu-id="1b551-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="1b551-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="1b551-125">0x00003001</span></span>  <br/> |<span data-ttu-id="1b551-126">"\<PidTagDisplayName\>"</span><span class="sxs-lookup"><span data-stu-id="1b551-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="1b551-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="1b551-128">"\<PidTagGivenName\>"</span><span class="sxs-lookup"><span data-stu-id="1b551-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-129">0x00003a11</span><span class="sxs-lookup"><span data-stu-id="1b551-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="1b551-130">"\<PidTagSurname\>"</span><span class="sxs-lookup"><span data-stu-id="1b551-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-131">0x00003a16</span><span class="sxs-lookup"><span data-stu-id="1b551-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="1b551-132">"\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="1b551-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="1b551-133">0x00008017</span></span>  <br/> |<span data-ttu-id="1b551-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>"\<\></span><span class="sxs-lookup"><span data-stu-id="1b551-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="1b551-135">0x00008018</span></span>  <br/> |<span data-ttu-id="1b551-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>、\<space\>\<PidTagGivenName\>\<space\>"\<\></span><span class="sxs-lookup"><span data-stu-id="1b551-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="1b551-137">0x00008019</span></span>  <br/> |<span data-ttu-id="1b551-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\>space PidTagMiddleName\>\r\n\<PidTagCompanyName\>"\<\<</span><span class="sxs-lookup"><span data-stu-id="1b551-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="1b551-139">0x00008030</span></span>  <br/> |<span data-ttu-id="1b551-140">"\<PidTagSurname\>\<\>PidTagGivenName\<space\>PidTagMiddleName\>"\<</span><span class="sxs-lookup"><span data-stu-id="1b551-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="1b551-141">0x00008031</span></span>  <br/> |<span data-ttu-id="1b551-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName space\>PidTagMiddleName\>"\<\>\<</span><span class="sxs-lookup"><span data-stu-id="1b551-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="1b551-143">0x00008032</span></span>  <br/> |<span data-ttu-id="1b551-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>"\<\></span><span class="sxs-lookup"><span data-stu-id="1b551-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="1b551-145">0x00008033</span></span>  <br/> |<span data-ttu-id="1b551-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName space\>PidTagMiddleName\>"\<\>\<</span><span class="sxs-lookup"><span data-stu-id="1b551-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="1b551-147">0x00008034</span></span>  <br/> |<span data-ttu-id="1b551-148">"\<PidTagSurname\>\<PidTagGivenName\>\>space PidTagMiddleName\>\r\n\<PidTagCompanyName\>"\<\<</span><span class="sxs-lookup"><span data-stu-id="1b551-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="1b551-149">0x00008035</span></span>  <br/> |<span data-ttu-id="1b551-150">"\<PidTagSurname\>\<space\>\<\>PidTagGivenName space\>PidTagMiddleName \r\n PidTagCompanyName"\<\>\<\>\<</span><span class="sxs-lookup"><span data-stu-id="1b551-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="1b551-151">0x00008036</span></span>  <br/> |<span data-ttu-id="1b551-152">"\<PidTagSurname\>\<space\>\>\>PidTagGivenName\>space PidTagMiddleName\>space\>PidTagGeneration\<"\<\<\<\<</span><span class="sxs-lookup"><span data-stu-id="1b551-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="1b551-153">0x00008037</span></span>  <br/> |<span data-ttu-id="1b551-154">"\<PidTagGivenName\>\<space\>\>\>PidTagMiddleName\>space PidTagSurname\>space\>PidTagGeneration\<"\<\<\<\<</span><span class="sxs-lookup"><span data-stu-id="1b551-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="1b551-155">0x00008038</span></span>  <br/> |<span data-ttu-id="1b551-156">"\<PidTagSurname\>\<PidTagGivenName\>\>space\>PidTagMiddleName\>space\>PidTagGeneration"\<\<\<\<</span><span class="sxs-lookup"><span data-stu-id="1b551-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="1b551-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="1b551-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="1b551-158">連絡先を表示するときに、アプリケーションは、その連絡先のプロパティの現在の値\*\*\*\* を使用して、この表の前の値の1つに対して、 **dispidfileunder id**の "最適な一致" を検索する必要があることを指定します。</span><span class="sxs-lookup"><span data-stu-id="1b551-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="1b551-159">0xfffffffe</span><span class="sxs-lookup"><span data-stu-id="1b551-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="1b551-160">連絡先を表示するときに、アプリで、選択した項目に一致するように、 **dispidfile過小 id**および update **dispidfileの**適切な既定値 (言語ロケールに応じて) を選択する必要があることを指定します。</span><span class="sxs-lookup"><span data-stu-id="1b551-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="1b551-161">0xffffffff</span><span class="sxs-lookup"><span data-stu-id="1b551-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="1b551-162">の**dispidfileunder**ユーザーが指定した PT_UNICODE で、別の連絡先の名前のプロパティが変更されたときには変更できません。</span><span class="sxs-lookup"><span data-stu-id="1b551-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1b551-163">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1b551-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1b551-164">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="1b551-164">Protocol specifications</span></span>

<span data-ttu-id="1b551-165">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b551-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b551-166">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="1b551-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1b551-167">[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b551-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b551-168">連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="1b551-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1b551-169">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="1b551-169">Header files</span></span>

<span data-ttu-id="1b551-170">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b551-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b551-171">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1b551-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b551-172">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b551-172">See also</span></span>



[<span data-ttu-id="1b551-173">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="1b551-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b551-174">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1b551-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b551-175">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1b551-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b551-176">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1b551-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

