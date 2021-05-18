---
title: アドレス帳通知の処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 122e50328272a4009e5a129233d449613817dfc8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413536"
---
# <a name="handing-address-book-notification"></a>アドレス帳通知の処理
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳通知を使用すると、クライアントは、任意のアドレス帳エントリまたは特定のエントリに発生するイベントを学習できます。 これらの通知に登録するには、MAPI アドレス帳を使用して [IAddrBook::Advise](iaddrbook-advise.md) を呼び出するか [、IMAPITable::Advise](imapitable-advise.md)を呼び出してアドレス帳コンテナーの階層またはコンテンツ テーブルを使用します。 
  
特定のエントリの通知に登録する場合はアドレス帳コンテナー、配布リスト、またはメッセージング ユーザーのエントリ識別子を指定し、アドレス帳全体で通知に登録する場合は NULL を指定します。 エントリ識別子は、アドレス帳コンテナー内のメッセージング ユーザーまたは配布リストを表す必要があります。 **IAddrBook::Advise** は、このエントリ識別子を調べて、対応するオブジェクトを担当するアドレス帳プロバイダーを特定し、適切なアドレス帳プロバイダーの [IABLogon::Advise](iablogon-advise.md) メソッドに呼び出しを転送します。 
  
クライアントは、アドレス帳エントリで次の種類のイベントに登録できます。
  
- 重大なエラー
    
- オブジェクト イベント (作成、変更、削除、移動、またはコピー)
    
- 変更されたテーブル
    
通常、登録はアドレス帳コンテナーの内容と階層テーブルでのみ発生します。 クライアントが下位レベルのメッセージング ユーザーおよび配布リスト オブジェクトに登録されるのはまれです。 これは、次の理由が理由です。
  
- 多くのアドレス帳プロバイダーは、メッセージング ユーザーと配布リストの通知をサポートしていない。
    
- テーブル通知は、変更を追跡し、ユーザーに報告するのに十分です。
    

