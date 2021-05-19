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
description: アプリケーションが、アドオン、Microsoft Visual Basic for Applications (VBA) コード、または COM アドインにマーカー イベントを発生します。
ms.openlocfilehash: 841f6acc63497a6f0b8930c89534b5f8b04c0393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418807"
---
# <a name="queuemarkerevent-function"></a>QUEUEMARKEREVENT 関数

アプリケーションが、アドオン、Microsoft Visual Basic for Applications (VBA) コード、または COM アドインにマーカー イベントを発生します。 
  
## <a name="syntax"></a>構文

QUEUEMARKEREVENT (** *event_string* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |必須  <br/> |**String** <br/> | イベント ハンドラーに渡す文字列。  <br/> |
   
## <a name="remarks"></a>注釈

開発者は QUEUEMARKEREVENT 関数を使用して、シェイプシートのセルからコードを通知したり、ソリューション固有の情報を渡すことができます。 QUEUEMARKEREVENT 関数を持つ数式を含むセルを評価すると、アプリケーションはマーカー イベントを発生し _、markerEvent_ イベントをリッスンしているすべてのイベント ハンドラーに event_stringを渡します。 
  
マーカー イベントの詳細については、「Microsoft Visio オートメーション リファレンス」の **「QueueMarkerEvent** メソッドと **MarkerEvent** イベントのトピック」を参照してください。 
  
## <a name="example"></a>例

QUEUEMARKEREVENT ("MyCustomNotification") 
  
アプリケーションはマーカー イベントを発生し、**MarkerEvent** イベントを受信しているイベント ハンドラーに文字列 "MyCustomNotification" を渡します。 
  

