---
title: IMAPISync IUnknown
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fb7a8ea39d6e7b1d7df1560658ceb67a79d39d92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800807"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="50243-103">IMAPISync: IUnknown</span><span class="sxs-lookup"><span data-stu-id="50243-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="50243-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="50243-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="50243-105">トランスポート API を使用する代わりに e メールを同期するためのメカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="50243-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="50243-106">ストア オブジェクトには、このインターフェイスは公開されています。</span><span class="sxs-lookup"><span data-stu-id="50243-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="50243-107">このインターフェイスを使用して、 [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)トランスポート プロバイダーより良い進行状況を提供できるし、エラー メッセージよりも、Microsoft Outlook で [送受信] ダイアログ ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="50243-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="50243-108">[送信トレイ] は、既定のストアにまだが。</span><span class="sxs-lookup"><span data-stu-id="50243-108">The outbox is still in the default store.</span></span> <span data-ttu-id="50243-109">トランスポート Api を使用して送信するメッセージは、外部ストアにすることはできませんので、メールを送信するのには、outlook が続行されます。</span><span class="sxs-lookup"><span data-stu-id="50243-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="50243-110">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="50243-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="50243-111">ストアおよびトランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="50243-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="50243-112">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="50243-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="50243-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="50243-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="50243-114">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50243-114">Called by:</span></span>  <br/> |<span data-ttu-id="50243-115">ストアおよびトランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="50243-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="50243-116">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="50243-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="50243-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="50243-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="50243-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="50243-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="50243-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="50243-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="50243-120">メッセージ ストア プロバイダーによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="50243-120">Implemented by message store providers.</span></span> <span data-ttu-id="50243-121">このメソッドは同期を開始するには、Outlook 2010、Outlook 2013 で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="50243-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50243-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="50243-122">See also</span></span>



[<span data-ttu-id="50243-123">IMAPISyncProgressCallback: IUnknown</span><span class="sxs-lookup"><span data-stu-id="50243-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="50243-124">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="50243-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

