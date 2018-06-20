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
# <a name="queuemarkerevent-function"></a>QUEUEMARKEREVENT 関数

アプリケーション、アドオン、Microsoft の Visual Basic for Applications (VBA) コード、または COM アドインにマーカー イベントを発生するが発生します。 
  
## <a name="syntax"></a>構文

QUEUEMARKEREVENT (* * *event_string* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | イベント ハンドラーに渡す文字列です。  <br/> |
   
## <a name="remarks"></a>備考

QUEUEMARKEREVENT 関数には、シェイプ シートのセルからコードを通知し、ソリューションに固有の情報を渡す方法を開発者が用意されています。 QUEUEMARKEREVENT 関数で数式を含むセルが評価されると、アプリケーションはマーカー イベントを発生し、 **MarkerEvent**イベントをリッスンしているすべてのイベント ハンドラーに_event_string_を渡します。 
  
マーカー イベントの詳細については、 **QueueMarkerEvent**メソッドおよび**MarkerEvent**イベントのトピックでは、Visio オートメーション リファレンス 』 を参照してください。 
  
## <a name="example"></a>例

QUEUEMARKEREVENT ("MyCustomNotification") 
  
アプリケーションが、マーカー イベントを発生し、 **MarkerEvent**イベントをリッスンしているイベント ハンドラーに、文字列"MyCustomNotification"を渡します。 
  

