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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315499"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="11762-103">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11762-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="11762-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11762-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11762-105">個人用フォルダー ファイル (PST) ストア プロバイダーが PSTDisableGrow ポリシーを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="11762-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11762-106">継承元:</span><span class="sxs-lookup"><span data-stu-id="11762-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="11762-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="11762-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="11762-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="11762-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="11762-109">PST ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="11762-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="11762-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="11762-110">Called by:</span></span>  <br/> |<span data-ttu-id="11762-111">クライアント</span><span class="sxs-lookup"><span data-stu-id="11762-111">Client</span></span>  <br/> |
|<span data-ttu-id="11762-112">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="11762-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="11762-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="11762-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="11762-114">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="11762-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="11762-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="11762-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="11762-116">個人用フォルダー (.pst) ファイルの登録の一覧を取得します。</span><span class="sxs-lookup"><span data-stu-id="11762-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="11762-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="11762-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="11762-118">HrTrustedPSTOverrideHandlerCallback へのそれ以上の呼び出しを回避し、自動ロック解除用に個人用フォルダー ファイルを登録します。</span><span class="sxs-lookup"><span data-stu-id="11762-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="11762-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="11762-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="11762-120">成長のために個人用フォルダー ファイルのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="11762-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11762-121">注釈</span><span class="sxs-lookup"><span data-stu-id="11762-121">Remarks</span></span>

<span data-ttu-id="11762-122">PST オーバーライド ハンドラー インターフェイス識別子は、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。その場合は [、MAPI 定数](mapi-constants.md) のトピックで見つけ、それらをコピーしてコードに追加できます。</span><span class="sxs-lookup"><span data-stu-id="11762-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="11762-123">Microsoft Windows ソフトウェア開発キット (SDK) ヘッダー ファイル guiddef.h で定義されている DEFINE_GUID マクロを使用して、グローバル一意識別子 (GUID) 記号名をその値に関連付ける。</span><span class="sxs-lookup"><span data-stu-id="11762-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="11762-124">詳細については、「PST オーバーライド[ハンドラーを実装して、2007 年の PSTDisableGrow](https://support.microsoft.com/kb/956070)ポリシーをバイパスするOutlook参照してください。</span><span class="sxs-lookup"><span data-stu-id="11762-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="11762-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="11762-125">See also</span></span>



[<span data-ttu-id="11762-126">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11762-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

