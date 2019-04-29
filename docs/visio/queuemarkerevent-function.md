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
description: アプリケーションが、アドオン、Microsoft Visual Basic for Applications (VBA) コード、または COM アドインに対してマーカーイベントを発生させます。
ms.openlocfilehash: 841f6acc63497a6f0b8930c89534b5f8b04c0393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418807"
---
# <a name="queuemarkerevent-function"></a><span data-ttu-id="8b97e-103">QUEUEMARKEREVENT 関数</span><span class="sxs-lookup"><span data-stu-id="8b97e-103">QUEUEMARKEREVENT Function</span></span>

<span data-ttu-id="8b97e-104">アプリケーションが、アドオン、Microsoft Visual Basic for Applications (VBA) コード、または COM アドインに対してマーカーイベントを発生させます。</span><span class="sxs-lookup"><span data-stu-id="8b97e-104">Causes the application to fire a marker event to your add-on, Microsoft Visual Basic for Applications (VBA) code, or COM add-in.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8b97e-105">構文</span><span class="sxs-lookup"><span data-stu-id="8b97e-105">Syntax</span></span>

<span data-ttu-id="8b97e-106">QUEUEMARKEREVENT (\* \* *event_string* \* \*)</span><span class="sxs-lookup"><span data-stu-id="8b97e-106">QUEUEMARKEREVENT (\*\* *event_string* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8b97e-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8b97e-107">Parameters</span></span>

|<span data-ttu-id="8b97e-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="8b97e-108">**Name**</span></span>|<span data-ttu-id="8b97e-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="8b97e-109">**Required/Optional**</span></span>|<span data-ttu-id="8b97e-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="8b97e-110">**Data Type**</span></span>|<span data-ttu-id="8b97e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="8b97e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8b97e-112">_event_string_</span><span class="sxs-lookup"><span data-stu-id="8b97e-112">_event_string_</span></span> <br/> |<span data-ttu-id="8b97e-113">必須</span><span class="sxs-lookup"><span data-stu-id="8b97e-113">Required</span></span>  <br/> |<span data-ttu-id="8b97e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="8b97e-114">**String**</span></span> <br/> | <span data-ttu-id="8b97e-115">イベントハンドラーに渡す文字列。</span><span class="sxs-lookup"><span data-stu-id="8b97e-115">The string to pass to your event handler.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b97e-116">注釈</span><span class="sxs-lookup"><span data-stu-id="8b97e-116">Remarks</span></span>

<span data-ttu-id="8b97e-117">開発者は QUEUEMARKEREVENT 関数を使用して、シェイプシートのセルからコードを通知したり、ソリューション固有の情報を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="8b97e-117">The QUEUEMARKEREVENT function provides developers with a way to notify their code from a ShapeSheet cell, and pass solution-specific information.</span></span> <span data-ttu-id="8b97e-118">QUEUEMARKEREVENT 関数を使用して数式を含むセルが評価されると、アプリケーションは marker イベントを発生させ、 **MarkerEvent**イベントをリッスンしているすべてのイベントハンドラーに_event_string_を渡します。</span><span class="sxs-lookup"><span data-stu-id="8b97e-118">When the cell containing the formula with the QUEUEMARKEREVENT function is evaluated, the application fires a marker event and passes  _event_string_ to all event handlers that are listening to the **MarkerEvent** event.</span></span> 
  
<span data-ttu-id="8b97e-119">マーカーイベントの詳細については、Microsoft Visio Automation リファレンスの**QueueMarkerEvent**メソッドと**MarkerEvent**イベントのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b97e-119">For more information about marker events, see the **QueueMarkerEvent** method and **MarkerEvent** event topics in the Microsoft Visio Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8b97e-120">例</span><span class="sxs-lookup"><span data-stu-id="8b97e-120">Example</span></span>

<span data-ttu-id="8b97e-121">QUEUEMARKEREVENT ("MyCustomNotification")</span><span class="sxs-lookup"><span data-stu-id="8b97e-121">QUEUEMARKEREVENT ("MyCustomNotification")</span></span> 
  
<span data-ttu-id="8b97e-122">アプリケーションはマーカー イベントを発生し、**MarkerEvent** イベントを受信しているイベント ハンドラーに文字列 "MyCustomNotification" を渡します。</span><span class="sxs-lookup"><span data-stu-id="8b97e-122">Causes the application to fire a marker event, and passes the string "MyCustomNotification" to event handlers that are listening to the **MarkerEvent** event.</span></span> 
  

