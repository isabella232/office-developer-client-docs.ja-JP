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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 029df4397f4d24c7c111d2017d34e6403df367d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325635"
---
# <a name="pidtagmessageeditorformat-canonical-property"></a><span data-ttu-id="55924-103">PidTagMessageEditorFormat 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="55924-103">PidTagMessageEditorFormat Canonical Property</span></span>

  
  
<span data-ttu-id="55924-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55924-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55924-105">メッセージの表示に使用するエディターの形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="55924-105">Specifies the format for an editor to use to display a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55924-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="55924-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55924-107">PR_MSG_EDITOR_FORMAT</span><span class="sxs-lookup"><span data-stu-id="55924-107">PR_MSG_EDITOR_FORMAT</span></span>  <br/> |
|<span data-ttu-id="55924-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="55924-108">Identifier:</span></span>  <br/> |<span data-ttu-id="55924-109">0x5909</span><span class="sxs-lookup"><span data-stu-id="55924-109">0x5909</span></span>  <br/> |
|<span data-ttu-id="55924-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="55924-110">Data type:</span></span>  <br/> |<span data-ttu-id="55924-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="55924-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="55924-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="55924-112">Area:</span></span>  <br/> |<span data-ttu-id="55924-113">その他</span><span class="sxs-lookup"><span data-stu-id="55924-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55924-114">注釈</span><span class="sxs-lookup"><span data-stu-id="55924-114">Remarks</span></span>

<span data-ttu-id="55924-115">指定できる値は **PR_MSG_EDITOR_FORMAT** のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="55924-115">The possible values for **PR_MSG_EDITOR_FORMAT** can be one of the following:</span></span> 
  
|<span data-ttu-id="55924-116">**値**</span><span class="sxs-lookup"><span data-stu-id="55924-116">**Value**</span></span>|<span data-ttu-id="55924-117">**説明**</span><span class="sxs-lookup"><span data-stu-id="55924-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55924-118">**EDITOR_FORMAT_DONTKNOW**</span><span class="sxs-lookup"><span data-stu-id="55924-118">**EDITOR_FORMAT_DONTKNOW**</span></span> <br/> |<span data-ttu-id="55924-119">エディターで使用する形式が不明です。</span><span class="sxs-lookup"><span data-stu-id="55924-119">The format for the editor to use is unknown.</span></span>  <br/> |
|<span data-ttu-id="55924-120">**EDITOR_FORMAT_PLAINTEXT**</span><span class="sxs-lookup"><span data-stu-id="55924-120">**EDITOR_FORMAT_PLAINTEXT**</span></span> <br/> |<span data-ttu-id="55924-121">エディターはメッセージをプレーン テキスト形式で表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55924-121">The editor should display the message in plain text format.</span></span>  <br/> |
|<span data-ttu-id="55924-122">**EDITOR_FORMAT_HTML**</span><span class="sxs-lookup"><span data-stu-id="55924-122">**EDITOR_FORMAT_HTML**</span></span> <br/> |<span data-ttu-id="55924-123">エディターはメッセージを HTML 形式で表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55924-123">The editor should display the message in HTML format.</span></span>  <br/> |
|<span data-ttu-id="55924-124">**EDITOR_FORMAT_RTF**</span><span class="sxs-lookup"><span data-stu-id="55924-124">**EDITOR_FORMAT_RTF**</span></span> <br/> |<span data-ttu-id="55924-125">エディターはリッチ テキスト形式でメッセージを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55924-125">The editor should display the message in Rich Text Format.</span></span>  <br/> |
   
<span data-ttu-id="55924-126">既定では、メール メッセージ (メッセージ クラス **IPM を含む)。メモ** または IPM から派生したカスタム メッセージ クラス **を使用します。注**) は、POP3/SMTP メール アカウントから送信され、トランスポート ニュートラル カプセル化形式 (TNEF) で送信されます。</span><span class="sxs-lookup"><span data-stu-id="55924-126">By default, mail messages (with the message class **IPM.Note** or with a custom message class derived from **IPM.Note**) sent from a POP3/SMTP mail account are sent in the Transport Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="55924-127">PR_MSG_EDITOR_FORMATプロパティ **を** 使用すると、メッセージの送信時に TNEF ではなくプレーン テキストのみを適用できます。</span><span class="sxs-lookup"><span data-stu-id="55924-127">The **PR_MSG_EDITOR_FORMAT** property can be used to enforce only plain text, and not TNEF, when sending a message.</span></span> <span data-ttu-id="55924-128">この **PR_MSG_EDITOR_FORMAT** に **設定されている場合** EDITOR_FORMAT_PLAINTEXT、メッセージは TNEF なしでプレーン テキストとして送信されます。</span><span class="sxs-lookup"><span data-stu-id="55924-128">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_PLAINTEXT**, the message is sent as plain text without TNEF.</span></span> <span data-ttu-id="55924-129">PR_MSG_EDITOR_FORMAT **が** **EDITOR_FORMAT_RTF** に設定されている場合、TNEF エンコードは暗黙的に有効にされ、メッセージはクライアントで指定された既定のインターネット形式を使用してOutlookされます。</span><span class="sxs-lookup"><span data-stu-id="55924-129">If **PR_MSG_EDITOR_FORMAT** is set to **EDITOR_FORMAT_RTF**, TNEF encoding is implicitly enabled, and the message is sent by using the default Internet format that is specified in the Outlook client.</span></span>
  
<span data-ttu-id="55924-130">メッセージの送信時に TNEF の使用を強制するには、他に 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="55924-130">There are two other ways to enforce the use of TNEF when sending a message.</span></span>
  
- <span data-ttu-id="55924-131">メッセージの **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) 名前付きプロパティを True に設定すると、MAPI から MIME/SMTP にメッセージを変換するときに TNEF を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="55924-131">Setting the **dispidUseTNEF** ([PidLidUseTnef](pidlidusetnef-canonical-property.md)) named property to True on a message indicates TNEF should be included when converting the message from MAPI to MIME/SMTP.</span></span> <span data-ttu-id="55924-132">**dispidUseTNEF** は、メッセージが POP3/SMTP メール アカウントから送信された場合にのみ適用され、メッセージが Microsoft Exchange Server などの他のプロバイダーによって送信された場合は適用されません。</span><span class="sxs-lookup"><span data-stu-id="55924-132">Note that **dispidUseTNEF** only applies when the message is sent from a POP3/SMTP mail account, and does not apply when the message is sent by other providers, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="55924-133">**dispidUseTNEF は**、 の設定を **オーバーライドPR_MSG_EDITOR_FORMAT。**</span><span class="sxs-lookup"><span data-stu-id="55924-133">**dispidUseTNEF** overrides the setting in **PR_MSG_EDITOR_FORMAT**.</span></span>
    
- <span data-ttu-id="55924-134">[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)を呼び出す際に CCSF_USE_TNEF フラグを使用して発信 MAPI メッセージを MIME ストリームに変換すると、TNEF も強制できます。 </span><span class="sxs-lookup"><span data-stu-id="55924-134">Using the **CCSF_USE_TNEF** flag when calling [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) to convert an outgoing MAPI message to a MIME stream can also enforce TNEF.</span></span> <span data-ttu-id="55924-135">これは **、dispidUseTNEF** が設定されていない場合でも適用されます。</span><span class="sxs-lookup"><span data-stu-id="55924-135">This applies even if **dispidUseTNEF** is not set.</span></span> 
    
## <a name="related-resources"></a><span data-ttu-id="55924-136">関連リソース</span><span class="sxs-lookup"><span data-stu-id="55924-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55924-137">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="55924-137">Protocol specifications</span></span>

<span data-ttu-id="55924-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55924-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55924-139">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="55924-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="55924-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55924-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55924-141">リモート操作で使用される基本的なデータ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="55924-141">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="55924-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55924-142">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55924-143">電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="55924-143">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55924-144">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="55924-144">Header files</span></span>

<span data-ttu-id="55924-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55924-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="55924-146">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="55924-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="55924-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="55924-147">Mapitags.h</span></span>
  
> <span data-ttu-id="55924-148">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="55924-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55924-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="55924-149">See also</span></span>



[<span data-ttu-id="55924-150">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="55924-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55924-151">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="55924-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55924-152">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="55924-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55924-153">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="55924-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

