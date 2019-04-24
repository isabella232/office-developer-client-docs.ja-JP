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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358730"
---
# <a name="queuemarkerevent-function"></a>QUEUEMARKEREVENT 関数

アプリケーションが、アドオン、Microsoft Visual Basic for Applications (VBA) コード、または COM アドインに対してマーカーイベントを発生させます。 
  
## <a name="syntax"></a>構文

QUEUEMARKEREVENT (* * *event_string* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |必須  <br/> |**String** <br/> | イベントハンドラーに渡す文字列。  <br/> |
   
## <a name="remarks"></a>解説

開発者は QUEUEMARKEREVENT 関数を使用して、シェイプシートのセルからコードを通知したり、ソリューション固有の情報を渡すことができます。 QUEUEMARKEREVENT 関数を使用して数式を含むセルが評価されると、アプリケーションは marker イベントを発生させ、 **MarkerEvent**イベントをリッスンしているすべてのイベントハンドラーに_event_string_を渡します。 
  
マーカーイベントの詳細については、Microsoft Visio Automation リファレンスの**QueueMarkerEvent**メソッドと**MarkerEvent**イベントのトピックを参照してください。 
  
## <a name="example"></a>例

QUEUEMARKEREVENT ("MyCustomNotification") 
  
アプリケーションはマーカー イベントを発生し、**MarkerEvent** イベントを受信しているイベント ハンドラーに文字列 "MyCustomNotification" を渡します。 
  

