---
title: 通知の取り消し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fb0972638fdd062c99040694222724566281024f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326405"
---
# <a name="canceling-a-notification"></a>通知の取り消し

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通知を取り消すには、クライアントがアドバイズソースの**アドバイズ**中止メソッドを呼び出します。 **アドバイズ**中止は、サービスプロバイダーがアドバイズシンクへの参照を解放する原因となるため、重要です。 サービスプロバイダーがアドバイズシンクへの参照を保持している限り、アドバイズシンクは引き続き[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)呼び出しを受信できます。 実際には、イベント通知の非同期の性質上、**アドバイズ**に成功した後でもクライアントに通知できます。 クライアントは、いつでも通知の受信を処理できる必要があります。 
  
サービスプロバイダの実装は異なるため、通知を取り消す**アドバイズ**中止の呼び出しに失敗したクライアントは、プロバイダーがアドバイズシンクへの参照を解放したときに何もすることはできません。 一部のサービスプロバイダーは、アドバイズソースをリリースするときに、アドバイズシンクへの参照を解放します。 一部のサービスプロバイダーではできません。 サービスプロバイダーがアドバイズシンクへの参照を保持している限り、アドバイズシンクは通知を引き続き受け取ることができます。 
  

