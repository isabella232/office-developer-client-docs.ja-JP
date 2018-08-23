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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6ee4524d08e334df858c2f035f1b21bd2b0a1c8b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801183"
---
# <a name="ipstoverridereq--iunknown"></a><span data-ttu-id="e93e5-103">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e93e5-103">IPSTOVERRIDEREQ : IUnknown</span></span>

  
  
<span data-ttu-id="e93e5-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e93e5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e93e5-105">プロバイダーを格納する個人用フォルダー ファイル (PST) のリソースをアクセスします。</span><span class="sxs-lookup"><span data-stu-id="e93e5-105">Accesses resources of a Personal Folders file (PST) store provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e93e5-106">継承します。</span><span class="sxs-lookup"><span data-stu-id="e93e5-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="e93e5-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="e93e5-107">IUnknown</span></span>  <br/> |
|<span data-ttu-id="e93e5-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="e93e5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e93e5-109">PST ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e93e5-109">PST store provider</span></span>  <br/> |
|<span data-ttu-id="e93e5-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="e93e5-110">Called by:</span></span>  <br/> |<span data-ttu-id="e93e5-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="e93e5-111">Client applications</span></span>  <br/> |
|<span data-ttu-id="e93e5-112">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="e93e5-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e93e5-113">IID_IPSTOVERRIDEREQ</span><span class="sxs-lookup"><span data-stu-id="e93e5-113">IID_IPSTOVERRIDEREQ</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e93e5-114">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="e93e5-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e93e5-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="e93e5-115">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |<span data-ttu-id="e93e5-116">個人用フォルダー (.pst) ファイルのロックを解除する手順を開始します。</span><span class="sxs-lookup"><span data-stu-id="e93e5-116">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e93e5-117">注釈</span><span class="sxs-lookup"><span data-stu-id="e93e5-117">Remarks</span></span>

<span data-ttu-id="e93e5-118">PST をオーバーライドするハンドラーのインターフェイス識別子は可能性があります現在がある場合は、 [MAPI の定数](mapi-constants.md)のトピックで検索してコピーし、コードに追加のダウンロード可能なヘッダー ファイルで定義されていません。</span><span class="sxs-lookup"><span data-stu-id="e93e5-118">The PST Override Handler Interface Identifiers might not be defined in the downloadable header file you currently have, in which case you will find them in the [MAPI Constants](mapi-constants.md) topic, and can copy and add them to your code.</span></span> <span data-ttu-id="e93e5-119">値はシンボル名のグローバル一意識別子 (GUID) を関連付けるには、Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル guiddef.h に定義されている DEFINE_GUID マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="e93e5-119">Use the DEFINE_GUID macro defined in the Microsoft Windows Software Development Kit (SDK) header file guiddef.h to associate globally unique identifier (GUID) symbolic names with their values.</span></span> 
  
<span data-ttu-id="e93e5-120">詳細については、 [Outlook 2007 で PSTDisableGrow ポリシーをバイパスするのには、PST オーバーライドするハンドラーを実装する方法](http://support.microsoft.com/kb/956070)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e93e5-120">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e93e5-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="e93e5-121">See also</span></span>



[<span data-ttu-id="e93e5-122">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e93e5-122">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)

