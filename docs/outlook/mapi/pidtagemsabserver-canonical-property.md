---
title: PidTagEmsAbServer の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 27e3a9687d66bd1cd3586a25a3ca5792523096c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802714"
---
# <a name="pidtagemsabserver-canonical-property"></a><span data-ttu-id="a14ae-103">PidTagEmsAbServer の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="a14ae-103">PidTagEmsAbServer Canonical Property</span></span>

  
  
<span data-ttu-id="a14ae-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a14ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a14ae-105">オフラインのシナリオ、またはオンラインのシナリオでは、アドレス帳コンテナーが存在するグローバル カタログ サーバーの完全修飾ドメイン名で、アドレス帳コンテナーのいずれかのパスを指定します。</span><span class="sxs-lookup"><span data-stu-id="a14ae-105">Specifies either the path of an address book container in an offline scenario or the fully qualified domain name of the global catalog server where the address book container resides in an online scenario.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="a14ae-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="a14ae-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a14ae-107">PR_EMS_AB_SERVER、PR_EMS_AB_SERVER_A、PR_EMS_AB_SERVER_W</span><span class="sxs-lookup"><span data-stu-id="a14ae-107">PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W</span></span>  <br/> |
|<span data-ttu-id="a14ae-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="a14ae-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a14ae-109">0 xfffe</span><span class="sxs-lookup"><span data-stu-id="a14ae-109">0xFFFE</span></span>  <br/> |
|<span data-ttu-id="a14ae-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="a14ae-110">Data type:</span></span>  <br/> |<span data-ttu-id="a14ae-111">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="a14ae-111">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="a14ae-112">領域:</span><span class="sxs-lookup"><span data-stu-id="a14ae-112">Area:</span></span>  <br/> |<span data-ttu-id="a14ae-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="a14ae-113">Address Book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a14ae-114">備考</span><span class="sxs-lookup"><span data-stu-id="a14ae-114">Remarks</span></span>

<span data-ttu-id="a14ae-115">このプロパティは、プロパティの型がコンパイル時に**PT_UNICODE**にリセット、`UNICODE`プラットフォームでは、Unicode、および**PT_STRING8**がコンパイルできないときに、シンボル、`UNICODE`の記号です。</span><span class="sxs-lookup"><span data-stu-id="a14ae-115">This property has the property type reset to **PT_UNICODE** when it is compiled with the  `UNICODE` symbol on a Unicode platform, and to **PT_STRING8** when it is not compiled with the  `UNICODE` symbol.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a14ae-116">関連リソース</span><span class="sxs-lookup"><span data-stu-id="a14ae-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a14ae-117">プロトコルの仕様</span><span class="sxs-lookup"><span data-stu-id="a14ae-117">Protocol specifications</span></span>

<span data-ttu-id="a14ae-118">[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a14ae-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a14ae-119">プロパティ セットの定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a14ae-119">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a14ae-120">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="a14ae-120">Header files</span></span>

<span data-ttu-id="a14ae-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a14ae-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="a14ae-122">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="a14ae-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="a14ae-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a14ae-123">Mapitags.h</span></span>
  
> <span data-ttu-id="a14ae-124">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a14ae-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a14ae-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a14ae-125">See also</span></span>



[<span data-ttu-id="a14ae-126">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a14ae-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a14ae-127">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="a14ae-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a14ae-128">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="a14ae-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a14ae-129">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="a14ae-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

