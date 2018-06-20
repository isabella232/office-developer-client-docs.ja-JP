---
title: PidTagExtendedFolderFlags の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedFolderFlags
api_type:
- HeaderDef
ms.assetid: e0c04f98-3d66-4ab5-ba05-69f9df539fcf
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 4a4d3c940539c23be8ec212cb85e3dd4f3a04aab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802745"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a><span data-ttu-id="3d6cd-103">PidTagExtendedFolderFlags の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="3d6cd-103">PidTagExtendedFolderFlags Canonical Property</span></span>
 
<span data-ttu-id="3d6cd-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3d6cd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3d6cd-105">フォルダーの拡張のフラグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-105">Contains extended flags about a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3d6cd-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3d6cd-107">PR_EXTENDED_FOLDER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="3d6cd-107">PR_EXTENDED_FOLDER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="3d6cd-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="3d6cd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3d6cd-109">0x36DA</span><span class="sxs-lookup"><span data-stu-id="3d6cd-109">0x36DA</span></span>  <br/> |
|<span data-ttu-id="3d6cd-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-110">Data type:</span></span>  <br/> |<span data-ttu-id="3d6cd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3d6cd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3d6cd-112">領域:</span><span class="sxs-lookup"><span data-stu-id="3d6cd-112">Area:</span></span>  <br/> |<span data-ttu-id="3d6cd-113">MAPI のコンテナー</span><span class="sxs-lookup"><span data-stu-id="3d6cd-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d6cd-114">備考</span><span class="sxs-lookup"><span data-stu-id="3d6cd-114">Remarks</span></span>

<span data-ttu-id="3d6cd-115">このプロパティは、エンコードされたサブ フォルダーのプロパティを含むバイナリ ストリームです。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-115">This property is a binary stream that contains encoded sub-properties for the folder.</span></span> <span data-ttu-id="3d6cd-116">それは一連の可変長サブ項目として書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-116">It is formatted as a series of variable length sub items.</span></span> <span data-ttu-id="3d6cd-117">サブ項目の最初の 8 ビットでは、[ID] フィールドは、サブ項目を表すフラグの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-117">The first 8 bits of the sub item is an ID field, which indicates what kind of flag the sub item represents.</span></span> <span data-ttu-id="3d6cd-118">2 つ目の 8 ビットは、次のデータのバイト数です。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-118">The second 8 bits is the number of bytes of data that follow.</span></span>
  
<span data-ttu-id="3d6cd-119">使用可能な ID の値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-119">Possible ID values include:</span></span>
  
- <span data-ttu-id="3d6cd-120">無効</span><span class="sxs-lookup"><span data-stu-id="3d6cd-120">Invalid</span></span>
    
   <span data-ttu-id="3d6cd-121">この値は使用しないで</span><span class="sxs-lookup"><span data-stu-id="3d6cd-121">Do not use this value</span></span>
    
- <span data-ttu-id="3d6cd-122">ExtendedFlags</span><span class="sxs-lookup"><span data-stu-id="3d6cd-122">ExtendedFlags</span></span>
    
   <span data-ttu-id="3d6cd-123">データは、4 バイトの値が設定されています。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-123">The data is a four byte value formatted as:</span></span>
    
   |<span data-ttu-id="3d6cd-124">**ビット**</span><span class="sxs-lookup"><span data-stu-id="3d6cd-124">**Bits**</span></span>|<span data-ttu-id="3d6cd-125">**説明**</span><span class="sxs-lookup"><span data-stu-id="3d6cd-125">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="3d6cd-126">0 ～ 1</span><span class="sxs-lookup"><span data-stu-id="3d6cd-126">0-1</span></span>  <br/> |<span data-ttu-id="3d6cd-127">予約済み。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-127">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="3d6cd-128">2</span><span class="sxs-lookup"><span data-stu-id="3d6cd-128">2</span></span>  <br/> |<span data-ttu-id="3d6cd-129">アプリケーション ポリシーの説明を表示する必要がある場合は 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-129">Set to 0 if the application should show a policy description.</span></span>  <br/> |
   |<span data-ttu-id="3d6cd-130">3-5</span><span class="sxs-lookup"><span data-stu-id="3d6cd-130">3-5</span></span>  <br/> |<span data-ttu-id="3d6cd-131">予約済み。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-131">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="3d6cd-132">6-7</span><span class="sxs-lookup"><span data-stu-id="3d6cd-132">6-7</span></span>  <br/> |<span data-ttu-id="3d6cd-133">フォルダー内のメッセージ数の表示を制御します。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-133">Controls the display of the number of messages in the folder.</span></span>  <br/> <span data-ttu-id="3d6cd-134">0 - 既定の設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-134">0 - Use the default setting</span></span>  <br/> <span data-ttu-id="3d6cd-135">1-未読メ ッ セージの数を使用します。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-135">1 - Use the number of unread messages</span></span>  <br/> <span data-ttu-id="3d6cd-136">3 - メッセージの合計数を使用します。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-136">3 - Use the total number of messages</span></span>  <br/> |
   |<span data-ttu-id="3d6cd-137">8-31</span><span class="sxs-lookup"><span data-stu-id="3d6cd-137">8-31</span></span>  <br/> |<span data-ttu-id="3d6cd-138">予約済み。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-138">Reserved.</span></span>  <br/> |
   
<span data-ttu-id="3d6cd-139">予約済みの項目は無視できますが、既存の値を保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-139">Reserved items can be ignored, but existing values must be preserved.</span></span>
    
- <span data-ttu-id="3d6cd-140">SearchFolderID</span><span class="sxs-lookup"><span data-stu-id="3d6cd-140">SearchFolderID</span></span>
    
   <span data-ttu-id="3d6cd-141">データ フィールドは、16 バイトのフィールドです。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-141">The data field is a 16-byte field.</span></span> <span data-ttu-id="3d6cd-142">値は**PR_WB_SF_TAG**と同じフォルダーにこのフィールドを設定する必要がありますアプリケーションは、永続的な検索フォルダーを作成する場合 ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) 検索フォルダーのメッセージにバイナリのプロパティです。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-142">When the application creates a persistent search folder, it must set this field on the folder to the same value as the **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) binary property on the Search Folder Message.</span></span>
    
- <span data-ttu-id="3d6cd-143">ToDoFolderVersion</span><span class="sxs-lookup"><span data-stu-id="3d6cd-143">ToDoFolderVersion</span></span>
    
   <span data-ttu-id="3d6cd-144">データ フィールドは、4 バイト フィールドです。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-144">The data field is a 4-byte field.</span></span> <span data-ttu-id="3d6cd-145">アプリケーションは、[to do] 検索フォルダーを作成するには、リトル エンディアンの整数値に"0x000c0000"のフォルダーにこのフィールドの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-145">When the application creates the to-do search folder, it must set the value of this field on the folder to the little-endian integer value of" 0x000c0000":</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="3d6cd-146">関連リソース</span><span class="sxs-lookup"><span data-stu-id="3d6cd-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3d6cd-147">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="3d6cd-147">Protocol specifications</span></span>

<span data-ttu-id="3d6cd-148">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d6cd-148">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d6cd-149">関連する Exchange Server プロトコルの仕様への参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3d6cd-150">[[MS OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d6cd-150">[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d6cd-151">場所と共有カテゴリのリストおよび作業時間など、クライアントとサーバーの構成データのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-151">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="3d6cd-152">[[MS OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d6cd-152">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3d6cd-153">プロパティや検索フォルダーの一覧の構成を操作するための動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-153">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3d6cd-154">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="3d6cd-154">Header files</span></span>

<span data-ttu-id="3d6cd-155">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3d6cd-155">Mapidefs.h</span></span>
  
> <span data-ttu-id="3d6cd-156">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-156">Provides data type definitions.</span></span>
    
<span data-ttu-id="3d6cd-157">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3d6cd-157">Mapitags.h</span></span>
  
> <span data-ttu-id="3d6cd-158">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-158">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d6cd-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d6cd-159">See also</span></span>

- [<span data-ttu-id="3d6cd-160">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d6cd-160">MAPI Properties</span></span>](mapi-properties.md)
- [<span data-ttu-id="3d6cd-161">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="3d6cd-161">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="3d6cd-162">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="3d6cd-162">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="3d6cd-163">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="3d6cd-163">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

