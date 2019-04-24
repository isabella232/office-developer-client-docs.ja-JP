---
title: PidTagServiceSupportFiles 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceSupportFiles
api_type:
- COM
ms.assetid: df4be986-62a8-49d6-8eca-25b55c74f830
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3753177552d45e32e53ae192a9dfae15b601afcc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359473"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="53199-103">PidTagServiceSupportFiles 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="53199-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="53199-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53199-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53199-105">メッセージサービスに属するファイルの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="53199-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53199-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="53199-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53199-107">PR_SERVICE_SUPPORT_FILES、PR_SERVICE_SUPPORT_FILES_A、PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="53199-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="53199-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="53199-108">Identifier:</span></span>  <br/> |<span data-ttu-id="53199-109">0x3d0f</span><span class="sxs-lookup"><span data-stu-id="53199-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="53199-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="53199-110">Data type:</span></span>  <br/> |<span data-ttu-id="53199-111">PT_MV_STRING8、PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="53199-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="53199-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="53199-112">Area:</span></span>  <br/> |<span data-ttu-id="53199-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="53199-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53199-114">解説</span><span class="sxs-lookup"><span data-stu-id="53199-114">Remarks</span></span>

<span data-ttu-id="53199-115">コントロールパネルアプレットのダイアログボックスを使用して、ユーザーはメッセージサービスに属するファイルの一覧を取得できます。</span><span class="sxs-lookup"><span data-stu-id="53199-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="53199-116">たとえば、ユーザーは、サービスに属しているすべてのダイナミックリンクライブラリ (dll) の名前を取得できます。</span><span class="sxs-lookup"><span data-stu-id="53199-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="53199-117">ユーザーは、指定されたファイル (すべての dll の名前とバージョン番号など) に関する追加の詳細を検索できます。</span><span class="sxs-lookup"><span data-stu-id="53199-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="53199-118">MAPI では、これらのプロパティを使用して、メッセージングユーザーの選択に対応するダイアログボックスにサポートファイルリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="53199-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="53199-119">MAPI は、Active Directory サービスインターフェイス (ANSI) 文字セットでファイル名とその他の文字列が渡された場合にのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="53199-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="53199-120">OEM (相手先ブランド供給) 文字セットでファイル名を使用するクライアントアプリケーションは、MAPI を呼び出す前に、それらを ANSI に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53199-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="53199-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="53199-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="53199-122">ヘッダーファイル</span><span class="sxs-lookup"><span data-stu-id="53199-122">Header files</span></span>

<span data-ttu-id="53199-123">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53199-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="53199-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="53199-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="53199-125">Mapitags</span><span class="sxs-lookup"><span data-stu-id="53199-125">Mapitags.h</span></span>
  
> <span data-ttu-id="53199-126">代替名としてリストされているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="53199-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53199-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="53199-127">See also</span></span>



[<span data-ttu-id="53199-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="53199-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53199-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="53199-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53199-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="53199-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53199-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="53199-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

