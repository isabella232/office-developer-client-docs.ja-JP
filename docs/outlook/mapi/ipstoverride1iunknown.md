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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5208e77f3605b5ba861f68786d8fe5e91b990d32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315499"
---
# <a name="ipstoverride1--iunknown"></a><span data-ttu-id="cac0b-103">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cac0b-103">IPSTOVERRIDE1 : IUnknown</span></span>

  
  
<span data-ttu-id="cac0b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cac0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cac0b-105">個人用フォルダーファイル (PST) ストアプロバイダーが PSTDisableGrow ポリシーを上書きできるようにします。</span><span class="sxs-lookup"><span data-stu-id="cac0b-105">Allows a Personal Folders file (PST) store provider to override the PSTDisableGrow policy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cac0b-106">継承元:</span><span class="sxs-lookup"><span data-stu-id="cac0b-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="cac0b-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="cac0b-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="cac0b-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="cac0b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cac0b-109">PST ストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="cac0b-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="cac0b-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="cac0b-110">Called by:</span></span>  <br/> |<span data-ttu-id="cac0b-111">クライアント</span><span class="sxs-lookup"><span data-stu-id="cac0b-111">Client</span></span>  <br/> |
|<span data-ttu-id="cac0b-112">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="cac0b-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cac0b-113">IID_IPSTOVERRIDE1</span><span class="sxs-lookup"><span data-stu-id="cac0b-113">IID_IPSTOVERRIDE1</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cac0b-114">v の順序</span><span class="sxs-lookup"><span data-stu-id="cac0b-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cac0b-115">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="cac0b-115">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>](ipstoverride1-getpersistedregistrations.md) <br/> |<span data-ttu-id="cac0b-116">個人用フォルダー (.pst) ファイルの登録リストを取得します。</span><span class="sxs-lookup"><span data-stu-id="cac0b-116">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>  <br/> |
|[<span data-ttu-id="cac0b-117">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="cac0b-117">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>](ipstoverride1-setpersistedregistrations.md) <br/> |<span data-ttu-id="cac0b-118">自動的にロックを解除する個人用フォルダーファイルを登録して、HrTrustedPSTOverrideHandlerCallback へのその他の呼び出しを回避します。</span><span class="sxs-lookup"><span data-stu-id="cac0b-118">Registers Personal Folders files for automatic unlocking, avoiding further calls to HrTrustedPSTOverrideHandlerCallback.</span></span>  <br/> |
|[<span data-ttu-id="cac0b-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span><span class="sxs-lookup"><span data-stu-id="cac0b-119">IPSTOVERRIDE1::OverridePSTDisableGrow</span></span>](ipstoverride1-overridepstdisablegrow.md) <br/> |<span data-ttu-id="cac0b-120">拡張のために個人用フォルダーファイルのロックを解除します。</span><span class="sxs-lookup"><span data-stu-id="cac0b-120">Unlocks a Personal Folders file for growth.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cac0b-121">解説</span><span class="sxs-lookup"><span data-stu-id="cac0b-121">Remarks</span></span>

<span data-ttu-id="cac0b-122">現在使用しているダウンロード可能なヘッダーファイルでは、PST オーバーライドハンドラインターフェイス識別子が定義されていない場合があります。その場合は、 [MAPI の定数](mapi-constants.md)のトピックに記載されているので、それをコピーしてコードに追加できます。</span><span class="sxs-lookup"><span data-stu-id="cac0b-122">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="cac0b-123">Microsoft Windows Software Development Kit (SDK) ヘッダーファイル guiddef で定義されている DEFINE_GUID マクロを使用して、グローバル一意識別子 (GUID) シンボリック名を値に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="cac0b-123">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="cac0b-124">詳細については、「 [Outlook 2007 で PSTDisableGrow ポリシーをバイパスするように PST オーバーライドハンドラーを実装する方法](https://support.microsoft.com/kb/956070)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cac0b-124">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cac0b-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="cac0b-125">See also</span></span>



[<span data-ttu-id="cac0b-126">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cac0b-126">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

