---
title: 処理の延期
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336933"
---
# <a name="deferring-processing"></a>処理の延期

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI_DEFERRED_ERRORS フラグをメソッド呼び出しに可能な限り渡します。 多くの MAPI メソッド呼び出しは、このフラグを受け入れるように最適化されているため、プロバイダーは、一度に複数のタスクを実行できるようになるか、または結果を待つことができなくなるまで、要求されたタスクを延期することができます。
  
たとえば、MAPI_DEFERRED_ERRORS を[IMsgStore:: openentry](imsgstore-openentry.md)に渡してフォルダーを開くと、フォルダーを開く操作とリモート呼び出しを延期することができます。そのためには、フォルダーの**GetHierarchyTable**の呼び出し、または**その他の呼び出しを実行する必要があります。GetProps**メソッド **GetHierarchyTable**と**GetProps**の両方に、サービスプロバイダーからのデータを返す必要があります。タスクは、すぐに実行する必要があります。 
  
処理を延期する別の方法は、単に通話を行わないことです。 ユーザーを認識し、ユーザーがリソースのドレインや処理時間を感じられる場合は、どのような場合に呼び出しを行うのが妥当かを判断できます。 ユーザーが気付かないときに、または一度に呼び出しを行うことによって、パフォーマンスを向上させる機会があります。
  
たとえば、非常に多くのメッセージを移動しているメッセージストアから1秒間に複数の通知を受信する場合の状況を考えてみます。 操作の完了率を示す進行状況インジケーターが表示されます。 通常、ユーザーは数秒間経過するまで、この操作が遅くなることを感じることはありません。 そのため、進行状況インジケーターを更新している場合は、移動操作の開始後、少なくとも4秒後に変更を加えないでください。 これにより、操作が高速な場合の一般的なケースで時間が節約され、操作が遅くなるときにユーザーにタイムリーに通知されます。
  

