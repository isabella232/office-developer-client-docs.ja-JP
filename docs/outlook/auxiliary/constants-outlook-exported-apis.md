---
title: (Outlook エクスポート Api) 定数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: このトピックでは、エクスポートする API の定数Outlookします。
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319874"
---
# <a name="constants-outlook-exported-apis"></a><span data-ttu-id="ad179-103">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="ad179-103">Constants (Outlook exported APIs)</span></span>

<span data-ttu-id="ad179-104">このトピックでは、エクスポートする API の定数Outlookします。</span><span class="sxs-lookup"><span data-stu-id="ad179-104">This topic contains constant definitions for APIs that Outlook exports.</span></span>
  
## <a name="definitions-for-time-zone-support"></a><span data-ttu-id="ad179-105">タイム ゾーンのサポートの定義</span><span class="sxs-lookup"><span data-stu-id="ad179-105">Definitions for Time Zone support</span></span>

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a><span data-ttu-id="ad179-106">Category サポートの定義</span><span class="sxs-lookup"><span data-stu-id="ad179-106">Definitions for Category support</span></span>

|<span data-ttu-id="ad179-107">**定数**</span><span class="sxs-lookup"><span data-stu-id="ad179-107">**Constant**</span></span>|<span data-ttu-id="ad179-108">**定義**</span><span class="sxs-lookup"><span data-stu-id="ad179-108">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ad179-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="ad179-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="ad179-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ad179-110">0x00000001</span></span>  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a><span data-ttu-id="ad179-111">その他のディスパッチ識別子</span><span class="sxs-lookup"><span data-stu-id="ad179-111">Miscellaneous dispatch identifiers</span></span>

<span data-ttu-id="ad179-112">Outlook開発者が[IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke)を使用して対応するプロパティまたはメソッドにアクセスしたり、対応するイベントをリッスンしたりできるよう、次のディスパッチ識別子 (dispids) を公開します。</span><span class="sxs-lookup"><span data-stu-id="ad179-112">Outlook exposes the following dispatch identifiers (dispids) so that developers can use [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) to access the corresponding property or method, or listen to the corresponding event.</span></span> 
  
|<span data-ttu-id="ad179-113">**関連付けられた定数**</span><span class="sxs-lookup"><span data-stu-id="ad179-113">**Associated constant**</span></span>|<span data-ttu-id="ad179-114">**Dispid 値**</span><span class="sxs-lookup"><span data-stu-id="ad179-114">**Dispid value**</span></span>|<span data-ttu-id="ad179-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="ad179-115">**Description**</span></span>|<span data-ttu-id="ad179-116">**適用可能なインターフェイス**</span><span class="sxs-lookup"><span data-stu-id="ad179-116">**Applicable interface**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ad179-117">**dispidFDirty**</span><span class="sxs-lookup"><span data-stu-id="ad179-117">**dispidFDirty**</span></span> <br/> |<span data-ttu-id="ad179-118">0xF024</span><span class="sxs-lookup"><span data-stu-id="ad179-118">0xF024</span></span>  <br/> |<span data-ttu-id="ad179-119">アイテムの対応するプロパティを呼び出して、アイテムが変更されたが保存されていないかどうかを確認するために使用します。</span><span class="sxs-lookup"><span data-stu-id="ad179-119">Used to invoke the corresponding property on an item to verify whether the item has been modified but has not been saved.</span></span>  <br/> |<span data-ttu-id="ad179-120">アイテム レベルのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="ad179-120">Item-level objects</span></span>  <br/> |
|<span data-ttu-id="ad179-121">**dispidShowSenderPhoto**</span><span class="sxs-lookup"><span data-stu-id="ad179-121">**dispidShowSenderPhoto**</span></span> <br/> |<span data-ttu-id="ad179-122">0xF0D0</span><span class="sxs-lookup"><span data-stu-id="ad179-122">0xF0D0</span></span>  <br/> |<span data-ttu-id="ad179-123">エクスプローラーまたはインスペクターで対応するメソッドを呼び出して、指定した引数に基づいて連絡先の画像を表示するかどうかを指定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="ad179-123">Used to invoke the corresponding method on the explorer or inspector to specify whether to display a contact's picture, based on a given argument.</span></span>  <br/> |<span data-ttu-id="ad179-124">エクスプローラーまたはインスペクター</span><span class="sxs-lookup"><span data-stu-id="ad179-124">Explorer or inspector</span></span>  <br/> |
|<span data-ttu-id="ad179-125">**dispidBeforePrint**</span><span class="sxs-lookup"><span data-stu-id="ad179-125">**dispidBeforePrint**</span></span> <br/> |<span data-ttu-id="ad179-126">0xFC8E</span><span class="sxs-lookup"><span data-stu-id="ad179-126">0xFC8E</span></span>  <br/> |<span data-ttu-id="ad179-127">印刷操作の前に発生する **IDispatch::Invoke** 関数からイベントを処理するために使用します。</span><span class="sxs-lookup"><span data-stu-id="ad179-127">Used to handle the event from the **IDispatch::Invoke** function that fires before a printing operation.</span></span>  <br/> |<span data-ttu-id="ad179-128">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="ad179-128">Application</span></span>  <br/> |
|<span data-ttu-id="ad179-129">**dispidEventReadComplete**</span><span class="sxs-lookup"><span data-stu-id="ad179-129">**dispidEventReadComplete**</span></span> <br/> |<span data-ttu-id="ad179-130">0xFC8F</span><span class="sxs-lookup"><span data-stu-id="ad179-130">0xFC8F</span></span>  <br/> |<span data-ttu-id="ad179-131">アイテムのプロパティの読み取りが完了した場合に発生する **IDispatch::Invoke** 関数Outlook処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ad179-131">Used to handle the event from the **IDispatch::Invoke** function that fires when Outlook has completed reading the properties of the item.</span></span>  <br/> |<span data-ttu-id="ad179-132">アイテム レベルのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="ad179-132">Item-level objects</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad179-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="ad179-133">See also</span></span>

- [<span data-ttu-id="ad179-134">Outlook でエクスポートされている API</span><span class="sxs-lookup"><span data-stu-id="ad179-134">Outlook exported APIs</span></span>](outlook-exported-apis.md)
- [<span data-ttu-id="ad179-135">Outlook によりエクスポートされる API について</span><span class="sxs-lookup"><span data-stu-id="ad179-135">About APIs exported by Outlook</span></span>](about-apis-exported-by-outlook.md)
- [<span data-ttu-id="ad179-136">Outlook アイテムが変更されたが保存されていないかどうかを確認する (Outlook の補助リファレンス)</span><span class="sxs-lookup"><span data-stu-id="ad179-136">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [<span data-ttu-id="ad179-137">Outlook (Outlook の補助リファレンス) で、連絡先の画像を表示するかどうかを指定</span><span class="sxs-lookup"><span data-stu-id="ad179-137">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [<span data-ttu-id="ad179-138">使用可能なイベントの dispid (Outlook エクスポート Api)</span><span class="sxs-lookup"><span data-stu-id="ad179-138">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)

