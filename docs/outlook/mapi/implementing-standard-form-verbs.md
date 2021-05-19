---
title: 標準フォーム動詞の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426122"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="455c6-103">標準フォーム動詞の実装</span><span class="sxs-lookup"><span data-stu-id="455c6-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="455c6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="455c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="455c6-105">MAPI は、すべてのフォーム ビューアーがサポートする必要がある一連の標準動詞、またはユーザーがメニュー選択を行った場合、またはボタンをクリックするときに実行されるアクションを定義します。</span><span class="sxs-lookup"><span data-stu-id="455c6-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="455c6-106">各動詞には、EXCHFORM で定義された識別用に関連付けられた定数があります。H ヘッダー ファイル。</span><span class="sxs-lookup"><span data-stu-id="455c6-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="455c6-107">次の表に、標準フォーム動詞とその関連する定数を示します。</span><span class="sxs-lookup"><span data-stu-id="455c6-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="455c6-108">**Verb**</span><span class="sxs-lookup"><span data-stu-id="455c6-108">**Verb**</span></span>|<span data-ttu-id="455c6-109">**値**</span><span class="sxs-lookup"><span data-stu-id="455c6-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="455c6-110">開く</span><span class="sxs-lookup"><span data-stu-id="455c6-110">Open</span></span>  <br/> |<span data-ttu-id="455c6-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="455c6-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="455c6-112">返信</span><span class="sxs-lookup"><span data-stu-id="455c6-112">Reply</span></span>  <br/> |<span data-ttu-id="455c6-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="455c6-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="455c6-114">全員へ返信</span><span class="sxs-lookup"><span data-stu-id="455c6-114">Reply to All</span></span>  <br/> |<span data-ttu-id="455c6-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="455c6-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="455c6-116">転送</span><span class="sxs-lookup"><span data-stu-id="455c6-116">Forward</span></span>  <br/> |<span data-ttu-id="455c6-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="455c6-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="455c6-118">印刷</span><span class="sxs-lookup"><span data-stu-id="455c6-118">Print</span></span>  <br/> |<span data-ttu-id="455c6-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="455c6-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="455c6-120">名前を付けて保存</span><span class="sxs-lookup"><span data-stu-id="455c6-120">Save As</span></span>  <br/> |<span data-ttu-id="455c6-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="455c6-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="455c6-122">フォルダーへ投稿</span><span class="sxs-lookup"><span data-stu-id="455c6-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="455c6-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="455c6-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="455c6-124">ユーザーが動詞を選択すると、その定数をフォームの [IMAPIForm::D oVerb](imapiform-doverb.md) メソッドに渡して、対応するアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="455c6-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="455c6-125">フォーム ビューアーを介して動詞にアクセスする以外に、ユーザーはフォームから直接動詞にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="455c6-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="455c6-126">たとえば、一部のフォーム オブジェクトでは、フォームを右クリックし、コンテキストに依存するメニューから [印刷] を選択することで、ユーザーが **Print** 動詞を呼び出す場合があります。</span><span class="sxs-lookup"><span data-stu-id="455c6-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

