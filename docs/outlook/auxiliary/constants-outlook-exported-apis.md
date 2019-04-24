---
title: (Outlook エクスポート Api) 定数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: このトピックでは、Outlook でエクスポートされる api の定数定義について説明します。
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319874"
---
# <a name="constants-outlook-exported-apis"></a><span data-ttu-id="d4c7f-103">(Outlook エクスポート Api) 定数</span><span class="sxs-lookup"><span data-stu-id="d4c7f-103">Constants (Outlook exported APIs)</span></span>

<span data-ttu-id="d4c7f-104">このトピックでは、Outlook でエクスポートされる api の定数定義について説明します。</span><span class="sxs-lookup"><span data-stu-id="d4c7f-104">This topic contains constant definitions for APIs that Outlook exports.</span></span>
  
## <a name="definitions-for-time-zone-support"></a><span data-ttu-id="d4c7f-105">タイムゾーンサポートの定義</span><span class="sxs-lookup"><span data-stu-id="d4c7f-105">Definitions for Time Zone support</span></span>

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a><span data-ttu-id="d4c7f-106">カテゴリサポートの定義</span><span class="sxs-lookup"><span data-stu-id="d4c7f-106">Definitions for Category support</span></span>

|<span data-ttu-id="d4c7f-107">**定数**</span><span class="sxs-lookup"><span data-stu-id="d4c7f-107">**Constant**</span></span>|<span data-ttu-id="d4c7f-108">**定義**</span><span class="sxs-lookup"><span data-stu-id="d4c7f-108">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d4c7f-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="d4c7f-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="d4c7f-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d4c7f-110">0x00000001</span></span>  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a><span data-ttu-id="d4c7f-111">その他のディスパッチ識別子</span><span class="sxs-lookup"><span data-stu-id="d4c7f-111">Miscellaneous dispatch identifiers</span></span>

<span data-ttu-id="d4c7f-112">Outlook では、次のディスパッチ識別子 (dispid) が公開されているため、開発者は[IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke)を使用して、対応するプロパティやメソッドにアクセスしたり、対応するイベントを聞いたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="d4c7f-112">Outlook exposes the following dispatch identifiers (dispids) so that developers can use [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) to access the corresponding property or method, or listen to the corresponding event.</span></span> 
  
|<span data-ttu-id="d4c7f-113">**関連する定数**</span><span class="sxs-lookup"><span data-stu-id="d4c7f-113">**Associated constant**</span></span>|<span data-ttu-id="d4c7f-114">**Dispid 値**</span><span class="sxs-lookup"><span data-stu-id="d4c7f-114">**Dispid value**</span></span>|<span data-ttu-id="d4c7f-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="d4c7f-115">**Description**</span></span>|<span data-ttu-id="d4c7f-116">**適用可能なインターフェイス**</span><span class="sxs-lookup"><span data-stu-id="d4c7f-116">**Applicable interface**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d4c7f-117">**dispidfdirty**</span><span class="sxs-lookup"><span data-stu-id="d4c7f-117">**dispidFDirty**</span></span> <br/> |<span data-ttu-id="d4c7f-118">0xf024</span><span class="sxs-lookup"><span data-stu-id="d4c7f-118">0xF024</span></span>  <br/> |<span data-ttu-id="d4c7f-119">アイテムの対応するプロパティを呼び出して、アイテムが変更されたが保存されていないかどうかを確認するために使用します。</span><span class="sxs-lookup"><span data-stu-id="d4c7f-119">Used to invoke the corresponding property on an item to verify whether the item has been modified but has not been saved.</span></span>  <br/> |<span data-ttu-id="d4c7f-120">アイテムレベルのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="d4c7f-120">Item-level objects</span></span>  <br/> |
|<span data-ttu-id="d4c7f-121">**dispidShowSenderPhoto**</span><span class="sxs-lookup"><span data-stu-id="d4c7f-121">**dispidShowSenderPhoto**</span></span> <br/> |<span data-ttu-id="d4c7f-122">0xf・0</span><span class="sxs-lookup"><span data-stu-id="d4c7f-122">0xF0D0</span></span>  <br/> |<span data-ttu-id="d4c7f-123">指定した引数に基づいて連絡先の画像を表示するかどうかを指定するために、エクスプローラーまたはインスペクターの対応するメソッドを呼び出すために使用します。</span><span class="sxs-lookup"><span data-stu-id="d4c7f-123">Used to invoke the corresponding method on the explorer or inspector to specify whether to display a contact's picture, based on a given argument.</span></span>  <br/> |<span data-ttu-id="d4c7f-124">エクスプローラーまたはインスペクター</span><span class="sxs-lookup"><span data-stu-id="d4c7f-124">Explorer or inspector</span></span>  <br/> |
|<span data-ttu-id="d4c7f-125">**dispidbeforeprint**</span><span class="sxs-lookup"><span data-stu-id="d4c7f-125">**dispidBeforePrint**</span></span> <br/> |<span data-ttu-id="d4c7f-126">0xFC8E</span><span class="sxs-lookup"><span data-stu-id="d4c7f-126">0xFC8E</span></span>  <br/> |<span data-ttu-id="d4c7f-127">**IDispatch:: Invoke**関数からのイベントを処理するために使用します。このイベントは、印刷操作の前に発生します。</span><span class="sxs-lookup"><span data-stu-id="d4c7f-127">Used to handle the event from the **IDispatch::Invoke** function that fires before a printing operation.</span></span>  <br/> |<span data-ttu-id="d4c7f-128">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="d4c7f-128">Application</span></span>  <br/> |
|<span data-ttu-id="d4c7f-129">**dispidEventReadComplete**</span><span class="sxs-lookup"><span data-stu-id="d4c7f-129">**dispidEventReadComplete**</span></span> <br/> |<span data-ttu-id="d4c7f-130">0xfc8f</span><span class="sxs-lookup"><span data-stu-id="d4c7f-130">0xFC8F</span></span>  <br/> |<span data-ttu-id="d4c7f-131">Outlook がアイテムのプロパティの読み取りを完了したときに発生する**IDispatch:: Invoke**関数からのイベントを処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d4c7f-131">Used to handle the event from the **IDispatch::Invoke** function that fires when Outlook has completed reading the properties of the item.</span></span>  <br/> |<span data-ttu-id="d4c7f-132">アイテムレベルのオブジェクト</span><span class="sxs-lookup"><span data-stu-id="d4c7f-132">Item-level objects</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4c7f-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="d4c7f-133">See also</span></span>

- [<span data-ttu-id="d4c7f-134">Outlook でエクスポートされている API</span><span class="sxs-lookup"><span data-stu-id="d4c7f-134">Outlook exported APIs</span></span>](outlook-exported-apis.md)
- [<span data-ttu-id="d4c7f-135">Outlook によりエクスポートされる API について</span><span class="sxs-lookup"><span data-stu-id="d4c7f-135">About APIs exported by Outlook</span></span>](about-apis-exported-by-outlook.md)
- [<span data-ttu-id="d4c7f-136">Outlook アイテムが変更されたが保存されていないかどうかを確認する (Outlook の補助リファレンス)</span><span class="sxs-lookup"><span data-stu-id="d4c7f-136">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [<span data-ttu-id="d4c7f-137">Outlook (Outlook の補助リファレンス) で、連絡先の画像を表示するかどうかを指定</span><span class="sxs-lookup"><span data-stu-id="d4c7f-137">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [<span data-ttu-id="d4c7f-138">使用可能なイベントの dispid (Outlook エクスポート Api)</span><span class="sxs-lookup"><span data-stu-id="d4c7f-138">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)

