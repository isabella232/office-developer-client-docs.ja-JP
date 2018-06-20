---
title: フォームの標準的な動詞を実装します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8135af7947f30ac600b8d9af364b2a79a3443ab6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800954"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="13fca-103">フォームの標準的な動詞を実装します。</span><span class="sxs-lookup"><span data-stu-id="13fca-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="13fca-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13fca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13fca-105">MAPI では、標準的な動詞、またはユーザーがメニュー アイテムを選択、またはフォームのすべてのビューアーをサポートする必要がありますボタンをクリックしたときに実行されたアクションのセットを定義します。</span><span class="sxs-lookup"><span data-stu-id="13fca-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="13fca-106">各動詞には、EXCHFORM で定義されている、識別用に、それに関連する定数です。H ヘッダー ファイルです。</span><span class="sxs-lookup"><span data-stu-id="13fca-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="13fca-107">次の表は、フォームの標準動詞と、関連付けられている定数の一覧。</span><span class="sxs-lookup"><span data-stu-id="13fca-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="13fca-108">**動詞**</span><span class="sxs-lookup"><span data-stu-id="13fca-108">**Verb**</span></span>|<span data-ttu-id="13fca-109">**値**</span><span class="sxs-lookup"><span data-stu-id="13fca-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13fca-110">開く</span><span class="sxs-lookup"><span data-stu-id="13fca-110">Open</span></span>  <br/> |<span data-ttu-id="13fca-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="13fca-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="13fca-112">Reply</span><span class="sxs-lookup"><span data-stu-id="13fca-112">Reply</span></span>  <br/> |<span data-ttu-id="13fca-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="13fca-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="13fca-114">全員へ返信</span><span class="sxs-lookup"><span data-stu-id="13fca-114">Reply to All</span></span>  <br/> |<span data-ttu-id="13fca-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="13fca-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="13fca-116">Forward</span><span class="sxs-lookup"><span data-stu-id="13fca-116">Forward</span></span>  <br/> |<span data-ttu-id="13fca-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="13fca-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="13fca-118">印刷</span><span class="sxs-lookup"><span data-stu-id="13fca-118">Print</span></span>  <br/> |<span data-ttu-id="13fca-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="13fca-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="13fca-120">としてを保存します。</span><span class="sxs-lookup"><span data-stu-id="13fca-120">Save As</span></span>  <br/> |<span data-ttu-id="13fca-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="13fca-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="13fca-122">フォルダーへの返信</span><span class="sxs-lookup"><span data-stu-id="13fca-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="13fca-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="13fca-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="13fca-124">ユーザーが動詞を選択したときに対応するアクションを実行するのには、フォームの[IMAPIForm::DoVerb](imapiform-doverb.md)メソッドの呼び出しでその定数を渡します。</span><span class="sxs-lookup"><span data-stu-id="13fca-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="13fca-125">動詞にアクセスする、フォームのビューアーで、ほか、ユーザーはフォームから直接動詞をもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="13fca-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="13fca-126">などのいくつかのフォーム オブジェクトを許可すると、ユーザーがフォーム上を右クリックし、コンテキスト メニューから**印刷**を選択する**印刷**の動詞を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="13fca-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

