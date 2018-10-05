---
title: PidTagDisplayType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: da26fd2a8643817cf60adbfa6f4e85da345b875c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393470"
---
# <a name="pidtagdisplaytype-canonical-property"></a><span data-ttu-id="806fa-103">PidTagDisplayType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="806fa-103">PidTagDisplayType Canonical Property</span></span>

  
  
<span data-ttu-id="806fa-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="806fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="806fa-105">テーブルの特定の行にアイコンを関連付けるに使用する値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="806fa-105">Contains a value used to associate an icon with a particular row of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="806fa-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="806fa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="806fa-107">PR_DISPLAY_TYPE</span><span class="sxs-lookup"><span data-stu-id="806fa-107">PR_DISPLAY_TYPE</span></span>  <br/> |
|<span data-ttu-id="806fa-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="806fa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="806fa-109">0x3900</span><span class="sxs-lookup"><span data-stu-id="806fa-109">0x3900</span></span>  <br/> |
|<span data-ttu-id="806fa-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="806fa-110">Data type:</span></span>  <br/> |<span data-ttu-id="806fa-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="806fa-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="806fa-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="806fa-112">Area:</span></span>  <br/> |<span data-ttu-id="806fa-113">MAPI アドレス帳</span><span class="sxs-lookup"><span data-stu-id="806fa-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="806fa-114">備考</span><span class="sxs-lookup"><span data-stu-id="806fa-114">Remarks</span></span>

<span data-ttu-id="806fa-115">このプロパティには、その型に基づいてテーブルのエントリの特別な処理を容易にする長整数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="806fa-115">This property contains a long integer that facilitates special treatment of the table entry based on its type.</span></span> <span data-ttu-id="806fa-116">この特別な処理は、通常、アイコン、または、表示の種類に関連付けられているその他の表示要素を表示するので構成されます。</span><span class="sxs-lookup"><span data-stu-id="806fa-116">This special treatment typically consists of displaying an icon, or other display element, associated with the display type.</span></span> 
  
<span data-ttu-id="806fa-117">フォルダーの内容のテーブルでは、このプロパティは使用されません。</span><span class="sxs-lookup"><span data-stu-id="806fa-117">This property is not used in folder contents tables.</span></span> <span data-ttu-id="806fa-118">クライアント アプリケーションは、 **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) と**PR_MINI_ICON** ([を取得するのにメッセージのプロパティの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) と[IMAPIFormInfo](imapiforminfoimapiprop.md)の適切なインターフェイスを使用する必要があります。PidTagMiniIcon](pidtagminiicon-canonical-property.md)) そのメッセージのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="806fa-118">Client applications should use a message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property and appropriate [IMAPIFormInfo](imapiforminfoimapiprop.md) interface to get the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties for that message.</span></span> 
  
<span data-ttu-id="806fa-119">このプロパティは、次の値の 1 つだけ持つことができます。</span><span class="sxs-lookup"><span data-stu-id="806fa-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="806fa-120">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="806fa-120">DT_AGENT</span></span> 
  
> <span data-ttu-id="806fa-121">その日の見積もりなど、自動化されたエージェントまたは気象のグラフ表示します。</span><span class="sxs-lookup"><span data-stu-id="806fa-121">An automated agent, such as Quote-Of-The-Day or a weather chart display.</span></span>
    
<span data-ttu-id="806fa-122">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="806fa-122">DT_DISTLIST</span></span> 
  
> <span data-ttu-id="806fa-123">配布リスト。</span><span class="sxs-lookup"><span data-stu-id="806fa-123">A distribution list.</span></span>
    
<span data-ttu-id="806fa-124">DT_FOLDER</span><span class="sxs-lookup"><span data-stu-id="806fa-124">DT_FOLDER</span></span> 
  
> <span data-ttu-id="806fa-125">フォルダーの横にある既定のフォルダー アイコンを表示します。</span><span class="sxs-lookup"><span data-stu-id="806fa-125">Display default folder icon adjacent to folder.</span></span>
    
<span data-ttu-id="806fa-126">DT_FOLDER_LINK</span><span class="sxs-lookup"><span data-stu-id="806fa-126">DT_FOLDER_LINK</span></span> 
  
> <span data-ttu-id="806fa-127">既定のフォルダー アイコンではなく既定フォルダーのリンクのアイコンがフォルダーの横にあるを表示します。</span><span class="sxs-lookup"><span data-stu-id="806fa-127">Display default folder link icon adjacent to folder rather than the default folder icon.</span></span>
    
<span data-ttu-id="806fa-128">DT_FOLDER_SPECIAL</span><span class="sxs-lookup"><span data-stu-id="806fa-128">DT_FOLDER_SPECIAL</span></span> 
  
> <span data-ttu-id="806fa-129">パブリック フォルダーの特殊な型など特定のアプリケーションの違いは、のフォルダーのアイコンを表示します。</span><span class="sxs-lookup"><span data-stu-id="806fa-129">Display icon for a folder with an application-specific distinction, such as a special type of public folder.</span></span>
    
<span data-ttu-id="806fa-130">DT_FORUM</span><span class="sxs-lookup"><span data-stu-id="806fa-130">DT_FORUM</span></span> 
  
> <span data-ttu-id="806fa-131">フォーラム、掲示板サービスなど、パブリック フォルダーまたは共有フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="806fa-131">A forum, such as a bulletin board service or a public or shared folder.</span></span>
    
<span data-ttu-id="806fa-132">DT_GLOBAL</span><span class="sxs-lookup"><span data-stu-id="806fa-132">DT_GLOBAL</span></span> 
  
> <span data-ttu-id="806fa-133">グローバル アドレス帳です。</span><span class="sxs-lookup"><span data-stu-id="806fa-133">A global address book.</span></span>
    
<span data-ttu-id="806fa-134">DT_LOCAL</span><span class="sxs-lookup"><span data-stu-id="806fa-134">DT_LOCAL</span></span> 
  
> <span data-ttu-id="806fa-135">少人数のワークグループと共有しているローカルのアドレス帳です。</span><span class="sxs-lookup"><span data-stu-id="806fa-135">A local address book that you share with a small workgroup.</span></span>
    
<span data-ttu-id="806fa-136">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="806fa-136">DT_MAILUSER</span></span> 
  
> <span data-ttu-id="806fa-137">一般的なメッセージングのユーザーです。</span><span class="sxs-lookup"><span data-stu-id="806fa-137">A typical messaging user.</span></span>
    
<span data-ttu-id="806fa-138">DT_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="806fa-138">DT_MODIFIABLE</span></span> 
  
> <span data-ttu-id="806fa-139">変更可能です。コンテナーは必要がありますと変更可能なユーザー ・ インタ フェースで示されます。</span><span class="sxs-lookup"><span data-stu-id="806fa-139">Modifiable; the container should be denoted as modifiable in the user interface.</span></span>
    
<span data-ttu-id="806fa-140">DT_NOT_SPECIFIC</span><span class="sxs-lookup"><span data-stu-id="806fa-140">DT_NOT_SPECIFIC</span></span> 
  
> <span data-ttu-id="806fa-141">他の設定のいずれかが一致しません。</span><span class="sxs-lookup"><span data-stu-id="806fa-141">Does not match any of the other settings.</span></span>
    
<span data-ttu-id="806fa-142">DT_ORGANIZATION</span><span class="sxs-lookup"><span data-stu-id="806fa-142">DT_ORGANIZATION</span></span> 
  
> <span data-ttu-id="806fa-143">ヘルプデスク、会計、または血のドライブのコーディネーターなど、大規模なグループに対して定義されている特殊なエイリアスです。</span><span class="sxs-lookup"><span data-stu-id="806fa-143">A special alias defined for a large group, such as helpdesk, accounting, or blood-drive coordinator.</span></span>
    
<span data-ttu-id="806fa-144">DT_PRIVATE_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="806fa-144">DT_PRIVATE_DISTLIST</span></span> 
  
> <span data-ttu-id="806fa-145">プライベートは、個人的には配布リストを管理します。</span><span class="sxs-lookup"><span data-stu-id="806fa-145">A private, personally administered distribution list.</span></span>
    
<span data-ttu-id="806fa-146">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="806fa-146">DT_REMOTE_MAILUSER</span></span> 
  
> <span data-ttu-id="806fa-147">既知の外部またはリモートのメッセージング システムから受信者です。</span><span class="sxs-lookup"><span data-stu-id="806fa-147">A recipient known to be from a foreign or remote messaging system.</span></span>
    
<span data-ttu-id="806fa-148">DT_WAN</span><span class="sxs-lookup"><span data-stu-id="806fa-148">DT_WAN</span></span> 
  
> <span data-ttu-id="806fa-149">ワイド エリア ネットワークのアドレス帳です。</span><span class="sxs-lookup"><span data-stu-id="806fa-149">A wide area network address book.</span></span>
    
<span data-ttu-id="806fa-150">アドレス帳の内容のテーブルでは、DT_AGENT、DT_DISTLIST、DT_FORUM、DT_MAILUSER、DT_ORGANIZATION、DT_PRIVATE_DISTLIST、および DT_REMOTE_MAILUSER の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="806fa-150">Address book contents tables use the DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST, and DT_REMOTE_MAILUSER values.</span></span> <span data-ttu-id="806fa-151">アドレス帳階層テーブルと一時テーブルは、DT_GLOBAL、DT_LOCAL、DT_MODIFIABLE、DT_NOT_SPECIFIC、および DT_WAN の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="806fa-151">Address book hierarchy tables and one-off tables use the DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC, and DT_WAN values.</span></span> <span data-ttu-id="806fa-152">フォルダーの階層テーブルには、DT_FOLDER、DT_FOLDER_LINK、DT_FOLDER_SPECIAL の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="806fa-152">Folder hierarchy tables use the DT_FOLDER, DT_FOLDER_LINK, and DT_FOLDER_SPECIAL values.</span></span> 
  
<span data-ttu-id="806fa-153">このプロパティが設定されていない場合、クライアントを想定してください既定の型、テーブル、通常 DT_FOLDER、DT_LOCAL、または DT_MAILUSER の適切です。</span><span class="sxs-lookup"><span data-stu-id="806fa-153">If this property is not set, the client should assume the default type appropriate for the table, typically DT_FOLDER, DT_LOCAL, or DT_MAILUSER.</span></span> 
  
 <span data-ttu-id="806fa-154">**メモ**記載されていないすべての値は、MAPI 用に予約されています。</span><span class="sxs-lookup"><span data-stu-id="806fa-154">**Note** All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="806fa-155">クライアント アプリケーションは、新しい値を定義する必要がないと、文書化されていない値で対処するために準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="806fa-155">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="806fa-156">関連リソース</span><span class="sxs-lookup"><span data-stu-id="806fa-156">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="806fa-157">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="806fa-157">Protocol specifications</span></span>

<span data-ttu-id="806fa-158">[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="806fa-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="806fa-159">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="806fa-159">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="806fa-160">[[MS OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="806fa-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="806fa-161">メッセージと添付ファイルのオブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="806fa-161">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="806fa-162">[[MS OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="806fa-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="806fa-163">プロパティは、アドレス帳のテンプレートの許可の操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="806fa-163">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="806fa-164">[[MS OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="806fa-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="806fa-165">ディレクトリのアクセスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="806fa-165">Enables directory access.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="806fa-166">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="806fa-166">Header files</span></span>

<span data-ttu-id="806fa-167">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="806fa-167">Mapidefs.h</span></span>
  
> <span data-ttu-id="806fa-168">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="806fa-168">Provides data type definitions.</span></span>
    
<span data-ttu-id="806fa-169">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="806fa-169">Mapitags.h</span></span>
  
> <span data-ttu-id="806fa-170">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="806fa-170">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="806fa-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="806fa-171">See also</span></span>



[<span data-ttu-id="806fa-172">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="806fa-172">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="806fa-173">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="806fa-173">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="806fa-174">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="806fa-174">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="806fa-175">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="806fa-175">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

