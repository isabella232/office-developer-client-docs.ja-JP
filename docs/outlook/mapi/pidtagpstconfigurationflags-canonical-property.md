---
title: PidTagPstConfigurationFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b79b40a59a2bf7b68c58bffbccca04034b853a15
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570206"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="98694-103">PidTagPstConfigurationFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="98694-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="98694-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98694-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98694-105">個人用領域 (.pst ファイル) テーブルの構成フラグをオン表示されるようです。</span><span class="sxs-lookup"><span data-stu-id="98694-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98694-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="98694-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="98694-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="98694-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="98694-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="98694-108">Identifier:</span></span>  <br/> |<span data-ttu-id="98694-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="98694-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="98694-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="98694-110">Data type:</span></span>  <br/> |<span data-ttu-id="98694-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="98694-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="98694-112">領域:</span><span class="sxs-lookup"><span data-stu-id="98694-112">Area:</span></span>  <br/> |<span data-ttu-id="98694-113">パーソナル ストレージ表 (.pst) 内部</span><span class="sxs-lookup"><span data-stu-id="98694-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98694-114">注釈</span><span class="sxs-lookup"><span data-stu-id="98694-114">Remarks</span></span>

<span data-ttu-id="98694-115">以下は、このプロパティの有効な値です。</span><span class="sxs-lookup"><span data-stu-id="98694-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="98694-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="98694-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="98694-117">Unicode の .pst ファイルを示します。</span><span class="sxs-lookup"><span data-stu-id="98694-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="98694-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="98694-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="98694-119">クライアントから設定フラグ、 [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドを**ConfigureMsgService**を[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)の呼び出しと同様に扱われ、「このインフォメーション サービスが構成されていません」をスキップ警告します。</span><span class="sxs-lookup"><span data-stu-id="98694-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="98694-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="98694-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="98694-121">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値を変更するのには**ConfigureMsgService**は、指定されていてもに指示します。</span><span class="sxs-lookup"><span data-stu-id="98694-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="98694-122">その場合は、新しい .pst ファイルに対してのみ、指定されました。</span><span class="sxs-lookup"><span data-stu-id="98694-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="98694-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="98694-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="98694-124">構成コードは、オフライン フォルダー (.ost) ファイルがされているかどうかを確認するダイアログ ボックスが、ユーザーの応答によって検出されたオフライン フォルダーを使用してか、または別のオフライン フォルダーを参照するユーザーを有効にする最初に表示するように指示します。</span><span class="sxs-lookup"><span data-stu-id="98694-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="98694-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="98694-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="98694-126">新しい一意の名前を使用して .ost ファイルをコピーし、現在の名前を破棄します。</span><span class="sxs-lookup"><span data-stu-id="98694-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="98694-127">既存の .ost ファイルは、コンピューター上に残りますが、このプロファイルでは使用されなく。</span><span class="sxs-lookup"><span data-stu-id="98694-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="98694-128">これは通常、Microsoft Outlook は、特定の .ost ファイルを許可しないと、レジストリ ポリシーは、ファイルの名前を変更するユーザーを許可しない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="98694-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="98694-129">関連リソース</span><span class="sxs-lookup"><span data-stu-id="98694-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="98694-130">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="98694-130">Protocol specifications</span></span>

<span data-ttu-id="98694-131">[MS OXPROPS]</span><span class="sxs-lookup"><span data-stu-id="98694-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="98694-132">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="98694-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="98694-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="98694-133">Header files</span></span>

<span data-ttu-id="98694-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="98694-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="98694-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="98694-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="98694-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="98694-136">Mapitags.h</span></span>
  
> <span data-ttu-id="98694-137">関連付けられているプロパティとして記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="98694-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="98694-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="98694-138">See also</span></span>



[<span data-ttu-id="98694-139">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="98694-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="98694-140">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="98694-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="98694-141">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="98694-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="98694-142">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="98694-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

