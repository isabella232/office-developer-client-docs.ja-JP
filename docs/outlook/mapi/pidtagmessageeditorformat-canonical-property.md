---
title: PidTagMessageEditorFormat 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageEditorFormat
api_type:
- HeaderDef
ms.assetid: 197b21ed-9f2f-425f-a6ed-cae1208fa2ca
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 029df4397f4d24c7c111d2017d34e6403df367d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325635"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a><span data-ttu-id="2451f-103">PidTagMessageEditorFormat 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2451f-103">PidTagMessageEditorFormat Canonical Property</span></span>

  
  
<span data-ttu-id="2451f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2451f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2451f-105">エディターがメッセージの表示に使用する形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="2451f-105">Specifies the format for an editor to use to display a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2451f-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2451f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2451f-107">PR_MSG_EDITOR_FORMAT</span><span class="sxs-lookup"><span data-stu-id="2451f-107">PR_MSG_EDITOR_FORMAT</span></span>  <br/> |
|<span data-ttu-id="2451f-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2451f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2451f-109">0x5909</span><span class="sxs-lookup"><span data-stu-id="2451f-109">0x5909</span></span>  <br/> |
|<span data-ttu-id="2451f-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2451f-110">Data type:</span></span>  <br/> |<span data-ttu-id="2451f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2451f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2451f-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2451f-112">Area:</span></span>  <br/> |<span data-ttu-id="2451f-113">その他</span><span class="sxs-lookup"><span data-stu-id="2451f-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2451f-114">解説</span><span class="sxs-lookup"><span data-stu-id="2451f-114">Remarks</span></span>

<span data-ttu-id="2451f-115">**PR_MSG_EDITOR_FORMAT**に使用できる値は、次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="2451f-115">The possible values for **PR_MSG_EDITOR_FORMAT** can be one of the following:</span></span> 
  
|<span data-ttu-id="2451f-116">**値**</span><span class="sxs-lookup"><span data-stu-id="2451f-116">**Value**</span></span>|<span data-ttu-id="2451f-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="2451f-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2451f-118">**EDITOR_FORMAT_DONTKNOW**</span><span class="sxs-lookup"><span data-stu-id="2451f-118">**EDITOR_FORMAT_DONTKNOW**</span></span> <br/> |<span data-ttu-id="2451f-119">使用するエディターの形式が不明です。</span><span class="sxs-lookup"><span data-stu-id="2451f-119">The format for the editor to use is unknown.</span></span>  <br/> |
|<span data-ttu-id="2451f-120">**EDITOR_FORMAT_PLAINTEXT**</span><span class="sxs-lookup"><span data-stu-id="2451f-120">**EDITOR_FORMAT_PLAINTEXT**</span></span> <br/> |<span data-ttu-id="2451f-121">エディターは、メッセージをプレーンテキスト形式で表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2451f-121">The editor should display the message in plain text format.</span></span>  <br/> |
|<span data-ttu-id="2451f-122">**EDITOR_FORMAT_HTML**</span><span class="sxs-lookup"><span data-stu-id="2451f-122">**EDITOR_FORMAT_HTML**</span></span> <br/> |<span data-ttu-id="2451f-123">エディターによって、メッセージが HTML 形式で表示されます。</span><span class="sxs-lookup"><span data-stu-id="2451f-123">The editor should display the message in HTML format.</span></span>  <br/> |
|<span data-ttu-id="2451f-124">**EDITOR_FORMAT_RTF**</span><span class="sxs-lookup"><span data-stu-id="2451f-124">**EDITOR_FORMAT_RTF**</span></span> <br/> |<span data-ttu-id="2451f-125">エディターによって、メッセージがリッチテキスト形式で表示されます。</span><span class="sxs-lookup"><span data-stu-id="2451f-125">The editor should display the message in Rich Text Format.</span></span>  <br/> |
   
<span data-ttu-id="2451f-126">既定では、メールメッセージ (メッセージクラス**IPM.** または、IPM から派生したカスタムメッセージクラスを使用していることに注意**してください。注**) POP3/SMTP メールアカウントから送信されたメールは、トランスポートニュートラルカプセル化形式 (TNEF) で送信されます。</span><span class="sxs-lookup"><span data-stu-id="2451f-126">By default, mail messages (with the message class **IPM.Note** or with a custom message class derived from **IPM.Note**) sent from a POP3/SMTP mail account are sent in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="2451f-127">**PR_MSG_EDITOR_FORMAT**プロパティを使用すると、メッセージを送信するときに、TNEF ではなくプレーンテキストのみを適用できます。</span><span class="sxs-lookup"><span data-stu-id="2451f-127">The **PR_MSG_EDITOR_FORMAT** property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="2451f-128">**PR_MSG_EDITOR_FORMAT**が**EDITOR_FORMAT_PLAINTEXT**に設定されている場合、メッセージは TNEF なしのプレーンテキストとして送信されます。</span><span class="sxs-lookup"><span data-stu-id="2451f-128">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_PLAINTEXT**, the message is sent as plain text without TNEF.</span></span> <span data-ttu-id="2451f-129">**PR_MSG_EDITOR_FORMAT**が**EDITOR_FORMAT_RTF**に設定されている場合、TNEF エンコードは暗黙的に有効になり、メッセージは Outlook クライアントで指定された既定のインターネット形式を使用して送信されます。</span><span class="sxs-lookup"><span data-stu-id="2451f-129">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_RTF**, TNEF encoding is implicitly enabled, and the message is sent by using the default Internet format that is specified in the Outlook client.</span></span>
  
<span data-ttu-id="2451f-130">メッセージを送信するときに TNEF の使用を強制するには、他に2つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="2451f-130">There are two other ways to enforce the use of TNEF when sending a message.</span></span>
  
- <span data-ttu-id="2451f-131">メッセージで**dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) 名前付きプロパティを True に設定することは、メッセージを MAPI から MIME/SMTP に変換するときに、TNEF を含める必要があることを示しています。</span><span class="sxs-lookup"><span data-stu-id="2451f-131">Setting the **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) named property to True on a message indicates TNEF should be included when converting the message from MAPI to MIME/SMTP.</span></span> <span data-ttu-id="2451f-132">**dispidUseTNEF**は、メッセージが POP3/SMTP メールアカウントから送信された場合にのみ適用されることに注意してください。また、メッセージが他のプロバイダー (Microsoft Exchange Server など) によって送信された場合には適用されません。</span><span class="sxs-lookup"><span data-stu-id="2451f-132">Note that **dispidUseTNEF** only applies when the message is sent from a POP3/SMTP mail account, and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="2451f-133">**dispidUseTNEF**は、 **PR_MSG_EDITOR_FORMAT**の設定より優先されます。</span><span class="sxs-lookup"><span data-stu-id="2451f-133">**dispidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**.</span></span>
    
- <span data-ttu-id="2451f-134">[iconvertersession:: MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を呼び出して**CCSF_USE_TNEF**フラグを使用すると、送信 MAPI メッセージを MIME ストリームに変換できます。また、TNEF を強制することもできます。</span><span class="sxs-lookup"><span data-stu-id="2451f-134">Using the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="2451f-135">これは、 **dispidUseTNEF**が設定されていない場合でも適用されます。</span><span class="sxs-lookup"><span data-stu-id="2451f-135">This applies even if **dispidUseTNEF** is not set.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="2451f-136">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2451f-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2451f-137">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2451f-137">Protocol specifications</span></span>

<span data-ttu-id="2451f-138">[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2451f-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2451f-139">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2451f-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2451f-140">[[OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2451f-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2451f-141">リモート操作で使用される基本データ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="2451f-141">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="2451f-142">[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2451f-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2451f-143">電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="2451f-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2451f-144">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="2451f-144">Header files</span></span>

<span data-ttu-id="2451f-145">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2451f-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="2451f-146">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2451f-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="2451f-147">Mapitags</span><span class="sxs-lookup"><span data-stu-id="2451f-147">Mapitags.h</span></span>
  
> <span data-ttu-id="2451f-148">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2451f-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2451f-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="2451f-149">See also</span></span>



[<span data-ttu-id="2451f-150">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2451f-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2451f-151">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2451f-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2451f-152">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2451f-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2451f-153">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2451f-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

