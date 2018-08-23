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
ms.openlocfilehash: 5165867e46d3d86d65932e7ae432b446efbd8fff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589127"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="4d746-103">PidTagServiceSupportFiles 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="4d746-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="4d746-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d746-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d746-105">メッセージ サービスに属しているファイルの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4d746-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4d746-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="4d746-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4d746-107">PR_SERVICE_SUPPORT_FILES、PR_SERVICE_SUPPORT_FILES_A、PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="4d746-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="4d746-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="4d746-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4d746-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="4d746-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="4d746-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="4d746-110">Data type:</span></span>  <br/> |<span data-ttu-id="4d746-111">PT_MV_STRING8、PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4d746-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4d746-112">領域:</span><span class="sxs-lookup"><span data-stu-id="4d746-112">Area:</span></span>  <br/> |<span data-ttu-id="4d746-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="4d746-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d746-114">注釈</span><span class="sxs-lookup"><span data-stu-id="4d746-114">Remarks</span></span>

<span data-ttu-id="4d746-115">[コントロール パネル] ダイアログ ボックスを使用すると、ユーザーはメッセージ サービスに属しているファイルの一覧を取得できます。</span><span class="sxs-lookup"><span data-stu-id="4d746-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="4d746-116">たとえば、ユーザーはサービスに属しているすべてのダイナミック リンク ライブラリ (Dll) の名前を取得できます。</span><span class="sxs-lookup"><span data-stu-id="4d746-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="4d746-117">ユーザーは、名前とすべての Dll のバージョン番号など、指定したファイルに関する追加情報をシークし、できます。</span><span class="sxs-lookup"><span data-stu-id="4d746-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="4d746-118">MAPI を使用して、これらのメッセージング ユーザーの選択ダイアログ ボックスにサポート ファイルの一覧を作成するプロパティです。</span><span class="sxs-lookup"><span data-stu-id="4d746-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="4d746-119">MAPI は、ファイル名でのみ動作し、Active Directory サービス インターフェイス (ANSI) 文字セットで、その他の文字列が渡されます。</span><span class="sxs-lookup"><span data-stu-id="4d746-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="4d746-120">正規機器製造元 (OEM) 文字セットでファイル名を使用するクライアント アプリケーションする必要があります ANSI に変換する、MAPI を呼び出す前にします。</span><span class="sxs-lookup"><span data-stu-id="4d746-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4d746-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="4d746-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4d746-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="4d746-122">Header files</span></span>

<span data-ttu-id="4d746-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4d746-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="4d746-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="4d746-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="4d746-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4d746-125">Mapitags.h</span></span>
  
> <span data-ttu-id="4d746-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4d746-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4d746-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="4d746-127">See also</span></span>



[<span data-ttu-id="4d746-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4d746-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4d746-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="4d746-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4d746-130">標準プロパティ名から MAPI 名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4d746-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4d746-131">MAPI 名から標準プロパティ名へのマッピング</span><span class="sxs-lookup"><span data-stu-id="4d746-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

