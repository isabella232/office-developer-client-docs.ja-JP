---
title: PidTagServiceSupportFiles の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2dc431d807bd74640e5b5a9c020f668b13530197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803568"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a><span data-ttu-id="23e0b-103">PidTagServiceSupportFiles の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="23e0b-103">PidTagServiceSupportFiles Canonical Property</span></span>

  
  
<span data-ttu-id="23e0b-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23e0b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23e0b-105">メッセージ サービスに属しているファイルの一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="23e0b-105">Contains a list of the files that belong to the message service.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="23e0b-106">関連するプロパティ。</span><span class="sxs-lookup"><span data-stu-id="23e0b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="23e0b-107">PR_SERVICE_SUPPORT_FILES、PR_SERVICE_SUPPORT_FILES_A、PR_SERVICE_SUPPORT_FILES_W</span><span class="sxs-lookup"><span data-stu-id="23e0b-107">PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W</span></span>  <br/> |
|<span data-ttu-id="23e0b-108">識別子:</span><span class="sxs-lookup"><span data-stu-id="23e0b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="23e0b-109">0x3D0F</span><span class="sxs-lookup"><span data-stu-id="23e0b-109">0x3D0F</span></span>  <br/> |
|<span data-ttu-id="23e0b-110">データを入力します。</span><span class="sxs-lookup"><span data-stu-id="23e0b-110">Data type:</span></span>  <br/> |<span data-ttu-id="23e0b-111">PT_MV_STRING8、PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="23e0b-111">PT_MV_STRING8, PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="23e0b-112">領域:</span><span class="sxs-lookup"><span data-stu-id="23e0b-112">Area:</span></span>  <br/> |<span data-ttu-id="23e0b-113">MAPI プロファイル</span><span class="sxs-lookup"><span data-stu-id="23e0b-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23e0b-114">備考</span><span class="sxs-lookup"><span data-stu-id="23e0b-114">Remarks</span></span>

<span data-ttu-id="23e0b-115">[コントロール パネル] ダイアログ ボックスを使用すると、ユーザーはメッセージ サービスに属しているファイルの一覧を取得できます。</span><span class="sxs-lookup"><span data-stu-id="23e0b-115">Using a dialog box in the control panel applet, a user can obtain the list of files that belong to the message service.</span></span> <span data-ttu-id="23e0b-116">たとえば、ユーザーはサービスに属しているすべてのダイナミック リンク ライブラリ (Dll) の名前を取得できます。</span><span class="sxs-lookup"><span data-stu-id="23e0b-116">For example, the user can obtain the names of all dynamic-link libraries (DLLs) that belong to the service.</span></span> <span data-ttu-id="23e0b-117">ユーザーは、名前とすべての Dll のバージョン番号など、指定したファイルに関する追加情報をシークし、できます。</span><span class="sxs-lookup"><span data-stu-id="23e0b-117">The user can then seek additional details about the specified files, such as the names and version numbers of all the DLLs.</span></span> <span data-ttu-id="23e0b-118">MAPI を使用して、これらのメッセージング ユーザーの選択ダイアログ ボックスにサポート ファイルの一覧を作成するプロパティです。</span><span class="sxs-lookup"><span data-stu-id="23e0b-118">MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.</span></span>
  
<span data-ttu-id="23e0b-119">MAPI は、ファイル名でのみ動作し、Active Directory サービス インターフェイス (ANSI) 文字セットで、その他の文字列が渡されます。</span><span class="sxs-lookup"><span data-stu-id="23e0b-119">MAPI works only with filenames, and other strings passed to it, in the Active Directory Service Interfaces (ANSI) character set.</span></span> <span data-ttu-id="23e0b-120">正規機器製造元 (OEM) 文字セットでファイル名を使用するクライアント アプリケーションする必要があります ANSI に変換する、MAPI を呼び出す前にします。</span><span class="sxs-lookup"><span data-stu-id="23e0b-120">Client applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="23e0b-121">関連リソース</span><span class="sxs-lookup"><span data-stu-id="23e0b-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="23e0b-122">ヘッダー ファイル</span><span class="sxs-lookup"><span data-stu-id="23e0b-122">Header files</span></span>

<span data-ttu-id="23e0b-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="23e0b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="23e0b-124">データ型定義を提供します。</span><span class="sxs-lookup"><span data-stu-id="23e0b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="23e0b-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="23e0b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="23e0b-126">代替名として記載されているプロパティの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="23e0b-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="23e0b-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="23e0b-127">See also</span></span>



[<span data-ttu-id="23e0b-128">MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="23e0b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="23e0b-129">標準の MAPI プロパティ</span><span class="sxs-lookup"><span data-stu-id="23e0b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="23e0b-130">MAPI 名への標準的なプロパティ名のマッピング</span><span class="sxs-lookup"><span data-stu-id="23e0b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="23e0b-131">MAPI 名前を標準のプロパティ名にマップします。</span><span class="sxs-lookup"><span data-stu-id="23e0b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

