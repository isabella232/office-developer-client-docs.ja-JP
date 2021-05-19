---
title: IPSTOVERRIDEREQ IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7f3f6ae2b9849710bf44d3635fc7bb9a62016f48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356981"
---
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="e5d23-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5d23-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="e5d23-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5d23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5d23-105">個人用フォルダー ファイル (PST) ストア プロバイダーのリソースにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="e5d23-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e5d23-106">継承元:</span><span class="sxs-lookup"><span data-stu-id="e5d23-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="e5d23-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5d23-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="e5d23-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="e5d23-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e5d23-109">PST ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e5d23-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="e5d23-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e5d23-110">Called by:</span></span>  <br/> |<span data-ttu-id="e5d23-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="e5d23-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="e5d23-112">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="e5d23-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e5d23-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="e5d23-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e5d23-114">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="e5d23-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e5d23-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="e5d23-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="e5d23-116">個人用フォルダー (.pst) ファイルのロック解除手順を開始します。</span><span class="sxs-lookup"><span data-stu-id="e5d23-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5d23-117">注釈</span><span class="sxs-lookup"><span data-stu-id="e5d23-117">Remarks</span></span>

<span data-ttu-id="e5d23-118">PST オーバーライド ハンドラー インターフェイス識別子は、現在使用しているダウンロード可能なヘッダー ファイルで定義されていない可能性があります。その場合は [、MAPI 定数](mapi-constants.md) のトピックで見つけ、それらをコピーしてコードに追加できます。</span><span class="sxs-lookup"><span data-stu-id="e5d23-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="e5d23-119">Microsoft Windows ソフトウェア開発キット (SDK) ヘッダー ファイル guiddef.h で定義されている DEFINE_GUID マクロを使用して、グローバル一意識別子 (GUID) 記号名をその値に関連付ける。</span><span class="sxs-lookup"><span data-stu-id="e5d23-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="e5d23-120">詳細については、「PST オーバーライド[ハンドラーを実装して、2007 年の PSTDisableGrow](https://support.microsoft.com/kb/956070)ポリシーをバイパスするOutlook参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5d23-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e5d23-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="e5d23-121">See also</span></span>



[<span data-ttu-id="e5d23-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e5d23-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

