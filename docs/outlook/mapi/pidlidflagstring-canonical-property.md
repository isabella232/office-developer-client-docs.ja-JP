---
title: PidLidFlagString 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagString
api_type:
- COM
ms.assetid: 4cf1e08b-c869-4965-a1e4-512a0684700f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b3cd88db7e93b53990cf0181af623ebca75f0c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357786"
---
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="4aff5-103">PidLidFlagString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4aff5-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="4aff5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4aff5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4aff5-105">フラグに関連付けられている定義済みのテキスト文字列のセットの1つを識別するインデックスを含みます。</span><span class="sxs-lookup"><span data-stu-id="4aff5-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4aff5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4aff5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4aff5-107">dispidflagstringenum</span><span class="sxs-lookup"><span data-stu-id="4aff5-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="4aff5-108">プロパティセット:</span><span class="sxs-lookup"><span data-stu-id="4aff5-108">Property set:</span></span>  <br/> |<span data-ttu-id="4aff5-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="4aff5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="4aff5-110">ロング ID (LID):</span><span class="sxs-lookup"><span data-stu-id="4aff5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="4aff5-111">0x000085c0</span><span class="sxs-lookup"><span data-stu-id="4aff5-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="4aff5-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4aff5-112">Data type:</span></span>  <br/> |<span data-ttu-id="4aff5-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4aff5-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4aff5-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="4aff5-114">Area:</span></span>  <br/> |<span data-ttu-id="4aff5-115">タスク</span><span class="sxs-lookup"><span data-stu-id="4aff5-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4aff5-116">解説</span><span class="sxs-lookup"><span data-stu-id="4aff5-116">Remarks</span></span>

<span data-ttu-id="4aff5-117">このプロパティが設定されている場合、クライアントは次の表の対応する文字列値を使用する必要があります (たとえば、現在のユーザーの言語に翻訳されている文字列を置換する場合)。 **dispidflagrequest**で設定した値は無視する必要があります ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) および**dispidvalidflagstringproof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="4aff5-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="4aff5-118">連絡先オブジェクトに対してユーザーに推奨される既定値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4aff5-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="4aff5-119">**値**</span><span class="sxs-lookup"><span data-stu-id="4aff5-119">**Value**</span></span>|<span data-ttu-id="4aff5-120">**英語の文字列**</span><span class="sxs-lookup"><span data-stu-id="4aff5-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4aff5-121">0x00000000 または存在しない</span><span class="sxs-lookup"><span data-stu-id="4aff5-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="4aff5-122">**dispidflagrequest**の表示に関連するガイダンスに従ってください。</span><span class="sxs-lookup"><span data-stu-id="4aff5-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="4aff5-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="4aff5-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="4aff5-124">"フォローアップ"</span><span class="sxs-lookup"><span data-stu-id="4aff5-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="4aff5-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="4aff5-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="4aff5-126">呼ん</span><span class="sxs-lookup"><span data-stu-id="4aff5-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="4aff5-127">0x00000070</span><span class="sxs-lookup"><span data-stu-id="4aff5-127">0x00000070</span></span>  <br/> |<span data-ttu-id="4aff5-128">"会議の調整"</span><span class="sxs-lookup"><span data-stu-id="4aff5-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="4aff5-129">0x00000071</span><span class="sxs-lookup"><span data-stu-id="4aff5-129">0x00000071</span></span>  <br/> |<span data-ttu-id="4aff5-130">"電子メールの送信"</span><span class="sxs-lookup"><span data-stu-id="4aff5-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="4aff5-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="4aff5-131">0x00000072</span></span>  <br/> |<span data-ttu-id="4aff5-132">[手紙の送信]</span><span class="sxs-lookup"><span data-stu-id="4aff5-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="4aff5-133">他のすべてのメッセージオブジェクトについて、ユーザーに提示される既定値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4aff5-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="4aff5-134">**値**</span><span class="sxs-lookup"><span data-stu-id="4aff5-134">**Value**</span></span>|<span data-ttu-id="4aff5-135">**英語の文字列**</span><span class="sxs-lookup"><span data-stu-id="4aff5-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4aff5-136">0x00000000 または存在しない</span><span class="sxs-lookup"><span data-stu-id="4aff5-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="4aff5-137">**dispidflagrequest**の表示に関連するガイダンスに従ってください。</span><span class="sxs-lookup"><span data-stu-id="4aff5-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="4aff5-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4aff5-138">0x00000001</span></span>  <br/> |<span data-ttu-id="4aff5-139">呼ん</span><span class="sxs-lookup"><span data-stu-id="4aff5-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="4aff5-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4aff5-140">0x00000002</span></span>  <br/> |<span data-ttu-id="4aff5-141">"転送不可"</span><span class="sxs-lookup"><span data-stu-id="4aff5-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="4aff5-142">0x00000003</span><span class="sxs-lookup"><span data-stu-id="4aff5-142">0x00000003</span></span>  <br/> |<span data-ttu-id="4aff5-143">"フォローアップ"</span><span class="sxs-lookup"><span data-stu-id="4aff5-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="4aff5-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="4aff5-144">0x00000004</span></span>  <br/> |<span data-ttu-id="4aff5-145">情報</span><span class="sxs-lookup"><span data-stu-id="4aff5-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="4aff5-146">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4aff5-146">0x00000005</span></span>  <br/> |<span data-ttu-id="4aff5-147">"転送する"</span><span class="sxs-lookup"><span data-stu-id="4aff5-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="4aff5-148">0x00000006</span><span class="sxs-lookup"><span data-stu-id="4aff5-148">0x00000006</span></span>  <br/> |<span data-ttu-id="4aff5-149">"応答を必要としない"</span><span class="sxs-lookup"><span data-stu-id="4aff5-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="4aff5-150">0x00000007</span><span class="sxs-lookup"><span data-stu-id="4aff5-150">0x00000007</span></span>  <br/> |<span data-ttu-id="4aff5-151">読み込む</span><span class="sxs-lookup"><span data-stu-id="4aff5-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="4aff5-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="4aff5-152">0x00000008</span></span>  <br/> |<span data-ttu-id="4aff5-153">"返信"</span><span class="sxs-lookup"><span data-stu-id="4aff5-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="4aff5-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="4aff5-154">0x00000009</span></span>  <br/> |<span data-ttu-id="4aff5-155">"全員に返信"</span><span class="sxs-lookup"><span data-stu-id="4aff5-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="4aff5-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="4aff5-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="4aff5-157">中</span><span class="sxs-lookup"><span data-stu-id="4aff5-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="4aff5-158">上記で指定したすべての文字列は、必要に応じてユーザーの言語に翻訳できます。</span><span class="sxs-lookup"><span data-stu-id="4aff5-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4aff5-159">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4aff5-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4aff5-160">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="4aff5-160">Protocol specifications</span></span>

<span data-ttu-id="4aff5-161">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4aff5-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4aff5-162">プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4aff5-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4aff5-163">[[OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4aff5-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4aff5-164">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="4aff5-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4aff5-165">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="4aff5-165">Header files</span></span>

<span data-ttu-id="4aff5-166">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4aff5-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="4aff5-167">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4aff5-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4aff5-168">関連項目</span><span class="sxs-lookup"><span data-stu-id="4aff5-168">See also</span></span>



[<span data-ttu-id="4aff5-169">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="4aff5-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4aff5-170">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4aff5-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4aff5-171">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4aff5-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4aff5-172">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4aff5-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

