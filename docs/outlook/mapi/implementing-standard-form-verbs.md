---
title: 標準のフォーム動詞の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 46585859e1dde4ecf38262f99cac5e3a9d29e5db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568750"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="c6181-103">標準のフォーム動詞の実装</span><span class="sxs-lookup"><span data-stu-id="c6181-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="c6181-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6181-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6181-105">MAPI では、標準的な動詞、またはユーザーがメニュー アイテムを選択、またはフォームのすべてのビューアーをサポートする必要がありますボタンをクリックしたときに実行されたアクションのセットを定義します。</span><span class="sxs-lookup"><span data-stu-id="c6181-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="c6181-106">各動詞には、EXCHFORM で定義されている、識別用に、それに関連する定数です。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="c6181-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="c6181-107">次の表は、フォームの標準動詞と、関連付けられている定数の一覧。</span><span class="sxs-lookup"><span data-stu-id="c6181-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="c6181-108">**動詞**</span><span class="sxs-lookup"><span data-stu-id="c6181-108">**Verb**</span></span>|<span data-ttu-id="c6181-109">**値**</span><span class="sxs-lookup"><span data-stu-id="c6181-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c6181-110">Open</span><span class="sxs-lookup"><span data-stu-id="c6181-110">Open</span></span>  <br/> |<span data-ttu-id="c6181-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="c6181-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="c6181-112">Reply</span><span class="sxs-lookup"><span data-stu-id="c6181-112">Reply</span></span>  <br/> |<span data-ttu-id="c6181-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="c6181-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="c6181-114">全員へ返信</span><span class="sxs-lookup"><span data-stu-id="c6181-114">Reply to All</span></span>  <br/> |<span data-ttu-id="c6181-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="c6181-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="c6181-116">Forward</span><span class="sxs-lookup"><span data-stu-id="c6181-116">Forward</span></span>  <br/> |<span data-ttu-id="c6181-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="c6181-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="c6181-118">印刷</span><span class="sxs-lookup"><span data-stu-id="c6181-118">Print</span></span>  <br/> |<span data-ttu-id="c6181-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="c6181-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="c6181-120">としてを保存します。</span><span class="sxs-lookup"><span data-stu-id="c6181-120">Save As</span></span>  <br/> |<span data-ttu-id="c6181-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="c6181-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="c6181-122">フォルダーへ投稿</span><span class="sxs-lookup"><span data-stu-id="c6181-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="c6181-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="c6181-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="c6181-124">ユーザーが動詞を選択したときに対応するアクションを実行するのには、フォームの[IMAPIForm::DoVerb](imapiform-doverb.md)メソッドの呼び出しでその定数を渡します。</span><span class="sxs-lookup"><span data-stu-id="c6181-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="c6181-125">動詞にアクセスする、フォームのビューアーで、ほか、ユーザーはフォームから直接動詞をもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c6181-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="c6181-126">などのいくつかのフォーム オブジェクトを許可すると、ユーザーがフォーム上を右クリックし、コンテキスト メニューから**印刷**を選択する**印刷**の動詞を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c6181-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

