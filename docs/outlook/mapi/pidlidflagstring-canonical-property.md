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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b3cd88db7e93b53990cf0181af623ebca75f0c6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357786"
---
# <a name="pidlidflagstring-canonical-property"></a><span data-ttu-id="552ea-103">PidLidFlagString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="552ea-103">PidLidFlagString Canonical Property</span></span>

  
  
<span data-ttu-id="552ea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="552ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="552ea-105">フラグに関連付けられた定義済みのテキスト文字列のセットのいずれかを識別するインデックスを含みます。</span><span class="sxs-lookup"><span data-stu-id="552ea-105">Contains an index that identifies one of a set of pre-defined text strings associated with the flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="552ea-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="552ea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="552ea-107">dispidFlagStringEnum</span><span class="sxs-lookup"><span data-stu-id="552ea-107">dispidFlagStringEnum</span></span>  <br/> |
|<span data-ttu-id="552ea-108">プロパティ セット:</span><span class="sxs-lookup"><span data-stu-id="552ea-108">Property set:</span></span>  <br/> |<span data-ttu-id="552ea-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="552ea-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="552ea-110">長い ID (LID):</span><span class="sxs-lookup"><span data-stu-id="552ea-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="552ea-111">0x000085C0</span><span class="sxs-lookup"><span data-stu-id="552ea-111">0x000085C0</span></span>  <br/> |
|<span data-ttu-id="552ea-112">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="552ea-112">Data type:</span></span>  <br/> |<span data-ttu-id="552ea-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="552ea-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="552ea-114">エリア:</span><span class="sxs-lookup"><span data-stu-id="552ea-114">Area:</span></span>  <br/> |<span data-ttu-id="552ea-115">タスク</span><span class="sxs-lookup"><span data-stu-id="552ea-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="552ea-116">注釈</span><span class="sxs-lookup"><span data-stu-id="552ea-116">Remarks</span></span>

<span data-ttu-id="552ea-117">このプロパティが設定されている場合、クライアントは以下の表で対応する文字列値を使用する必要があります (たとえば、現在のユーザーの言語に変換される文字列を置き換える場合 **)、dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) と **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) で設定された値を無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="552ea-117">If this property is set, clients should use the corresponding string value in the tables below (for example, to substitute a string that is translated into the current user's language), and should ignore the value set in **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) and **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).</span></span> 
  
<span data-ttu-id="552ea-118">連絡先オブジェクトに対してユーザーに提案される既定値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="552ea-118">Defaults suggested to the user for contact objects are as follows:</span></span>
  
|<span data-ttu-id="552ea-119">**値**</span><span class="sxs-lookup"><span data-stu-id="552ea-119">**Value**</span></span>|<span data-ttu-id="552ea-120">**英語の文字列**</span><span class="sxs-lookup"><span data-stu-id="552ea-120">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="552ea-121">0x00000000または存在しない</span><span class="sxs-lookup"><span data-stu-id="552ea-121">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="552ea-122">**dispidFlagRequest の表示に関連するガイダンスに従います**。</span><span class="sxs-lookup"><span data-stu-id="552ea-122">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="552ea-123">0x0000006E</span><span class="sxs-lookup"><span data-stu-id="552ea-123">0x0000006E</span></span>  <br/> |<span data-ttu-id="552ea-124">"フォローアップ"</span><span class="sxs-lookup"><span data-stu-id="552ea-124">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="552ea-125">0x0000006F</span><span class="sxs-lookup"><span data-stu-id="552ea-125">0x0000006F</span></span>  <br/> |<span data-ttu-id="552ea-126">"Call"</span><span class="sxs-lookup"><span data-stu-id="552ea-126">"Call"</span></span>  <br/> |
|<span data-ttu-id="552ea-127">0x00000070</span><span class="sxs-lookup"><span data-stu-id="552ea-127">0x00000070</span></span>  <br/> |<span data-ttu-id="552ea-128">"会議の手配"</span><span class="sxs-lookup"><span data-stu-id="552ea-128">"Arrange Meeting"</span></span>  <br/> |
|<span data-ttu-id="552ea-129">0x00000071</span><span class="sxs-lookup"><span data-stu-id="552ea-129">0x00000071</span></span>  <br/> |<span data-ttu-id="552ea-130">"メールの送信"</span><span class="sxs-lookup"><span data-stu-id="552ea-130">"Send Email"</span></span>  <br/> |
|<span data-ttu-id="552ea-131">0x00000072</span><span class="sxs-lookup"><span data-stu-id="552ea-131">0x00000072</span></span>  <br/> |<span data-ttu-id="552ea-132">"Send Letter"</span><span class="sxs-lookup"><span data-stu-id="552ea-132">"Send Letter"</span></span>  <br/> |
   
<span data-ttu-id="552ea-133">他のすべてのメッセージ オブジェクトに対してユーザーに提案される既定値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="552ea-133">Defaults suggested to the user for all other message objects are as follows:</span></span>
  
|<span data-ttu-id="552ea-134">**値**</span><span class="sxs-lookup"><span data-stu-id="552ea-134">**Value**</span></span>|<span data-ttu-id="552ea-135">**英語の文字列**</span><span class="sxs-lookup"><span data-stu-id="552ea-135">**English string**</span></span>|
|:-----|:-----|
|<span data-ttu-id="552ea-136">0x00000000または存在しない</span><span class="sxs-lookup"><span data-stu-id="552ea-136">0x00000000 or not present</span></span>  <br/> | <span data-ttu-id="552ea-137">**dispidFlagRequest の表示に関連するガイダンスに従います**。</span><span class="sxs-lookup"><span data-stu-id="552ea-137">Follow the guidance related to displaying **dispidFlagRequest**.</span></span>  <br/> |
|<span data-ttu-id="552ea-138">0x00000001</span><span class="sxs-lookup"><span data-stu-id="552ea-138">0x00000001</span></span>  <br/> |<span data-ttu-id="552ea-139">"Call"</span><span class="sxs-lookup"><span data-stu-id="552ea-139">"Call"</span></span>  <br/> |
|<span data-ttu-id="552ea-140">0x00000002</span><span class="sxs-lookup"><span data-stu-id="552ea-140">0x00000002</span></span>  <br/> |<span data-ttu-id="552ea-141">"転送しない"</span><span class="sxs-lookup"><span data-stu-id="552ea-141">"Do not Forward"</span></span>  <br/> |
|<span data-ttu-id="552ea-142">0x00000003</span><span class="sxs-lookup"><span data-stu-id="552ea-142">0x00000003</span></span>  <br/> |<span data-ttu-id="552ea-143">"フォローアップ"</span><span class="sxs-lookup"><span data-stu-id="552ea-143">"Follow up"</span></span>  <br/> |
|<span data-ttu-id="552ea-144">0x00000004</span><span class="sxs-lookup"><span data-stu-id="552ea-144">0x00000004</span></span>  <br/> |<span data-ttu-id="552ea-145">"For Your Information"</span><span class="sxs-lookup"><span data-stu-id="552ea-145">"For Your Information"</span></span>  <br/> |
|<span data-ttu-id="552ea-146">0x00000005</span><span class="sxs-lookup"><span data-stu-id="552ea-146">0x00000005</span></span>  <br/> |<span data-ttu-id="552ea-147">"転送する"</span><span class="sxs-lookup"><span data-stu-id="552ea-147">"Forward"</span></span>  <br/> |
|<span data-ttu-id="552ea-148">0x00000006</span><span class="sxs-lookup"><span data-stu-id="552ea-148">0x00000006</span></span>  <br/> |<span data-ttu-id="552ea-149">"応答不要"</span><span class="sxs-lookup"><span data-stu-id="552ea-149">"No Response Necessary"</span></span>  <br/> |
|<span data-ttu-id="552ea-150">0x00000007</span><span class="sxs-lookup"><span data-stu-id="552ea-150">0x00000007</span></span>  <br/> |<span data-ttu-id="552ea-151">"Read"</span><span class="sxs-lookup"><span data-stu-id="552ea-151">"Read"</span></span>  <br/> |
|<span data-ttu-id="552ea-152">0x00000008</span><span class="sxs-lookup"><span data-stu-id="552ea-152">0x00000008</span></span>  <br/> |<span data-ttu-id="552ea-153">"返信"</span><span class="sxs-lookup"><span data-stu-id="552ea-153">"Reply"</span></span>  <br/> |
|<span data-ttu-id="552ea-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="552ea-154">0x00000009</span></span>  <br/> |<span data-ttu-id="552ea-155">"全員に返信"</span><span class="sxs-lookup"><span data-stu-id="552ea-155">"Reply to All"</span></span>  <br/> |
|<span data-ttu-id="552ea-156">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="552ea-156">0x0000000A</span></span>  <br/> |<span data-ttu-id="552ea-157">"Review"</span><span class="sxs-lookup"><span data-stu-id="552ea-157">"Review"</span></span>  <br/> |
   
<span data-ttu-id="552ea-158">上記で指定した文字列はすべて、必要に応じてユーザーの言語に変換できます。</span><span class="sxs-lookup"><span data-stu-id="552ea-158">All strings specified above can be translated to the user's language, if appropriate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="552ea-159">関連リソース</span><span class="sxs-lookup"><span data-stu-id="552ea-159">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="552ea-160">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="552ea-160">Protocol specifications</span></span>

<span data-ttu-id="552ea-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="552ea-161">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="552ea-162">プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。</span><span class="sxs-lookup"><span data-stu-id="552ea-162">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="552ea-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="552ea-163">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="552ea-164">フラグに関連するプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="552ea-164">Specifies the properties and operations related to flagging.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="552ea-165">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="552ea-165">Header files</span></span>

<span data-ttu-id="552ea-166">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="552ea-166">Mapidefs.h</span></span>
  
> <span data-ttu-id="552ea-167">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="552ea-167">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="552ea-168">関連項目</span><span class="sxs-lookup"><span data-stu-id="552ea-168">See also</span></span>



[<span data-ttu-id="552ea-169">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="552ea-169">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="552ea-170">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="552ea-170">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="552ea-171">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="552ea-171">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="552ea-172">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="552ea-172">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

