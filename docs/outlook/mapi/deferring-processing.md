---
title: 処理の延期
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2c4577a35315c9df0055e97de26dd0baf1a2b489
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580587"
---
# <a name="deferring-processing"></a>処理の延期

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メソッドの呼び出しを可能な限りに MAPI_DEFERRED_ERRORS フラグを渡します。 MAPI メソッドの呼び出しの多くは、一度に複数のタスクを実行することができます設定したり、不要になった結果を得るまでか、要求されたタスクを延期するのにはプロバイダーの原因と、このフラグを受け入れるように最適化されています。
  
などの場合はフォルダーを開くには、 [IMsgStore::OpenEntry](imsgstore-openentry.md)に MAPI_DEFERRED_ERRORS を渡すと、フォルダー、および使用可能なリモート呼び出しの開始延期できるようにフォルダーの**GetHierarchyTable**または**の呼び出しなどの別の呼び出しを行うまでGetProps**方法です。 **GetProps**と**GetHierarchyTable**の両方はすぐに実行する必要があるタスク、サービス ・ プロバイダーからデータを返す必要があります。 
  
処理を延期するのには別の方法は、呼び出しを行うことないだけがです。 把握しているユーザーを使用して、ユーザーがリソースや処理時間の浪費を得ることが、呼び出しを行う方が良い場合を指定できます。 どちらかですると、ユーザーが気付くことはありませんの呼び出しを行うかを設定していないすべてのパフォーマンスを向上させる機会があります。
  
たとえば、多数のメッセージを移動するメッセージ ・ ストアから 1 秒あたりの 1 つ以上の通知を受信するときは、状況を検討します。 操作の完了の割合を示す進行状況のインジケーターが表示されます。 ユーザー一般認識は、ありませんこの操作は数秒が経過するまでに時間がかかることを。 したがって、プログレス インジケーターを更新する場合は、変更しないでください、最低 4 秒間の移動操作を開始した後まで。 操作が高速にしたときの一般的なケースで時間の節約、操作が低速にすると適切なタイミングでユーザーに通知します。
  

