---
title: 通知の取り消し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d0381adadcebca05281353abed78916b994df59e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576535"
---
# <a name="canceling-a-notification"></a>通知の取り消し

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通知を取り消す場合、クライアントはアドバイス ソースの **Unadvise メソッドを呼び出** します。 **Unadvise の呼** び出しは、サービス プロバイダーがアアドバイス シンクへの参照を解放する原因となるので重要です。 サービス プロバイダーがアアドバイス シンクへの参照を維持している限り、アドバイス シンクは引き続き [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) 呼び出しを受信できます。 実際、イベント通知の非同期的な性質のため **、Unadvise** 呼び出しが成功した後でもクライアントに通知できます。 クライアントは、いつでも通知の受信を処理できる必要があります。 
  
サービス プロバイダーの実装は異なるので、通知を取り消す **Unadvise** の呼び出しに失敗したクライアントは、プロバイダーがアドバイス シンクへの参照をいつリリースするのかについて何も想定できません。 一部のサービス プロバイダーは、参照をリリースして、アドバイス ソースをリリースするときにシンクにアドバイスを提供します。 一部のサービス プロバイダーはそうではありません。 サービス プロバイダーがアアドバイス シンクへの参照を維持している限り、その通知シンクは引き続き通知を受け取る可能性があります。 
  

