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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408944"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="effc7-103">PidTagPstConfigurationFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="effc7-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="effc7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="effc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="effc7-105">個人用ストレージ テーブル (.pst ファイル) の構成フラグを指定します。</span><span class="sxs-lookup"><span data-stu-id="effc7-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="effc7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="effc7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="effc7-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="effc7-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="effc7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="effc7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="effc7-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="effc7-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="effc7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="effc7-110">Data type:</span></span>  <br/> |<span data-ttu-id="effc7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="effc7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="effc7-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="effc7-112">Area:</span></span>  <br/> |<span data-ttu-id="effc7-113">個人用ストレージ テーブル (.pst) 内部</span><span class="sxs-lookup"><span data-stu-id="effc7-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="effc7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="effc7-114">Remarks</span></span>

<span data-ttu-id="effc7-115">このプロパティの有効な値を次に示します。</span><span class="sxs-lookup"><span data-stu-id="effc7-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="effc7-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="effc7-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="effc7-117">Unicode .pst ファイルを示します。</span><span class="sxs-lookup"><span data-stu-id="effc7-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="effc7-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="effc7-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="effc7-119">クライアント フラグから [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) メソッドに設定すると **、ConfigureMsgService** は [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) 呼び出しのように扱い、「この情報サービスが構成されていません」という警告をスキップします。</span><span class="sxs-lookup"><span data-stu-id="effc7-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="effc7-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="effc7-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="effc7-121">**ConfigureMsgService に**、指定された場合でも、PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値を変更しなくします。</span><span class="sxs-lookup"><span data-stu-id="effc7-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="effc7-122">その場合は、新しい .pst ファイルにのみ提供されました。</span><span class="sxs-lookup"><span data-stu-id="effc7-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="effc7-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="effc7-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="effc7-124">構成コードに、最初にダイアログ ボックスを表示して、オフライン フォルダー (.ost) ファイルが見つかったかどうかを確認し、ユーザーの応答に応じて、見つかったオフライン フォルダーを使用するか、ユーザーが別のオフライン フォルダーを参照できるようになります。</span><span class="sxs-lookup"><span data-stu-id="effc7-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="effc7-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="effc7-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="effc7-126">新しい一意の名前を持つ .ost ファイルをコピーし、現在の名前を破棄します。</span><span class="sxs-lookup"><span data-stu-id="effc7-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="effc7-127">既存の .ost ファイルはコンピューター上に残りますが、このプロファイルでは使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="effc7-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="effc7-128">これは通常、Microsoft Outlook特定の .ost ファイルが許可されなくなった場合に発生し、レジストリ ポリシーによってユーザーがファイルの名前を変更できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="effc7-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="effc7-129">関連リソース</span><span class="sxs-lookup"><span data-stu-id="effc7-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="effc7-130">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="effc7-130">Protocol specifications</span></span>

<span data-ttu-id="effc7-131">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="effc7-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="effc7-132">関連するプロトコル仕様へのExchange Server提供します。</span><span class="sxs-lookup"><span data-stu-id="effc7-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="effc7-133">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="effc7-133">Header files</span></span>

<span data-ttu-id="effc7-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="effc7-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="effc7-135">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="effc7-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="effc7-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="effc7-136">Mapitags.h</span></span>
  
> <span data-ttu-id="effc7-137">関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="effc7-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="effc7-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="effc7-138">See also</span></span>



[<span data-ttu-id="effc7-139">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="effc7-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="effc7-140">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="effc7-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="effc7-141">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="effc7-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="effc7-142">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="effc7-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

