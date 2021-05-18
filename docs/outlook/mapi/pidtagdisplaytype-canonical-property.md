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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: da26fd2a8643817cf60adbfa6f4e85da345b875c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360782"
---
# <a name="pidtagdisplaytype-canonical-property"></a><span data-ttu-id="8c4e6-103">PidTagDisplayType 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8c4e6-103">PidTagDisplayType Canonical Property</span></span>

  
  
<span data-ttu-id="8c4e6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8c4e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8c4e6-105">アイコンをテーブルの特定の行に関連付けるのに使用する値を含む。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-105">Contains a value used to associate an icon with a particular row of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8c4e6-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="8c4e6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8c4e6-107">PR_DISPLAY_TYPE</span><span class="sxs-lookup"><span data-stu-id="8c4e6-107">PR_DISPLAY_TYPE</span></span>  <br/> |
|<span data-ttu-id="8c4e6-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="8c4e6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8c4e6-109">0x3900</span><span class="sxs-lookup"><span data-stu-id="8c4e6-109">0x3900</span></span>  <br/> |
|<span data-ttu-id="8c4e6-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="8c4e6-110">Data type:</span></span>  <br/> |<span data-ttu-id="8c4e6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8c4e6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8c4e6-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="8c4e6-112">Area:</span></span>  <br/> |<span data-ttu-id="8c4e6-113">MAPI アドレス帳</span><span class="sxs-lookup"><span data-stu-id="8c4e6-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c4e6-114">注釈</span><span class="sxs-lookup"><span data-stu-id="8c4e6-114">Remarks</span></span>

<span data-ttu-id="8c4e6-115">このプロパティには長整数が含まれているので、その型に基づいてテーブル エントリを特別に処理できます。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-115">This property contains a long integer that facilitates special treatment of the table entry based on its type.</span></span> <span data-ttu-id="8c4e6-116">通常、この特別な処理は、表示の種類に関連付けられたアイコン、または他の表示要素を表示して構成されます。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-116">This special treatment typically consists of displaying an icon, or other display element, associated with the display type.</span></span> 
  
<span data-ttu-id="8c4e6-117">このプロパティは、フォルダーコンテンツ テーブルでは使用されません。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-117">This property is not used in folder contents tables.</span></span> <span data-ttu-id="8c4e6-118">クライアント アプリケーションは、メッセージの **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティと適切な [IMAPIFormInfo](imapiforminfoimapiprop.md) インターフェイスを使用して、そのメッセージの **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) プロパティと **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-118">Client applications should use a message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property and appropriate [IMAPIFormInfo](imapiforminfoimapiprop.md) interface to get the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties for that message.</span></span> 
  
<span data-ttu-id="8c4e6-119">このプロパティには、次のいずれかの値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="8c4e6-120">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="8c4e6-120">DT_AGENT</span></span> 
  
> <span data-ttu-id="8c4e6-121">自動エージェント (Quote-Of-The-Day や天気予報グラフの表示など)。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-121">An automated agent, such as Quote-Of-The-Day or a weather chart display.</span></span>
    
<span data-ttu-id="8c4e6-122">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="8c4e6-122">DT_DISTLIST</span></span> 
  
> <span data-ttu-id="8c4e6-123">配布リスト。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-123">A distribution list.</span></span>
    
<span data-ttu-id="8c4e6-124">DT_FOLDER</span><span class="sxs-lookup"><span data-stu-id="8c4e6-124">DT_FOLDER</span></span> 
  
> <span data-ttu-id="8c4e6-125">フォルダーの横に既定のフォルダー アイコンを表示します。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-125">Display default folder icon adjacent to folder.</span></span>
    
<span data-ttu-id="8c4e6-126">DT_FOLDER_LINK</span><span class="sxs-lookup"><span data-stu-id="8c4e6-126">DT_FOLDER_LINK</span></span> 
  
> <span data-ttu-id="8c4e6-127">既定のフォルダー アイコンではなく、フォルダーの横に既定のフォルダー リンク アイコンを表示します。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-127">Display default folder link icon adjacent to folder rather than the default folder icon.</span></span>
    
<span data-ttu-id="8c4e6-128">DT_FOLDER_SPECIAL</span><span class="sxs-lookup"><span data-stu-id="8c4e6-128">DT_FOLDER_SPECIAL</span></span> 
  
> <span data-ttu-id="8c4e6-129">特殊な種類のパブリック フォルダーなど、アプリケーション固有の区別を持つフォルダーの表示アイコン。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-129">Display icon for a folder with an application-specific distinction, such as a special type of public folder.</span></span>
    
<span data-ttu-id="8c4e6-130">DT_FORUM</span><span class="sxs-lookup"><span data-stu-id="8c4e6-130">DT_FORUM</span></span> 
  
> <span data-ttu-id="8c4e6-131">掲示板サービス、パブリック フォルダーまたは共有フォルダーなどのフォーラム。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-131">A forum, such as a bulletin board service or a public or shared folder.</span></span>
    
<span data-ttu-id="8c4e6-132">DT_GLOBAL</span><span class="sxs-lookup"><span data-stu-id="8c4e6-132">DT_GLOBAL</span></span> 
  
> <span data-ttu-id="8c4e6-133">グローバル アドレス帳。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-133">A global address book.</span></span>
    
<span data-ttu-id="8c4e6-134">DT_LOCAL</span><span class="sxs-lookup"><span data-stu-id="8c4e6-134">DT_LOCAL</span></span> 
  
> <span data-ttu-id="8c4e6-135">小さなワークグループと共有するローカル アドレス帳。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-135">A local address book that you share with a small workgroup.</span></span>
    
<span data-ttu-id="8c4e6-136">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="8c4e6-136">DT_MAILUSER</span></span> 
  
> <span data-ttu-id="8c4e6-137">一般的なメッセージング ユーザー。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-137">A typical messaging user.</span></span>
    
<span data-ttu-id="8c4e6-138">DT_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="8c4e6-138">DT_MODIFIABLE</span></span> 
  
> <span data-ttu-id="8c4e6-139">変更可能。コンテナーは、ユーザー インターフェイスで変更可能として示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-139">Modifiable; the container should be denoted as modifiable in the user interface.</span></span>
    
<span data-ttu-id="8c4e6-140">DT_NOT_SPECIFIC</span><span class="sxs-lookup"><span data-stu-id="8c4e6-140">DT_NOT_SPECIFIC</span></span> 
  
> <span data-ttu-id="8c4e6-141">他の設定と一致しません。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-141">Does not match any of the other settings.</span></span>
    
<span data-ttu-id="8c4e6-142">DT_ORGANIZATION</span><span class="sxs-lookup"><span data-stu-id="8c4e6-142">DT_ORGANIZATION</span></span> 
  
> <span data-ttu-id="8c4e6-143">ヘルプデスク、会計、血液駆動コーディネーターなど、大規模なグループに対して定義された特別なエイリアス。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-143">A special alias defined for a large group, such as helpdesk, accounting, or blood-drive coordinator.</span></span>
    
<span data-ttu-id="8c4e6-144">DT_PRIVATE_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="8c4e6-144">DT_PRIVATE_DISTLIST</span></span> 
  
> <span data-ttu-id="8c4e6-145">個人管理の配布リスト。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-145">A private, personally administered distribution list.</span></span>
    
<span data-ttu-id="8c4e6-146">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="8c4e6-146">DT_REMOTE_MAILUSER</span></span> 
  
> <span data-ttu-id="8c4e6-147">外部メッセージング システムまたはリモート メッセージング システムからの受信者。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-147">A recipient known to be from a foreign or remote messaging system.</span></span>
    
<span data-ttu-id="8c4e6-148">DT_WAN</span><span class="sxs-lookup"><span data-stu-id="8c4e6-148">DT_WAN</span></span> 
  
> <span data-ttu-id="8c4e6-149">ワイド エリア ネットワーク アドレス帳。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-149">A wide area network address book.</span></span>
    
<span data-ttu-id="8c4e6-150">アドレス帳のコンテンツ テーブルでは、DT_AGENT、DT_DISTLIST、DT_FORUM、DT_MAILUSER、DT_ORGANIZATION、DT_PRIVATE_DISTLIST、DT_REMOTE_MAILUSER の値をDT_REMOTE_MAILUSERします。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-150">Address book contents tables use the DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST, and DT_REMOTE_MAILUSER values.</span></span> <span data-ttu-id="8c4e6-151">アドレス帳階層テーブルと 1 回割り当てテーブルでは、DT_GLOBAL、DT_LOCAL、DT_MODIFIABLE、DT_NOT_SPECIFIC、DT_WANが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-151">Address book hierarchy tables and one-off tables use the DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC, and DT_WAN values.</span></span> <span data-ttu-id="8c4e6-152">フォルダー階層テーブルは、DT_FOLDER、DT_FOLDER_LINK、およびDT_FOLDER_SPECIAL使用します。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-152">Folder hierarchy tables use the DT_FOLDER, DT_FOLDER_LINK, and DT_FOLDER_SPECIAL values.</span></span> 
  
<span data-ttu-id="8c4e6-153">このプロパティを設定しない場合、クライアントはテーブルに適した既定の型 (通常はテーブル、DT_FOLDER、DT_LOCAL、またはDT_MAILUSER。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-153">If this property is not set, the client should assume the default type appropriate for the table, typically DT_FOLDER, DT_LOCAL, or DT_MAILUSER.</span></span> 
  
 <span data-ttu-id="8c4e6-154">**メモ** 文書化されていないすべての値は、MAPI 用に予約されています。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-154">**Note** All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="8c4e6-155">クライアント アプリケーションは、新しい値を定義し、文書化されていない値を処理する準備をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-155">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8c4e6-156">関連リソース</span><span class="sxs-lookup"><span data-stu-id="8c4e6-156">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8c4e6-157">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="8c4e6-157">Protocol specifications</span></span>

<span data-ttu-id="8c4e6-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c4e6-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c4e6-159">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-159">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8c4e6-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c4e6-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c4e6-161">メッセージ オブジェクトと添付ファイル オブジェクトを処理します。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-161">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="8c4e6-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c4e6-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c4e6-163">アドレス帳テンプレートで許容されるプロパティと操作を指定します。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-163">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="8c4e6-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8c4e6-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8c4e6-165">ディレクトリ アクセスを有効にする。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-165">Enables directory access.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8c4e6-166">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="8c4e6-166">Header files</span></span>

<span data-ttu-id="8c4e6-167">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8c4e6-167">Mapidefs.h</span></span>
  
> <span data-ttu-id="8c4e6-168">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-168">Provides data type definitions.</span></span>
    
<span data-ttu-id="8c4e6-169">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8c4e6-169">Mapitags.h</span></span>
  
> <span data-ttu-id="8c4e6-170">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="8c4e6-170">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8c4e6-171">関連項目</span><span class="sxs-lookup"><span data-stu-id="8c4e6-171">See also</span></span>



[<span data-ttu-id="8c4e6-172">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="8c4e6-172">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8c4e6-173">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="8c4e6-173">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8c4e6-174">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8c4e6-174">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8c4e6-175">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="8c4e6-175">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

