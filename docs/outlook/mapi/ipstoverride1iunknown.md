---
title: IPSTOVERRIDE1 IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1
api_type:
- COM
ms.assetid: d26cee81-45ea-4fd3-8a54-5f35264b5d6a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: db2853080b1fc2ff3a346dcfb8d112237b7f3459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801190"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="a0dbb-103">IPSTOVERRIDE1: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0dbb-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="a0dbb-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0dbb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0dbb-105">PSTDisableGrow ポリシーを無効にするには個人用フォルダー ファイル (PST) のストア プロバイダーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a0dbb-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0dbb-106">継承します。</span><span class="sxs-lookup"><span data-stu-id="a0dbb-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="a0dbb-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0dbb-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="a0dbb-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="a0dbb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a0dbb-109">PST ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a0dbb-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="a0dbb-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a0dbb-110">Called by:</span></span>  <br/> |<span data-ttu-id="a0dbb-111">クライアント</span><span class="sxs-lookup"><span data-stu-id="a0dbb-111">Client</span></span>  <br/> |
|<span data-ttu-id="a0dbb-112">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="a0dbb-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a0dbb-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="a0dbb-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a0dbb-114">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="a0dbb-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a0dbb-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="a0dbb-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="a0dbb-116">個人用フォルダー (.pst) ファイルの登録の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="a0dbb-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="a0dbb-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="a0dbb-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="a0dbb-118">HrTrustedPSTOverrideHandlerCallback それ以降の呼び出しを回避する自動ロック解除では、個人用フォルダー ファイルを登録します。</span><span class="sxs-lookup"><span data-stu-id="a0dbb-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="a0dbb-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="a0dbb-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="a0dbb-120">成長のための個人用フォルダー ファイルのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="a0dbb-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0dbb-121">備考</span><span class="sxs-lookup"><span data-stu-id="a0dbb-121">Remarks</span></span>

<span data-ttu-id="a0dbb-122">PST をオーバーライドするハンドラーのインターフェイス識別子は可能性があります現在がある場合は、 [MAPI の定数](mapi-constants.md)のトピックで検索してコピーし、コードに追加のダウンロード可能なヘッダー ファイルで定義されていません。</span><span class="sxs-lookup"><span data-stu-id="a0dbb-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="a0dbb-123">値はシンボル名のグローバル一意識別子 (GUID) を関連付けるには、Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル guiddef.h に定義されている DEFINE_GUID マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="a0dbb-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="a0dbb-124">詳細については、 [Outlook 2007 で PSTDisableGrow ポリシーをバイパスするのには、PST オーバーライドするハンドラーを実装する方法](http://support.microsoft.com/kb/956070)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a0dbb-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a0dbb-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0dbb-125">See also</span></span>



[<span data-ttu-id="a0dbb-126">IPSTOVERRIDEREQ: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0dbb-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

