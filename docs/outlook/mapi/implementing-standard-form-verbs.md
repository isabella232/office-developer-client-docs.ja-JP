---
title: 標準フォーム動詞の実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317445"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="7ca27-103">標準フォーム動詞の実装</span><span class="sxs-lookup"><span data-stu-id="7ca27-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="7ca27-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ca27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ca27-105">MAPI は、ユーザーがメニューを選択したり、ボタンをクリックしたりしたときに実行される標準の動詞のセットを定義します。これは、すべてのフォーム閲覧者がサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ca27-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="7ca27-106">各動詞には、exchform で定義されている、識別のための定数が関連付けられています。H ヘッダーファイル。</span><span class="sxs-lookup"><span data-stu-id="7ca27-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="7ca27-107">次の表に、標準のフォーム動詞とそれらに関連付けられている定数を示します。</span><span class="sxs-lookup"><span data-stu-id="7ca27-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="7ca27-108">**Verb**</span><span class="sxs-lookup"><span data-stu-id="7ca27-108">**Verb**</span></span>|<span data-ttu-id="7ca27-109">**値**</span><span class="sxs-lookup"><span data-stu-id="7ca27-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7ca27-110">Open</span><span class="sxs-lookup"><span data-stu-id="7ca27-110">Open</span></span>  <br/> |<span data-ttu-id="7ca27-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="7ca27-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="7ca27-112">返信</span><span class="sxs-lookup"><span data-stu-id="7ca27-112">Reply</span></span>  <br/> |<span data-ttu-id="7ca27-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="7ca27-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="7ca27-114">全員へ返信</span><span class="sxs-lookup"><span data-stu-id="7ca27-114">Reply to All</span></span>  <br/> |<span data-ttu-id="7ca27-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="7ca27-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="7ca27-116">[転送]</span><span class="sxs-lookup"><span data-stu-id="7ca27-116">Forward</span></span>  <br/> |<span data-ttu-id="7ca27-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="7ca27-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="7ca27-118">Print</span><span class="sxs-lookup"><span data-stu-id="7ca27-118">Print</span></span>  <br/> |<span data-ttu-id="7ca27-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="7ca27-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="7ca27-120">名前を付けて保存</span><span class="sxs-lookup"><span data-stu-id="7ca27-120">Save As</span></span>  <br/> |<span data-ttu-id="7ca27-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="7ca27-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="7ca27-122">フォルダーへ投稿</span><span class="sxs-lookup"><span data-stu-id="7ca27-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="7ca27-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="7ca27-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="7ca27-124">ユーザーが動詞を選択するときには、フォームの imapiform の呼び出しで定数を渡します[::D overb](imapiform-doverb.md)メソッドは、対応するアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="7ca27-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="7ca27-125">フォームビューアーから動詞にアクセスするだけでなく、ユーザーはフォームから直接動詞にアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="7ca27-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="7ca27-126">たとえば、一部のフォームオブジェクトでは、ユーザーがフォームを右クリックして、状況依存のメニューから [**印刷**] を選択することによって、 **print**動詞を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="7ca27-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

