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
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286409"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="2c46e-103">PidTagPstConfigurationFlags 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2c46e-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="2c46e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c46e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c46e-105">タイプの個人用ストレージテーブル (.pst ファイル) の構成フラグ。</span><span class="sxs-lookup"><span data-stu-id="2c46e-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2c46e-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="2c46e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2c46e-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="2c46e-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="2c46e-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="2c46e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2c46e-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="2c46e-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="2c46e-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="2c46e-110">Data type:</span></span>  <br/> |<span data-ttu-id="2c46e-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2c46e-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2c46e-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="2c46e-112">Area:</span></span>  <br/> |<span data-ttu-id="2c46e-113">パーソナルストレージテーブル (.pst) 内部</span><span class="sxs-lookup"><span data-stu-id="2c46e-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c46e-114">解説</span><span class="sxs-lookup"><span data-stu-id="2c46e-114">Remarks</span></span>

<span data-ttu-id="2c46e-115">このプロパティの有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2c46e-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="2c46e-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2c46e-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="2c46e-117">Unicode .pst ファイルを示します。</span><span class="sxs-lookup"><span data-stu-id="2c46e-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="2c46e-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="2c46e-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="2c46e-119">クライアントフラグから[IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドに設定した場合は、 [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md)呼び出しのような**ConfigureMsgService**を処理し、"この information service は構成されていません" を省略します。メッセージ.</span><span class="sxs-lookup"><span data-stu-id="2c46e-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="2c46e-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="2c46e-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="2c46e-121">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティの値が指定されていても、その値を変更しないように**ConfigureMsgService**に指示します。</span><span class="sxs-lookup"><span data-stu-id="2c46e-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="2c46e-122">その場合は、新しい .pst ファイルに対してのみ提供されています。</span><span class="sxs-lookup"><span data-stu-id="2c46e-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="2c46e-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="2c46e-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="2c46e-124">最初に、オフラインフォルダー (.ost) ファイルが見つかったかどうかを確認するダイアログボックスを表示し、ユーザーの応答に応じて、見つかったオフラインフォルダーを使用するか、ユーザーが別のオフラインフォルダーを参照できるようにするように指示します。</span><span class="sxs-lookup"><span data-stu-id="2c46e-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="2c46e-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="2c46e-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="2c46e-126">.ost ファイルを新しい一意の名前でコピーし、現在の名前を破棄します。</span><span class="sxs-lookup"><span data-stu-id="2c46e-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="2c46e-127">既存の .ost ファイルはコンピューターに残りますが、このプロファイルでは使用されなくなります。</span><span class="sxs-lookup"><span data-stu-id="2c46e-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="2c46e-128">これは通常、Microsoft Outlook で特定の .ost ファイルが許可されなくなり、レジストリポリシーによってユーザーがファイルの名前を変更できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="2c46e-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="2c46e-129">関連リソース</span><span class="sxs-lookup"><span data-stu-id="2c46e-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2c46e-130">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="2c46e-130">Protocol specifications</span></span>

<span data-ttu-id="2c46e-131">[[OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="2c46e-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="2c46e-132">関連する Exchange Server プロトコル仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="2c46e-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2c46e-133">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="2c46e-133">Header files</span></span>

<span data-ttu-id="2c46e-134">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2c46e-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="2c46e-135">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="2c46e-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="2c46e-136">Mapitags</span><span class="sxs-lookup"><span data-stu-id="2c46e-136">Mapitags.h</span></span>
  
> <span data-ttu-id="2c46e-137">関連するプロパティとしてリストされているプロパティの定義が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2c46e-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2c46e-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="2c46e-138">See also</span></span>



[<span data-ttu-id="2c46e-139">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="2c46e-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2c46e-140">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="2c46e-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2c46e-141">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2c46e-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2c46e-142">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="2c46e-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

