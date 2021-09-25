---
title: 処理の延期
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 909e25601e572e3373883b83791f4d8a785fdbea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588204"
---
# <a name="deferring-processing"></a>処理の延期

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メソッド呼び出MAPI_DEFERRED_ERRORS可能な限り、このフラグを渡します。 MAPI メソッドの呼び出しの多くは、このフラグを受け入れするために最適化されています。これにより、プロバイダーは、複数のタスクを一度に実行するか、結果を待てなくなるまで、要求されたタスクを延期します。
  
たとえば、MAPI_DEFERRED_ERRORS を [IMsgStore::OpenEntry](imsgstore-openentry.md) に渡してフォルダーを開く場合、フォルダーの **GetHierarchyTable** メソッドや **GetProps** メソッドへの呼び出しなど、別の呼び出しを行うまで、フォルダーの開始とリモート呼び出しの可能性を延期できます。 **GetHierarchyTable と** **GetProps** の両方で、すぐに実行する必要があるタスクであるサービス プロバイダーからのデータの戻り値が必要です。 
  
処理を延期するもう 1 つの方法は、単に呼び出しを行うのではありません。 ユーザーを認識し、ユーザーがリソースの消耗や処理時間を感知できる場合は、いつ呼び出しを行うのが理にかなったのか判断できます。 ユーザーが気付かないときや、呼び出しを行ってパフォーマンスを向上させる機会があります。
  
たとえば、多数のメッセージを移動しているメッセージ ストアから 1 秒に 2 つ以上の通知を受け取る状況を考え出します。 進行状況インジケーターが表示され、操作の完了率が示されます。 ユーザーは通常、数秒が経過するまで、この操作が遅いと認識されます。 したがって、進行状況インジケーターを更新する場合は、移動操作の開始から少なくとも 4 秒後まで変更を行う必要があります。 これにより、操作が高速な場合の一般的なケースの時間が節約され、操作が遅いときにユーザーに迅速に通知します。
  

