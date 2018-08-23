---
title: PidTagServiceDeleteFiles 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 236349a6b53eeb2f5c18c841c05cfb80a3fce824
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580223"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a><span data-ttu-id="1d3f7-103">PidTagServiceDeleteFiles 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1d3f7-103">PidTagServiceDeleteFiles Canonical Property</span></span>

  
  
<span data-ttu-id="1d3f7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d3f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d3f7-105">メッセージ サービスのアンインストール時に削除するファイル名の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1d3f7-105">Contains a list of filenames that are to be deleted when the message service is uninstalled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1d3f7-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="1d3f7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1d3f7-107">PR_SERVICE_DELETE_FILES、PR_SERVICE_DELETE_FILES_A、PR_SERVICE_DELETE_FILES_W</span><span class="sxs-lookup"><span data-stu-id="1d3f7-107">PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A, PR_SERVICE_DELETE_FILES_W</span></span>  <br/> |
|<span data-ttu-id="1d3f7-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="1d3f7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1d3f7-109">0x3D10</span><span class="sxs-lookup"><span data-stu-id="1d3f7-109">0x3D10</span></span>  <br/> |
|<span data-ttu-id="1d3f7-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="1d3f7-110">Data type:</span></span>  <br/> |<span data-ttu-id="1d3f7-111">PT_MV_STRING8、PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1d3f7-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1d3f7-112">領域:</span><span class="sxs-lookup"><span data-stu-id="1d3f7-112">Area:</span></span>  <br/> |<span data-ttu-id="1d3f7-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="1d3f7-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d3f7-114">注釈</span><span class="sxs-lookup"><span data-stu-id="1d3f7-114">Remarks</span></span>

<span data-ttu-id="1d3f7-115">メッセージ サービスをアンインストールするのには、コントロール パネルを使用する場合、これらのプロパティに含まれているボックスの一覧でファイル名がコンピューターから削除されます。</span><span class="sxs-lookup"><span data-stu-id="1d3f7-115">The filenames in the list contained in these properties are deleted from the computer when using the control panel to uninstall the message service.</span></span> <span data-ttu-id="1d3f7-116">含めないでください、ボックスの一覧で複数のメッセージ サービスをサポートする任意の DLL または追加のメッセージ サービスを誤って削除された可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1d3f7-116">Do not include in the list any DLL that supports multiple message services, or additional message services could be inadvertently removed.</span></span>
  
<span data-ttu-id="1d3f7-117">MAPI は、ファイル名でのみ動作し、ANSI 文字セットで、その他の文字列が渡されます。</span><span class="sxs-lookup"><span data-stu-id="1d3f7-117">MAPI works only with filenames, and other strings passed to it, in the ANSI character set.</span></span> <span data-ttu-id="1d3f7-118">OEM 文字セットでファイル名を使用するアプリケーションする必要があります ANSI に変換する、MAPI を呼び出す前にします。</span><span class="sxs-lookup"><span data-stu-id="1d3f7-118">Applications that use filenames in an OEM character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1d3f7-119">関連リソース</span><span class="sxs-lookup"><span data-stu-id="1d3f7-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1d3f7-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="1d3f7-120">Header files</span></span>

<span data-ttu-id="1d3f7-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1d3f7-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="1d3f7-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="1d3f7-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="1d3f7-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1d3f7-123">Mapitags.h</span></span>
  
> <span data-ttu-id="1d3f7-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1d3f7-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d3f7-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="1d3f7-125">See also</span></span>



[<span data-ttu-id="1d3f7-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1d3f7-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1d3f7-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="1d3f7-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1d3f7-128">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1d3f7-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1d3f7-129">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="1d3f7-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

