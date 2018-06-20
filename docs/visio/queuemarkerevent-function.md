---
title: QUEUEMARKEREVENT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60107
localization_priority: Normal
ms.assetid: b4671715-4209-7774-c174-c19dc9721a02
description: アプリケーション、アドオン、Microsoft の Visual Basic for Applications (VBA) コード、または COM アドインにマーカー イベントを発生するが発生します。
ms.openlocfilehash: b9175caf0845530c93f6db15e286f3eae21ea415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806134"
---
# <a name="queuemarkerevent-function"></a><span data-ttu-id="40967-103">QUEUEMARKEREVENT 関数</span><span class="sxs-lookup"><span data-stu-id="40967-103">QUEUEMARKEREVENT Function</span></span>

<span data-ttu-id="40967-104">アプリケーション、アドオン、Microsoft の Visual Basic for Applications (VBA) コード、または COM アドインにマーカー イベントを発生するが発生します。</span><span class="sxs-lookup"><span data-stu-id="40967-104">Causes the application to fire a marker event to your add-on, Microsoft Visual Basic for Applications (VBA) code, or COM add-in.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="40967-105">構文</span><span class="sxs-lookup"><span data-stu-id="40967-105">Syntax</span></span>

<span data-ttu-id="40967-106">QUEUEMARKEREVENT (* * *event_string* * *)</span><span class="sxs-lookup"><span data-stu-id="40967-106">QUEUEMARKEREVENT (** *event_string* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="40967-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="40967-107">Parameters</span></span>

|<span data-ttu-id="40967-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="40967-108">**Name**</span></span>|<span data-ttu-id="40967-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="40967-109">**Required/Optional**</span></span>|<span data-ttu-id="40967-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="40967-110">**Data Type**</span></span>|<span data-ttu-id="40967-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="40967-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="40967-112">_event_string_</span><span class="sxs-lookup"><span data-stu-id="40967-112">_event_string_</span></span> <br/> |<span data-ttu-id="40967-113">必須</span><span class="sxs-lookup"><span data-stu-id="40967-113">Required</span></span>  <br/> |<span data-ttu-id="40967-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="40967-114">**String**</span></span> <br/> | <span data-ttu-id="40967-115">イベント ハンドラーに渡す文字列です。</span><span class="sxs-lookup"><span data-stu-id="40967-115">The string to pass to your event handler.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40967-116">備考</span><span class="sxs-lookup"><span data-stu-id="40967-116">Remarks</span></span>

<span data-ttu-id="40967-117">QUEUEMARKEREVENT 関数には、シェイプ シートのセルからコードを通知し、ソリューションに固有の情報を渡す方法を開発者が用意されています。</span><span class="sxs-lookup"><span data-stu-id="40967-117">The QUEUEMARKEREVENT function provides developers with a way to notify their code from a ShapeSheet cell, and pass solution-specific information.</span></span> <span data-ttu-id="40967-118">QUEUEMARKEREVENT 関数で数式を含むセルが評価されると、アプリケーションはマーカー イベントを発生し、 **MarkerEvent**イベントをリッスンしているすべてのイベント ハンドラーに_event_string_を渡します。</span><span class="sxs-lookup"><span data-stu-id="40967-118">When the cell containing the formula with the QUEUEMARKEREVENT function is evaluated, the application fires a marker event and passes  _event_string_ to all event handlers that are listening to the **MarkerEvent** event.</span></span> 
  
<span data-ttu-id="40967-119">マーカー イベントの詳細については、 **QueueMarkerEvent**メソッドおよび**MarkerEvent**イベントのトピックでは、Visio オートメーション リファレンス 』 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40967-119">For more information about marker events, see the **QueueMarkerEvent** method and **MarkerEvent** event topics in the Microsoft Visio Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="40967-120">例</span><span class="sxs-lookup"><span data-stu-id="40967-120">Example</span></span>

<span data-ttu-id="40967-121">QUEUEMARKEREVENT ("MyCustomNotification")</span><span class="sxs-lookup"><span data-stu-id="40967-121">QUEUEMARKEREVENT ("MyCustomNotification")</span></span> 
  
<span data-ttu-id="40967-122">アプリケーションが、マーカー イベントを発生し、 **MarkerEvent**イベントをリッスンしているイベント ハンドラーに、文字列"MyCustomNotification"を渡します。</span><span class="sxs-lookup"><span data-stu-id="40967-122">Causes the application to fire a marker event, and passes the string "MyCustomNotification" to event handlers that are listening to the **MarkerEvent** event.</span></span> 
  

