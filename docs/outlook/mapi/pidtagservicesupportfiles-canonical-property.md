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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3753177552d45e32e53ae192a9dfae15b601afcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417043"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="d8857-103">PidTagServiceSupportFiles 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d8857-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="d8857-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8857-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8857-105">メッセージ サービスに属するファイルの一覧を格納します。</span><span class="sxs-lookup"><span data-stu-id="d8857-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8857-106">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="d8857-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d8857-107">PR_SERVICE_SUPPORT_FILES、PR_SERVICE_SUPPORT_FILES_A、PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="d8857-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="d8857-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="d8857-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d8857-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="d8857-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="d8857-110">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="d8857-110">Data type:</span></span>  <br/> |<span data-ttu-id="d8857-111">PT_MV_STRING8、PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d8857-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d8857-112">エリア:</span><span class="sxs-lookup"><span data-stu-id="d8857-112">Area:</span></span>  <br/> |<span data-ttu-id="d8857-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="d8857-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8857-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d8857-114">Remarks</span></span>

<span data-ttu-id="d8857-115">コントロール パネルアプレットのダイアログ ボックスを使用して、ユーザーはメッセージ サービスに属するファイルの一覧を取得できます。</span><span class="sxs-lookup"><span data-stu-id="d8857-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="d8857-116">たとえば、ユーザーは、サービスに属しているすべてのダイナミック リンク ライブラリ (DLL) の名前を取得できます。</span><span class="sxs-lookup"><span data-stu-id="d8857-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="d8857-117">その後、指定したファイルに関する詳細情報 (すべての DLL の名前やバージョン番号など) を検索できます。</span><span class="sxs-lookup"><span data-stu-id="d8857-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="d8857-118">MAPI では、これらのプロパティを使用して、メッセージング ユーザーの選択用のダイアログ ボックスにサポート ファイルの一覧を作成します。</span><span class="sxs-lookup"><span data-stu-id="d8857-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="d8857-119">MAPI は、Active Directory Service Interfaces (ANSI) 文字セット内のファイル名と、そのファイルに渡される他の文字列でのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="d8857-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="d8857-120">元の機器メーカー (OEM) の文字セットでファイル名を使用するクライアント アプリケーションは、MAPI を呼び出す前に ANSI に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8857-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d8857-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="d8857-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d8857-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="d8857-122">Header files</span></span>

<span data-ttu-id="d8857-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d8857-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d8857-124">データ型の定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="d8857-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d8857-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d8857-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d8857-126">代替名として一覧表示されるプロパティの定義が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d8857-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8857-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="d8857-127">See also</span></span>



[<span data-ttu-id="d8857-128">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="d8857-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d8857-129">MAPI 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d8857-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d8857-130">標準プロパティ名を MAPI 名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d8857-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d8857-131">MAPI 名を標準プロパティ名にマッピングする</span><span class="sxs-lookup"><span data-stu-id="d8857-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

