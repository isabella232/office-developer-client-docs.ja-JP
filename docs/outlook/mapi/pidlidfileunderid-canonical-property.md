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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397192"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="c088c-103">PidLidFileUnderId 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c088c-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="c088c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c088c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c088c-105">生成し、その他の連絡先の名前のプロパティの変更時に**dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) プロパティの値を再計算する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="c088c-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c088c-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="c088c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c088c-107">dispidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="c088c-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="c088c-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="c088c-108">Property set:</span></span>  <br/> |<span data-ttu-id="c088c-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="c088c-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="c088c-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="c088c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c088c-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="c088c-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="c088c-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="c088c-112">Data type:</span></span>  <br/> |<span data-ttu-id="c088c-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c088c-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c088c-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="c088c-114">Area:</span></span>  <br/> |<span data-ttu-id="c088c-115">Contact</span><span class="sxs-lookup"><span data-stu-id="c088c-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c088c-116">備考</span><span class="sxs-lookup"><span data-stu-id="c088c-116">Remarks</span></span>

<span data-ttu-id="c088c-117">このプロパティがないか、または[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)で、次の表で詳細にない値に設定、アプリケーションはその他の連絡先の名前のプロパティの変更と**dispidFileUnder**の値を再計算するのには、独自のロジックを選択できます。</span><span class="sxs-lookup"><span data-stu-id="c088c-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="c088c-118">次の表では、表記法に<PropertyName>」プロパティ名の値」を指定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="c088c-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="c088c-119">たとえば、 **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) プロパティの値は、チェック ボックスをオフ、および**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) プロパティの値が「佐藤」、"<PidTagGivenName> <PidTagSurname>""Ben Smith"という文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="c088c-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="c088c-120">キャリッジ リターン文字を指定する「\r」の表で、"\n"は、ライン フィード文字を指定し、、<space>空白文字を表します。</span><span class="sxs-lookup"><span data-stu-id="c088c-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="c088c-121">\*\*\*\*DispidFileUnderId**プロパティの値**</span><span class="sxs-lookup"><span data-stu-id="c088c-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="c088c-122">\*\*\*\*DispidFileUnder**プロパティの説明**</span><span class="sxs-lookup"><span data-stu-id="c088c-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c088c-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c088c-123">0x00000000</span></span>  <br/> |<span data-ttu-id="c088c-124">空の PT_UNICODE。</span><span class="sxs-lookup"><span data-stu-id="c088c-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="c088c-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="c088c-125">0x00003001</span></span>  <br/> |<span data-ttu-id="c088c-126">"\<PidTagDisplayName\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="c088c-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="c088c-128">"\<PidTagGivenName\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-129">0x00003A11</span><span class="sxs-lookup"><span data-stu-id="c088c-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="c088c-130">"\<PidTagSurname\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-131">0x00003A16</span><span class="sxs-lookup"><span data-stu-id="c088c-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="c088c-132">"\<PidTagCompanyName\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="c088c-133">0x00008017</span></span>  <br/> |<span data-ttu-id="c088c-134">"\<PidTagSurname\>、\<スペース\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="c088c-135">0x00008018</span></span>  <br/> |<span data-ttu-id="c088c-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>、\<スペース\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="c088c-137">0x00008019</span></span>  <br/> |<span data-ttu-id="c088c-138">"\<PidTagSurname\>、\<スペース\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="c088c-139">0x00008030</span></span>  <br/> |<span data-ttu-id="c088c-140">"\<PidTagSurname\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="c088c-141">0x00008031</span></span>  <br/> |<span data-ttu-id="c088c-142">"\<PidTagSurname\>\<スペース\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="c088c-143">0x00008032</span></span>  <br/> |<span data-ttu-id="c088c-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="c088c-145">0x00008033</span></span>  <br/> |<span data-ttu-id="c088c-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<スペース\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="c088c-147">0x00008034</span></span>  <br/> |<span data-ttu-id="c088c-148">"\<PidTagSurname\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="c088c-149">0x00008035</span></span>  <br/> |<span data-ttu-id="c088c-150">"\<PidTagSurname\>\<スペース\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="c088c-151">0x00008036</span></span>  <br/> |<span data-ttu-id="c088c-152">"\<PidTagSurname\>\<スペース\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>\<スペース\>\<PidTagGeneration\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="c088c-153">0x00008037</span></span>  <br/> |<span data-ttu-id="c088c-154">"\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>\<スペース\>\<PidTagSurname\>\<スペース\>\<PidTagGeneration\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="c088c-155">0x00008038</span></span>  <br/> |<span data-ttu-id="c088c-156">"\<PidTagSurname\>\<PidTagGivenName\>\<スペース\>\<PidTagMiddleName\>\<スペース\>\<PidTagGeneration\>」</span><span class="sxs-lookup"><span data-stu-id="c088c-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="c088c-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="c088c-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="c088c-158">、連絡先を表示するには、ときに、アプリケーション必要がありますしようとする**dispidFileUnder**およびその他の連絡先のプロパティの現在の値を使用して、次の表に示した値のいずれかに**dispidFileUnderId**の最適な"を検索するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c088c-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="c088c-159">0xfffffffe</span><span class="sxs-lookup"><span data-stu-id="c088c-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="c088c-160">指定、連絡先を表示するには、ときにアプリケーションする必要があります (言語のロケール) に基づく適切な既定値を選択して、 **dispidFileUnderId**の選択に一致するように**dispidFileUnder**を更新します。</span><span class="sxs-lookup"><span data-stu-id="c088c-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="c088c-161">0 xffffffff</span><span class="sxs-lookup"><span data-stu-id="c088c-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="c088c-162">**dispidFileUnder**は、ユーザーが指定した PT_UNICODE と、別の連絡先の名前のプロパティが変更されたときに変更されません。</span><span class="sxs-lookup"><span data-stu-id="c088c-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c088c-163">関連リソース</span><span class="sxs-lookup"><span data-stu-id="c088c-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c088c-164">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="c088c-164">Protocol specifications</span></span>

<span data-ttu-id="c088c-165">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c088c-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c088c-166">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="c088c-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c088c-167">[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c088c-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c088c-168">プロパティは、連絡先、個人用配布リストの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="c088c-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c088c-169">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="c088c-169">Header files</span></span>

<span data-ttu-id="c088c-170">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c088c-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="c088c-171">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="c088c-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c088c-172">関連項目</span><span class="sxs-lookup"><span data-stu-id="c088c-172">See also</span></span>



[<span data-ttu-id="c088c-173">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c088c-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c088c-174">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="c088c-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c088c-175">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c088c-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c088c-176">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="c088c-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

