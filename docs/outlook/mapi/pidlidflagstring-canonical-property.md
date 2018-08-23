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
ms.openlocfilehash: 53fe309fb15807ad698fef5a06781e5c3e0bae0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801984"
---
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="921e5-103">PidLidFlagString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="921e5-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="921e5-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="921e5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="921e5-105">フラグに関連付けられている定義済みのテキスト文字列のセットのいずれかを識別するインデックスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="921e5-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="921e5-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="921e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="921e5-107">dispidFlagStringEnum</span><span class="sxs-lookup"><span data-stu-id="921e5-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="921e5-108">プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="921e5-108">Property set:</span></span>  <br/> |<span data-ttu-id="921e5-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="921e5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="921e5-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="921e5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="921e5-111">0x000085C0</span><span class="sxs-lookup"><span data-stu-id="921e5-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="921e5-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="921e5-112">Data type:</span></span>  <br/> |<span data-ttu-id="921e5-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="921e5-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="921e5-114">領域:</span><span class="sxs-lookup"><span data-stu-id="921e5-114">Area:</span></span>  <br/> |<span data-ttu-id="921e5-115">タスク</span><span class="sxs-lookup"><span data-stu-id="921e5-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="921e5-116">注釈</span><span class="sxs-lookup"><span data-stu-id="921e5-116">Remarks</span></span>

<span data-ttu-id="921e5-117">クライアントが (たとえば、現在のユーザーの言語に翻訳された文字列を置換する)、以下の表に対応する文字列値を使用する必要があり、 **dispidFlagRequest** ([で設定された値を無視する必要がありますこのプロパティが設定されている場合PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) と**dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md))。</span><span class="sxs-lookup"><span data-stu-id="921e5-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="921e5-118">連絡先オブジェクトをユーザーに推奨される既定値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="921e5-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="921e5-119">**値**</span><span class="sxs-lookup"><span data-stu-id="921e5-119">**Value**</span></span>|<span data-ttu-id="921e5-120">**英語の文字列**</span><span class="sxs-lookup"><span data-stu-id="921e5-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="921e5-121">0x00000000 されていないか</span><span class="sxs-lookup"><span data-stu-id="921e5-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="921e5-122">**DispidFlagRequest**の表示に関連する指示に従います。</span><span class="sxs-lookup"><span data-stu-id="921e5-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="921e5-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="921e5-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="921e5-124">「フォロー アップ」</span><span class="sxs-lookup"><span data-stu-id="921e5-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="921e5-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="921e5-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="921e5-126">「呼び出し」</span><span class="sxs-lookup"><span data-stu-id="921e5-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="921e5-127">0x00000070</span><span class="sxs-lookup"><span data-stu-id="921e5-127">0x00000070</span></span>  <br/> |<span data-ttu-id="921e5-128">「会議を開催」</span><span class="sxs-lookup"><span data-stu-id="921e5-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="921e5-129">0x00000071</span><span class="sxs-lookup"><span data-stu-id="921e5-129">0x00000071</span></span>  <br/> |<span data-ttu-id="921e5-130">[電子メールを送信する]</span><span class="sxs-lookup"><span data-stu-id="921e5-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="921e5-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="921e5-131">0x00000072</span></span>  <br/> |<span data-ttu-id="921e5-132">"の文字を送信する]</span><span class="sxs-lookup"><span data-stu-id="921e5-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="921e5-133">他のすべてのメッセージ オブジェクトのユーザーに推奨される既定値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="921e5-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="921e5-134">**値**</span><span class="sxs-lookup"><span data-stu-id="921e5-134">**Value**</span></span>|<span data-ttu-id="921e5-135">**英語の文字列**</span><span class="sxs-lookup"><span data-stu-id="921e5-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="921e5-136">0x00000000 されていないか</span><span class="sxs-lookup"><span data-stu-id="921e5-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="921e5-137">**DispidFlagRequest**の表示に関連する指示に従います。</span><span class="sxs-lookup"><span data-stu-id="921e5-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="921e5-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="921e5-138">0x00000001</span></span>  <br/> |<span data-ttu-id="921e5-139">「呼び出し」</span><span class="sxs-lookup"><span data-stu-id="921e5-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="921e5-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="921e5-140">0x00000002</span></span>  <br/> |<span data-ttu-id="921e5-141">「転送不可」</span><span class="sxs-lookup"><span data-stu-id="921e5-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="921e5-142">0x00000003</span><span class="sxs-lookup"><span data-stu-id="921e5-142">0x00000003</span></span>  <br/> |<span data-ttu-id="921e5-143">「フォロー アップ」</span><span class="sxs-lookup"><span data-stu-id="921e5-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="921e5-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="921e5-144">0x00000004</span></span>  <br/> |<span data-ttu-id="921e5-145">"については、「</span><span class="sxs-lookup"><span data-stu-id="921e5-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="921e5-146">0x00000005</span><span class="sxs-lookup"><span data-stu-id="921e5-146">0x00000005</span></span>  <br/> |<span data-ttu-id="921e5-147">「転送」</span><span class="sxs-lookup"><span data-stu-id="921e5-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="921e5-148">0x00000006</span><span class="sxs-lookup"><span data-stu-id="921e5-148">0x00000006</span></span>  <br/> |<span data-ttu-id="921e5-149">「返信不要」</span><span class="sxs-lookup"><span data-stu-id="921e5-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="921e5-150">0x00000007</span><span class="sxs-lookup"><span data-stu-id="921e5-150">0x00000007</span></span>  <br/> |<span data-ttu-id="921e5-151">「読み取り」</span><span class="sxs-lookup"><span data-stu-id="921e5-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="921e5-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="921e5-152">0x00000008</span></span>  <br/> |<span data-ttu-id="921e5-153">[返信]</span><span class="sxs-lookup"><span data-stu-id="921e5-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="921e5-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="921e5-154">0x00000009</span></span>  <br/> |<span data-ttu-id="921e5-155">"全員へ返信]</span><span class="sxs-lookup"><span data-stu-id="921e5-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="921e5-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="921e5-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="921e5-157">「レビュー」</span><span class="sxs-lookup"><span data-stu-id="921e5-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="921e5-158">上で指定したすべての文字列は、適切な場合、ユーザーの言語に翻訳できます。</span><span class="sxs-lookup"><span data-stu-id="921e5-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="921e5-159">関連リソース</span><span class="sxs-lookup"><span data-stu-id="921e5-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="921e5-160">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="921e5-160">Protocol specifications</span></span>

<span data-ttu-id="921e5-161">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="921e5-161">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="921e5-162">プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="921e5-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="921e5-163">[[MS OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="921e5-163">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="921e5-164">プロパティ フラグに関連する操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="921e5-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="921e5-165">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="921e5-165">Header files</span></span>

<span data-ttu-id="921e5-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="921e5-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="921e5-167">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="921e5-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="921e5-168">関連項目</span><span class="sxs-lookup"><span data-stu-id="921e5-168">See also</span></span>



[<span data-ttu-id="921e5-169">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="921e5-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="921e5-170">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="921e5-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="921e5-171">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="921e5-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="921e5-172">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="921e5-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

