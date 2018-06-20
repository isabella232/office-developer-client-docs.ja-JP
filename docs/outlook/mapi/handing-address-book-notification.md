---
title: アドレス帳の通知の処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0dc4bb48-c8a1-447f-9e38-1c234a358fca
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f198be78dd36a6d0c9439da68ab322cd8cfa4172
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800168"
---
# <a name="handing-address-book-notification"></a>アドレス帳の通知の処理
  
**適用されます**: Outlook 
  
アドレス帳の通知は、任意のアドレス帳のエントリに、または特定のエントリに、発生するイベントを取得するためのクライアントを使用できます。 [IAddrBook::Advise](iaddrbook-advise.md)を呼び出すことによって、MAPI アドレス帳またはアドレス帳コンテナーの階層構造または内容のテーブルを介して、これらの通知を登録するには、 [IMAPITable::Advise](imapitable-advise.md)を呼び出すことです。 
  
全体のアドレス帳についての通知を登録する場合、特定のエントリでの通知を登録する場合は、アドレス帳コンテナー、配布リスト、またはメッセージングのユーザーのエントリの識別子を指定します。 エントリの識別子には、メッセージングのユーザーや、アドレス帳コンテナー内の配布リストを表す必要があります。 **IAddrBook::Advise**は、どのアドレス帳プロバイダーは、対応するオブジェクトを決定するには、このエントリ id を検証し、適切なアドレス帳プロバイダーの[IABLogon::Advise](iablogon-advise.md)メソッドの呼び出しを転送します。 
  
クライアントは、次の種類のアドレス帳のエントリのイベントを登録できます。
  
- 重大なエラー
    
- (作成、変更、削除、移動、またはコピー) のオブジェクトのイベントのいずれか
    
- 変更テーブル
    
通常、登録は、アドレス帳コンテナーのコンテンツおよび階層テーブルでのみ発生します。 クライアントがメッセージングのユーザーと配布リスト内のオブジェクトの下位レベルで登録することはまれです。 です。
  
- アドレス帳プロバイダーの多くは、メッセージングのユーザーと配布リストの通知をサポートしていません。
    
- テーブルの通知は、変更を追跡し、ユーザーに報告のための十分です。
    

