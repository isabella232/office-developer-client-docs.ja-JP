---
title: (Outlook エクスポート Api) 定数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: このトピックには、Outlook にエクスポートする Api の定数の定義が含まれています。
ms.openlocfilehash: 8b7a9d70b2fc5d26c52a8729797221a44526360c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564466"
---
# <a name="constants-outlook-exported-apis"></a><span data-ttu-id="e4938-103">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="e4938-103">Constants (Outlook exported APIs)</span></span>

<span data-ttu-id="e4938-104">このトピックには、Outlook にエクスポートする Api の定数の定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e4938-104">This topic contains constant definitions for APIs that Outlook exports.</span></span>
  
## <a name="definitions-for-time-zone-support"></a><span data-ttu-id="e4938-105">タイム ゾーンの定義をサポートします。</span><span class="sxs-lookup"><span data-stu-id="e4938-105">Definitions for Time Zone support</span></span>

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a><span data-ttu-id="e4938-106">カテゴリの定義をサポートします。</span><span class="sxs-lookup"><span data-stu-id="e4938-106">Definitions for Category support</span></span>

|<span data-ttu-id="e4938-107">**定数**</span><span class="sxs-lookup"><span data-stu-id="e4938-107">**Constant**</span></span>|<span data-ttu-id="e4938-108">**定義**</span><span class="sxs-lookup"><span data-stu-id="e4938-108">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e4938-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="e4938-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="e4938-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e4938-110">0x00000001</span></span>  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a><span data-ttu-id="e4938-111">その他のディスパッチ識別子</span><span class="sxs-lookup"><span data-stu-id="e4938-111">Miscellaneous dispatch identifiers</span></span>

<span data-ttu-id="e4938-112">開発者は、対応するプロパティまたはメソッドにアクセスしたり、対応するイベントを待機する[:invoke](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke)を使用できるように、outlook は次のディスパッチ識別子 (dispid) を公開します。</span><span class="sxs-lookup"><span data-stu-id="e4938-112">Outlook exposes the following dispatch identifiers (dispids) so that developers can use [IDispatch::Invoke](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) to access the corresponding property or method, or listen to the corresponding event.</span></span> 
  
|<span data-ttu-id="e4938-113">**関連付けられた定数**</span><span class="sxs-lookup"><span data-stu-id="e4938-113">**Associated constant**</span></span>|<span data-ttu-id="e4938-114">**Dispid 値**</span><span class="sxs-lookup"><span data-stu-id="e4938-114">**Dispid value**</span></span>|<span data-ttu-id="e4938-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="e4938-115">**Description**</span></span>|<span data-ttu-id="e4938-116">**適用可能なインタ フェース**</span><span class="sxs-lookup"><span data-stu-id="e4938-116">**Applicable interface**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e4938-117">**dispidFDirty**</span><span class="sxs-lookup"><span data-stu-id="e4938-117">**dispidFDirty**</span></span> <br/> |<span data-ttu-id="e4938-118">0xF024</span><span class="sxs-lookup"><span data-stu-id="e4938-118">0xF024</span></span>  <br/> |<span data-ttu-id="e4938-119">アイテムが変更されていますが保存されていないかどうかを確認する項目に対応するプロパティを呼び出すために使用します。</span><span class="sxs-lookup"><span data-stu-id="e4938-119">Used to invoke the corresponding property on an item to verify whether the item has been modified but has not been saved.</span></span>  <br/> |<span data-ttu-id="e4938-120">アイテム レベルのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="e4938-120">Item-level objects</span></span>  <br/> |
|<span data-ttu-id="e4938-121">**dispidShowSenderPhoto**</span><span class="sxs-lookup"><span data-stu-id="e4938-121">**dispidShowSenderPhoto**</span></span> <br/> |<span data-ttu-id="e4938-122">0xF0D0</span><span class="sxs-lookup"><span data-stu-id="e4938-122">0xF0D0</span></span>  <br/> |<span data-ttu-id="e4938-123">指定された引数に基づいて、連絡先の画像を表示するかどうかを指定するのには、エクスプ ローラーまたはインスペクターの対応するメソッドを呼び出すために使用します。</span><span class="sxs-lookup"><span data-stu-id="e4938-123">Used to invoke the corresponding method on the explorer or inspector to specify whether to display a contact's picture, based on a given argument.</span></span>  <br/> |<span data-ttu-id="e4938-124">エクスプ ローラーまたはインスペクター</span><span class="sxs-lookup"><span data-stu-id="e4938-124">Explorer or inspector</span></span>  <br/> |
|<span data-ttu-id="e4938-125">**dispidBeforePrint**</span><span class="sxs-lookup"><span data-stu-id="e4938-125">**dispidBeforePrint**</span></span> <br/> |<span data-ttu-id="e4938-126">0xFC8E</span><span class="sxs-lookup"><span data-stu-id="e4938-126">0xFC8E</span></span>  <br/> |<span data-ttu-id="e4938-127">印刷操作の前に起動する **:invoke**関数からイベントを処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e4938-127">Used to handle the event from the **IDispatch::Invoke** function that fires before a printing operation.</span></span>  <br/> |<span data-ttu-id="e4938-128">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="e4938-128">Application</span></span>  <br/> |
|<span data-ttu-id="e4938-129">**dispidEventReadComplete**</span><span class="sxs-lookup"><span data-stu-id="e4938-129">**dispidEventReadComplete**</span></span> <br/> |<span data-ttu-id="e4938-130">0xFC8F</span><span class="sxs-lookup"><span data-stu-id="e4938-130">0xFC8F</span></span>  <br/> |<span data-ttu-id="e4938-131">Outlook がアイテムのプロパティの読み取りを完了したときに発生する **:invoke**関数からイベントを処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e4938-131">Used to handle the event from the **IDispatch::Invoke** function that fires when Outlook has completed reading the properties of the item.</span></span>  <br/> |<span data-ttu-id="e4938-132">アイテム レベルのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="e4938-132">Item-level objects</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e4938-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="e4938-133">See also</span></span>

- [<span data-ttu-id="e4938-134">Outlook でエクスポートされている API</span><span class="sxs-lookup"><span data-stu-id="e4938-134">Outlook exported APIs</span></span>](outlook-exported-apis.md)
- [<span data-ttu-id="e4938-135">Outlook によりエクスポートされる API について</span><span class="sxs-lookup"><span data-stu-id="e4938-135">About APIs exported by Outlook</span></span>](about-apis-exported-by-outlook.md)
- [<span data-ttu-id="e4938-136">Outlook アイテムが変更されたが保存されていないかどうかを確認する (Outlook の補助リファレンス)</span><span class="sxs-lookup"><span data-stu-id="e4938-136">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [<span data-ttu-id="e4938-137">Outlook (Outlook の補助リファレンス) で、連絡先の画像を表示するかどうかを指定</span><span class="sxs-lookup"><span data-stu-id="e4938-137">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/en-us/library/office/gg262879.aspx)
- [<span data-ttu-id="e4938-138">使用可能なイベントの dispid (Outlook エクスポート Api)</span><span class="sxs-lookup"><span data-stu-id="e4938-138">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)

