---
title: imapisync IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405593"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="78c31-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="78c31-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="78c31-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78c31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78c31-105">トランスポート API を使用する代わりに、電子メールを同期するためのメカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="78c31-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="78c31-106">このインターフェイスは、store オブジェクトに公開されます。</span><span class="sxs-lookup"><span data-stu-id="78c31-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="78c31-107">このインターフェイスと[IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)を使用することにより、トランスポートプロバイダーは、Microsoft Outlook の送受信ダイアログに表示されるのとは異なる進行状況およびエラーメッセージを提供できます。</span><span class="sxs-lookup"><span data-stu-id="78c31-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="78c31-108">送信トレイはまだ既定のストアにあります。</span><span class="sxs-lookup"><span data-stu-id="78c31-108">The outbox is still in the default store.</span></span> <span data-ttu-id="78c31-109">送信メッセージが外部ストアに存在できないため、Outlook は引き続きトランスポート api を使用してメールを送信します。</span><span class="sxs-lookup"><span data-stu-id="78c31-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78c31-110">公開者:</span><span class="sxs-lookup"><span data-stu-id="78c31-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="78c31-111">ストアとトランスポートプロバイダー</span><span class="sxs-lookup"><span data-stu-id="78c31-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="78c31-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="78c31-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="78c31-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="78c31-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="78c31-114">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="78c31-114">Called by:</span></span>  <br/> |<span data-ttu-id="78c31-115">ストアとトランスポートプロバイダー</span><span class="sxs-lookup"><span data-stu-id="78c31-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="78c31-116">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="78c31-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="78c31-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="78c31-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="78c31-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="78c31-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="78c31-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="78c31-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="78c31-120">メッセージストアプロバイダーによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="78c31-120">Implemented by message store providers.</span></span> <span data-ttu-id="78c31-121">このメソッドは、outlook 2010 および outlook 2013 によって呼び出され、同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="78c31-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78c31-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="78c31-122">See also</span></span>



[<span data-ttu-id="78c31-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="78c31-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="78c31-124">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="78c31-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

